
# Overview

`AmaniGPT` is an experimental LLM architecture **designed to work efficiently on commodity CPU clusters in order to 
reduce the need for powerful but expensive GPUs**.

We took familiar transformer concepts (e.g. token embeddings, self-attention, etc) and reimagined them using CPU-only
algorithms and data structures.

This is the community repo where you can:
- Read the official guide on [quickly trying out AmaniGPT](owt-use.md) with a prebuilt model.
- Read the official guide on [training your own AmaniGPT model](owt-train.md) from scratch.
- Provide feedback and ask questions using [GitHub Issues](https://github.com/AmaniGPT/Community/issues).

# Benchmarks

While `AmaniGPT` is still experimental, the goal is to build a product that is worth using and paying for. To that end,
the only benchmarks we will discuss and optimize for are the following:

1. Does it work on your hardware?
1. Is it [fast enough](https://github.com/AmaniGPT/Community/issues/1) for your use case?
1. Does it produce accurate outputs without hallucinating?
1. Does it meet your compliance, privacy and security requirements?
1. Does it empower you to [do some truly legendary shit](https://www.youtube.com/watch?v=FyY0fEO5jVY&t=2611s)?

# Limitations

`AmaniGPT` is a tool. It is not alive, sentient, or conscious. It does not think, have an imagination, or want anything.

The hype around AI and the subsequent public backlash is based on treating AI tools as if they are human. They are not.

A calculator is not a mathematician. It is a tool that mathematicians can use for some tasks. `AmaniGPT` is the same.

We encourage people to use `AmaniGPT` where it makes sense and to do so while understanding that it has limitations.

Specifically, `AmaniGPT` models are only as good as their training data and will reflect the same inaccuracies, biases,
omissions, and inconsistencies present in that data. Always review model responses before using them for critical work.

# Releases

We plan to release one major version of `AmaniGPT` every year in November, with minor releases happening monthly until
the next major release. If you ask us for an ETA on a specific request, the answer will always be one of the following:

- **Minor requests:** "at the end of this or next month".
- **Major requests:** "at the end of this or next year".

This approach allows us to build high-quality software and deliver it on a predictable schedule for everyone. If you
have a specific deadline, please get in touch with your account manager to get a quote (this option is only available
for Enterprise and Sovereign Edition license holders).

# Licensing

`AmaniGPT` is currently (as of `April 2026`) in preview and can be used for non-production evaluation purposes only.
When it becomes generally available (expected by `November 2026`), it will be offered under the following editions:

- **Community Edition**: free for commercial and non-commercial use on up to 100 CPU cores.
- **Enterprise Edition**: paid for use on more than 100 CPU cores. Includes priority support and maintenance.
- **Sovereign Edition**: paid for use on unlimited CPU cores. Includes priority support and maintenance.

**NOTE:** the above is provided for informational purposes only and is subject to change without notice. For licensing
and pre-order inquiries, please see the contact section below.

# Partnerships

`AmaniGPT` allows you to build and use AI models which solve problems that matter to you. We personally care about the
following areas:

- Developer tools & IDEs.
- Mobile & desktop operating systems.
- Browsers & productivity apps.

If your company (1) offers a product in any of the areas listed above, (2) has pre-ordered an Enterprise or Sovereign 
Edition license, and (3) is building something we already use ourselves, then we would especially love to partner with
you! You will receive our full support and close collaboration, since your success directly benefits our own work and
the broader community.

# Roadmap

`AmaniGPT` is part of our vision to **make AI more accessible and useful** over the next 10 years in multiple phases:

- **Phase 0 (Preview)**: we are here now. The goal is to finalize and validate CPU-only LLMs as a more reliable and 
  sustainable alternative to GPU-based LLMs.

- **Phase 1 (General Availability)**: expected by `November 2026`. `AmaniGPT` should be generally available and offer
  **fast, offline, unlimited, privacy-preserving training and inference on commodity CPU clusters**. At this point, the
  marginal cost of both training and inference should be close to zero, and that's when everything changes!

- **Phase 2 (Agents Reboot)**: expected by `2027-2028`. With the cost of training and inference close to zero, the
  cost of experimentation and failure also approaches zero. This should unlock new possibilities through agents that
  work together in parallel to explore thousands of possible solutions to a problem without costs spiraling out of
  control.

- **Phase 3 (Symbiotes)**: expected by `2028-2030`. With the cost of training and inference close to zero, we can build
  hyper-personalized agents (called symbiotes) that are paired with individuals for life, continuously learning and
  evolving with them. If you are a professional surgeon, engineer, architect, etc, your symbiote learns from you until
  it becomes a professional in the same field and can assist you in your life's work.

- **Phase 4 (Embodied Symbiotes)**: expected by `2030-2036`. To cover the full spectrum of human knowledge and skills,
  symbiotes will gain physical embodiments outside phones and computers, such as humanoid robots, self-driving cars,
  drones, submarines, etc. Your embodied symbiote allows you to be in multiple places at once and carry out physical
  tasks (e.g. a mechanic symbiote can repair multiple cars at the same time under the supervision of its human partner).

Some of the features needed to achieve the above vision already exist in `AmaniGPT` today (e.g. it is multimodal which
should be useful when building symbiotes that can see, hear, speak, and move). The mission over the next 10 years is
to validate the architecture, optimize it for speed and reliability, and build an accessible ecosystem so everyone can
contribute. Get in touch if you want to be part of our Early Adopter Program and help us build AI that makes daily life
better in ways that matter to you!

# Acknowledgements

- Thanks to Aaron Gokaslan, Vanya Cohen, Ellie Pavlick and Stefanie Tellex at Brown University for putting together the
[OpenWebText](https://zenodo.org/records/3834942) dataset and to [Zenodo](https://zenodo.org/) for hosting it. This
dataset is used to train `AmaniGPT` models for research and demonstration purposes.

- Thanks to the [SharpCompress](https://github.com/adamhathcock/sharpcompress) project which allows `AmaniGPT` to process
the XZ compression format used by the OpenWebText dataset.

- Thanks to the [C#](https://github.com/dotnet/csharplang) and [dotnet](https://github.com/dotnet/runtime) teams for
providing free, open-source programming tools and libraries that make it possible to build high-performance CPU-only
LLMs like `AmaniGPT`.

- Thanks to the mysterious team behind the legendary [Visual Studio](https://learn.microsoft.com/visualstudio/debugger/)
debugger which makes it possible to "look into the mind" of an `AmaniGPT` model with millions of parameters and make sense
of how it predicts the next token during inference.

**NOTE:** `AmaniGPT` is an independent project and is NOT officially affiliated with or endorsed by the above individuals,
teams, and organizations. All trademarks and names are the property of their respective owners.

# Contact

For licensing, media and other inquiries, please contact: **eric.mutta@gmail.com**

