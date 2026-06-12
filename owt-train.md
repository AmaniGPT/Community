
# Introduction

For an overview of the `AmaniGPT` project, please refer to the [README](README.md) page.

This guide will take you through the steps for training an `AmaniGPT` model from scratch using the `OpenWebText` dataset.

The [OpenWebText dataset](https://zenodo.org/records/3834942) is a collection of web pages extracted from URLs shared on
Reddit. It is hosted on [Zenodo](https://zenodo.org/) and provides 40 GB of uncompressed text, which can be used to train
simple Large Language Models (LLMs) similar to OpenAI's [GPT-2 model](https://en.wikipedia.org/wiki/GPT-2).

> **FUN FACT:** "amani" is the Swahili word for "peace" :pray:

# Prerequisites

`AmaniGPT` is delivered as a `22 MB` self-contained binary executable. It is written in C# and compiled using
[.NET Native AOT](https://learn.microsoft.com/en-us/dotnet/core/deploying/native-aot/).

.NET supports Windows, Linux, and macOS. During preview, we will focus on Linux (including via
[WSL](https://learn.microsoft.com/en-us/windows/wsl/install) on Windows). In the future, we plan to provide native
binaries for all three platforms, including a library version for use with Android and iOS apps.

We use and recommend Debian for all `AmaniGPT` demos, but .NET supports a wide range of popular Linux distributions
including Ubuntu, Alpine, Fedora, RHEL, and [more](https://learn.microsoft.com/en-us/dotnet/core/install/linux).

**AmaniGPT was built to reduce the cost of AI**. It works just fine on tiny `$5/month` cloud VMs with `1 CPU, 0.5 GB RAM,
and 10 GB SSD storage`. However, for better performance, we recommend VMs with at least `2 CPUs, 4 GB RAM, and 80 GB SSD
storage` (which costs around `$20/month` on [Vultr](https://www.vultr.com/pricing/#cloud-compute)). `AmaniGPT` will use
all the CPUs and RAM you throw at it, so if your budget allows, you can save a lot of time by using larger VMs.

> **TIP:** you do NOT need to know anything about programming or machine learning in order to use `AmaniGPT`. It helps
if you do, but ultimately, you only need to be comfortable using the console/terminal on your computer.

# Installation

Execute the following commands to install `AmaniGPT` on your Linux VM:

```bash
# OPTIONAL (Debian): install unzip if you don't already have it.
sudo apt-get update && sudo apt-get install -y unzip

# Create a directory for AmaniGPT and navigate to it.
mkdir -p ~/amanigpt && cd ~/amanigpt

# Download the latest AmaniGPT binary from GitHub.
wget https://github.com/AmaniGPT/Community/releases/download/v2026.06/amanigpt-linux-x64-v2026.06.zip

# Unzip the downloaded file and delete it to save space.
unzip amanigpt-linux-x64-v2026.06.zip && rm amanigpt-linux-x64-v2026.06.zip

# Make the AmaniGPT binary executable.
chmod +x amani

# Add AmaniGPT to your PATH for easier access.
echo "export PATH=\"$HOME/amanigpt:\$PATH\"" >> ~/.bashrc && source ~/.bashrc

# Confirm that AmaniGPT was added to your PATH (should print "/<home-directory>/amanigpt/amani").
which amani

# Navigate back to your home directory.
cd ~

# Run your first AmaniGPT command (should print something like "AmaniGPT Release Build v2026.06").
amani version
```

Getting stuck? Got questions? Create a [new issue](https://github.com/AmaniGPT/Community/issues) to request help.

> **TIP:** you can download other versions from the [releases page](https://github.com/AmaniGPT/Community/releases). Be
sure to update the URLs and file names in the above commands if you choose a different version.

Now that `AmaniGPT` is installed, you can run `amani help` to see a detailed guide of what you can do with it. You should
also run `amani help --about=shell` to get a quick overview of the syntax for `AmaniGPT` shell-mode commands, which we
will use throughout this guide.

# Configuration

`AmaniGPT` stores configuration in a `settings` directory alongside the binary. Each configuration value is stored in a
separate text file.

To see the current configuration, run `amani show-settings --describe=no`. You should see output similar to the following:

```
SETTING: models-directory-path (string, optional, default: "models")

CURRENT VALUE: models

--------------------------------------------------------------------------------
SETTING: parameter-cache-min-size-mb (integer, optional, default: 128)

CURRENT VALUE: 128

--------------------------------------------------------------------------------
SETTING: parameter-cache-max-size-mb (integer, optional, default: 1,024)

CURRENT VALUE: 1,024
```

To get a detailed description of each setting, run `amani show-settings --describe=yes`.

> **TIP:** you can run `amani show-settings --describe=yes | less` to make it easier to read through the detailed
descriptions. Use the arrow keys to scroll up and down, and press `q` to exit `less` when you're done.

The most important setting for training and using `AmaniGPT` models is the `parameter-cache-max-size-mb` setting, which
controls the maximum amount of RAM used for caching model parameters. The default value is `1,024 MB` (i.e. `1 GB`). To
make it larger (e.g. `2,048 MB`), run the following command:

```bash
amani change-settings --name=parameter-cache-max-size-mb --value=2048
```

Smaller values work too (e.g. if you are running `AmaniGPT` locally on a laptop with limited RAM), but everything will
be slower because `AmaniGPT` spends a lot of time moving model parameters in and out of RAM during training and inference.

> **IMPORTANT:** due to cache management overhead, make sure the VM has at least `4x` the amount of RAM as the value you
set for `parameter-cache-max-size-mb`. For example, if you set it to `2,048 MB` (i.e. `2 GB`), make sure the VM has at
least `8 GB` of RAM. We are working to reduce the overhead in future versions.

# Training

During preview, `AmaniGPT` supports training models using the [OpenWebText dataset](https://zenodo.org/records/3834942).

> **TIP:** you can use any text dataset if you structure it in the same way as the `OpenWebText` dataset. For more details
on the expected structure, run `amani help --about=train-openwebtext | less`. This shows documentation for the training
command we'll be using in this section, which includes a detailed description of the expected dataset structure.

First, create a new model to be trained by running the following command:

```bash
amani create-model --name=owt128 --context-window-size=128
```

You should see output similar to the following:

```
Model created successfully:
            Directory Path: /root/amanigpt/models/owt128
                  Model ID: e907f4ef-6294-4c96-9030-c35dac11ccd4
                Model Name: owt128
       Context Window Size: 128 tokens
      Model Format Version: 1.0

To see all available functions for working with the new model, run:

  amani help --about=model
```

By convention, we use `owt` which is short for `OpenWebText`, followed by the context window size (e.g. `128`) as the
model name, but you can choose any name you like.

The `context-window-size` parameter controls how many tokens the model can process at once during training and inference.
Larger context windows improve model quality but also result in larger models that consume more RAM and CPU during training
and inference. `AmaniGPT` models work surprisingly well even with small context windows which is why we recommend starting
with a small size like `128` for experimentation.

Next, you can start training the model using the `OpenWebText` dataset by running the following command:

```bash
amani train-openwebtext --model-name=owt128 --source=web --max-documents=100
```

This command trains the `owt128` model using `100` documents from the `OpenWebText` dataset **which is streamed directly
from the web**. You should see output similar to the following:


```
Training on up to 100 documents from:

   https://zenodo.org/records/3834942/files/openwebtext.tar.xz

Loading model from directory:

   /root/amanigpt/models/owt128

Training in progress (press 's' to stop early).

             Shard Name: openwebtext/urlsf_subset00-1000_data.xz
              File Name: 0999334-f4e2898d8d9b107fcf662d673ca47bf0.txt
              File Text: It s a well-kept secret, but 95% of the climate mo...
        Vocabulary Size: 15,328 tokens

       Processed shards: 1
        Processed files: 100
        Processed bytes: 505,908
       Processed tokens: 105,828
         Excluded files: 0

   Parameter Cache Size: 80 MB
      Clean Entry Count: 0
       Cache Load Count: 15,328
     Cache Unload Count: 0
   Async Flush Progress: 0.00%
       Total Flush Wait: 0d 0h 0m 0s

           Elapsed time: 0d 0h 0m 5s
      Shards per second: 0.18
       Files per second: 18
       Bytes per second: 93,097
      Tokens per second: 19,474

Flushing model files: 100.00%

Training completed after 148,551 operations.
```

Congratulations! You've just trained your first `AmaniGPT` model from scratch without downloading the 12 GB dataset,
thinking about hardware drivers, or writing a single line of code :rocket:

> **TIP:** you can share your output on the [speed leaderboard](https://github.com/AmaniGPT/Community/issues/1) and see
other people's training speeds too!

To check the size of the trained model, run `du -h ~/amanigpt/models/owt128`. You should see output similar to the
following (i.e. the model is approximately `117 MB` in size):

```
117M    /root/amanigpt/models/owt128/5876856EB51E52E0
117M    /root/amanigpt/models/owt128
```

For larger training runs, we recommend downloading the dataset first as follows:

```bash
# Create a datasets directory and navigate to it.
mkdir -p ~/datasets && cd ~/datasets

# Download the OpenWebText dataset from Zenodo.
wget https://zenodo.org/records/3834942/files/openwebtext.tar.xz
```

The original `OpenWebText` dataset is around `12 GB` compressed and should take anywhere from a few minutes to several
hours to download depending on your internet connection speed.

When the download is complete, you can run the training command again with `--source=$HOME/datasets/openwebtext.tar.xz`
to train from the downloaded file instead of streaming from the web.

> **TIP:** `AmaniGPT` trains directly from the compressed file. No need to extract anything. You can save the dataset to
any location you like and specify the path with the `--source` parameter.

# Inference

To generate text with the model you just trained above, run the following command:

```bash
amani generate-text --model-name=owt128 --max-tokens=64
```

This will start an interactive text generation session using the `owt128` model. You should see output similar to the
following:

```
Loading model from directory:

   /root/amanigpt/models/owt128

Model loaded successfully.

               Model ID: c167fab7-be7e-43b8-9b9b-a74b019ae98b
             Model Name: owt128
   Model Format Version: 1.0
    Context Window Size: 128 tokens
        Vocabulary Size: 15,483 tokens
          Feature Count: 1

You can now enter prompts to generate text. The model will generate up to 64 tokens.

NOTE: this is NOT a chatbot. Text is generated by repeatedly predicting the next token based on your prompt.

----- Enter prompt (type 'xxx' to exit) -----
```

Enter the prompt `He said it was a "tough decision" ` (notice the space at the end) and press `Enter`. You should see
output similar to the following (**lightly edited for readability in this guide**):

```
----- Enter prompt (type 'xxx' to exit) -----
He said it was a "tough decision"

----- Prediction Result -----
He said it was a "tough decision" but that he accepted the U.N. offer to evacuate after a Canadian medical team, also at
the hospital with Canadian security officers, left the site Friday afternoon. The Belgian team returned Saturday morning.

Gijs said the United Nations has agreed to provide security for Saturday night. The team has requested the Belgian
government to send

Prediction rate: 110 tokens/second
```

Enter `The delay postponed a definitive answer to ` (again, notice the space at the end) and press `Enter`:

```
----- Enter prompt (type 'xxx' to exit) -----
The delay postponed a definitive answer to

----- Prediction Result -----
The delay postponed a definitive answer to whether Clinton had made a clean sweep of five big primaries on Tuesday night.
Even if she does not prevail in Missouri, her other victories push her closer to the Democratic presidential nomination
even as the considerably weakened Sanders vowed to press on with his insurgent campaign.

Clinton won big in Florida, North Carolina and Ohio, while claiming

Prediction rate: 128 tokens/second
```

Enter `see the incredible energy of people who love ` and press `Enter`:
```
----- Enter prompt (type 'xxx' to exit) -----
see the incredible energy of people who love

----- Prediction Result -----
see the incredible energy of people who love this country but know we can do so much better," Sanders said to loud screams.

Some of his die-hard supporters expressed hope that he could still pull out the nomination.

"I still think the revolution is coming," said James Homan, 55, a sound engineer for rock musicians, who has homes in

Prediction rate: 137 tokens/second
```

Enter `You can't listen. It's not what you do. ` and press `Enter`:

```
----- Enter prompt (type 'xxx' to exit) -----
You can't listen. It's not what you do.

----- Prediction Result -----
You can't listen. It's not what you do. But the American people have been listening, and they do understand your policies.
And it's a new day in America.


Prediction rate: 152 tokens/second
```

These prompts are cherry-picked directly from the first few files out of the 100 text files that were processed during
training earlier above.

The model is able to **reconstruct long passages of coherent text from the training data WITHOUT storing the original
data**. The algorithm is fast and deterministic (i.e. `same prompt + same model = same output`).

> **FUN FACT:** you can pick any snippet of text from the generated text, enter it as a new prompt, and the model will
continue reconstructing text from that point onwards. If you increase the value of `--max-tokens`, the model can
reconstruct entire documents from the training data, effectively showing
[RAG-like capabilities](https://en.wikipedia.org/wiki/Retrieval-augmented_generation) without actually using RAG.

Since the data comes from Reddit, it is heavy on American news and politics, but the full dataset contains over 8 million
pages so you will find more variety if you train on more files. During training, you can use the `--exclude-words` parameter
to exclude files based on certain keywords (run `amani help --about=train-openwebtext | less` for more details).

# Limitations

We still need to improve the [tokenizer](https://en.wikipedia.org/wiki/Large_language_model#Tokenization). For example
if you enter `He said it was a "tough decision"!` (we just added an exclamation mark at the end of one of the successful
prompts), you get an error because the model doesn't recognize the resulting tokens:

```
----- Enter prompt (type 'xxx' to exit) -----
He said it was a "tough decision"!

Error: prompt contains out-of-vocabulary tokens. Try again with a different prompt.
```

It's easy to assume we are "cheating" by secretly storing the training data and printing it back out during inference,
but that's not the case. You can confirm this by making small changes to the prompt and observing how the model gets lost
and produces repetitive text (a classic failure mode for LLMs). For example, enter `He said it was a tough decision `
(we just removed the quotation marks around "tough decision"):

```
----- Enter prompt (type 'xxx' to exit) -----
He said it was a tough decision

----- Prediction Result -----
He said it was a tough decision to the the the the the the the the the the the the a , the the of the the the the the
the the the .  , the the the the

Prediction rate: 55 tokens/second
```

Another example can be seen by mixing snippets from the different examples shown earlier, to make a longer prompt like
`The delay to the incredible energy ` which combines `The delay ...` and `... the incredible energy ...`:

```
----- Enter prompt (type 'xxx' to exit) -----
The delay to the incredible energy

----- Prediction Result -----
The delay to the incredible energy of a who is this the a of the the the the the the the the said the the and to
. of his '-in the the the that

Prediction rate: 74 tokens/second
```

The model is trying to generalize based on its limited training data and producing valid tokens like `the` and `of`, and
even short coherent phrases like `of a`, `who is this`, `of the`, `said the`, `and to`, `of his` and `in the`. **Based
on these observations, we have reason to believe the quality of the generated text will improve significantly as we train
on more data and increase the context window size**.

**NOTE:** you can train with more files and a larger context window size right now, but due to limitations in the current
tokenizer, you will end up with a very large vocabulary size (e.g. we observed `400K` tokens after training on just `20K` 
files from the `OpenWebText` dataset). A larger vocabulary size results in a much larger model (tens of gigabytes with
hundreds of thousands of model files on disk) and we want to address this issue in the next preview release.

# Conclusion

In this guide, we installed and configured `AmaniGPT`, trained a small model from scratch using the `OpenWebText`
dataset, then used it to generate coherent text samples based on prompts. We also discussed some of the limitations
of the current version and the improvements we are working on for the next preview release. **Most importantly, we did
all of this on ordinary, inexpensive computer hardware available to anyone without writing a single line of code!**.

While it is still early days for `AmaniGPT`, we are excited about the possibility of making AI more sustainable and useful
for everyone. To ask questions, share feedback, or stay updated on new releases, send an email to `eric@amanigpt.com`.

Thanks for reading. Please help us spread the word about `AmaniGPT` :rocket:

PS: **if your organization is feeling the strain of AI-related costs** and you like what you see even at this early
stage, you should check out our [licensing guide](licensing-guide.md) so you can prepare to adopt `AmaniGPT` when it
becomes generally and commercially available (expected by `November 2026`).

