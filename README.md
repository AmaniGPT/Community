
# Overview

`AmaniGPT` is an **experimental AI engine designed to work efficiently on commodity CPU clusters in order to reduce the
need for powerful but expensive GPUs**.

We took familiar transformer concepts (e.g. token embeddings and self-attention) and reimagined them using CPU-only
algorithms and data structures. The result is an AI engine that:

1. **Generates answers instantly** so you never have to wait.
1. **Runs offline** in situations where internet connections are not available or allowed.
1. **Supports personalization** by allowing you to train existing models on your own code and data.
1. **Protects your privacy** by keeping all code, data, and conversations on your devices or network.
1. **Gives you complete control** by allowing you to build your own models using your own rules and data.
1. **Maximizes your productivity** by removing token limits since everything runs on your own hardware.
1. **Dramatically reduces costs** by doing all of the above on commodity CPUs that you already use today.

This is the community repo where you can:

1. Read the official guide on [quickly trying out AmaniGPT](owt-use.md) with a prebuilt model.
1. Read the official guide on [training your own AmaniGPT model](owt-train.md) from scratch.
1. Provide feedback and ask questions using [GitHub Issues](https://github.com/AmaniGPT/Community/issues).

# Benchmarks

While `AmaniGPT` is still experimental, the goal is to build a product that is worth using and paying for. To that end,
the only benchmarks we will discuss and optimize for are the following:

1. Does it work on your hardware?
1. Is it [fast enough](https://github.com/AmaniGPT/Community/issues/1) for your use case?
1. Does it produce accurate outputs without hallucinating?
1. Does it meet your **compliance, privacy and security requirements**?
1. Does it allow you to [do legendary shit](https://www.youtube.com/watch?v=FyY0fEO5jVY&t=2611s)?

# Limitations

`AmaniGPT` is a tool. It is not alive, sentient, or conscious. It does not feel, have an imagination, or want anything.

The hype around AI and the subsequent public backlash is based on treating AI tools as if they are human. They are not.

A calculator is not a mathematician. It is a tool that mathematicians can use for some tasks. `AmaniGPT` is the same.

We encourage people to use `AmaniGPT` where it makes sense and to do so while understanding that it has limitations.

Specifically, `AmaniGPT` **models are only as good as their training data** and will reflect the same inaccuracies,
biases, omissions, and inconsistencies present in that data. Always review model responses before using them for 
critical work.

# Releases

We plan to release one major version of `AmaniGPT` every year in November, with minor releases happening monthly until
the next major release. If you ask us for an ETA on a specific request, the answer will always be one of the following:

- **Minor requests:** "at the end of this or next month".
- **Major requests:** "at the end of this or next year".

This approach allows us to build high-quality software and deliver it on a predictable schedule for everyone. If you
have a specific deadline, please get in touch with our team to share your requirements and get a quote (this option is
only available for Enterprise and Sovereign Edition license holders).

# Licensing

`AmaniGPT` is currently (as of `April 2026`) in preview and **can be used for non-production evaluation purposes only**.
When it becomes generally available (expected by `November 2026`), it will be offered under the following editions:

- **Community Edition**: free for commercial and non-commercial use on up to `100 CPU cores`.
- **Enterprise Edition**: paid for use on more than `100 CPU cores`. Includes priority support and maintenance.
- **Sovereign Edition**: paid for use on unlimited CPU cores. Includes priority support and maintenance.

**NOTE:** the above is provided for informational purposes only and is subject to change without notice.

# Pre-orders

If your organization is feeling the strain of AI-related capital and operational expenditures, `AmaniGPT` can help. By
pre-ordering an Enterprise or Sovereign Edition license, you gain access to fast, private, unlimited AI on hardware you
already own, along with the following benefits:

1. **Lock in preferential pricing** before general availability in `November 2026`.
1. **Secure a perpetual license** to use `AmaniGPT` technology, regardless of any future exclusivity arrangements.
1. **Influence the roadmap** by working directly with our team to prioritize features relevant to your core needs.
1. **Ensure successful adoption** by evaluating `AmaniGPT` with the help of our team before you make a full commitment.

For more information, please contact: **eric@amanigpt.com**

# Partnerships

`AmaniGPT` allows you to build and use AI models which solve problems that matter to you. We personally care about the
following areas:

1. Developer tools & IDEs.
1. Mobile & desktop operating systems.
1. Browsers & productivity apps.

We would especially love to partner with your organization if:

1. You offer a product in any of the areas listed above.
1. You have pre-ordered an Enterprise or Sovereign Edition license.
1. You are building products we already use ourselves.

As a qualified partner, **you will receive our full support and close collaboration**, since your success directly
benefits our own work and the broader community.

# Roadmap

`AmaniGPT` is part of our vision to **make AI more accessible and useful** over the next 10 years, in multiple phases:

- **Phase 0 (Preview)**: we are here now. The goal is to finalize and validate CPU-only AI as a more reliable and
  sustainable alternative to GPU-heavy AI.

- **Phase 1 (General Availability)**: expected by `November 2026`. `AmaniGPT` should offer **fast, offline, unlimited,
  private AI on commodity hardware**. The marginal cost of training and inference should be close to zero. Intelligence
  can be everywhere at once. **Everything can _think_: from houses to cities, cars to planes, farms to factories,
  businesses to entire markets**. Everything is your agent. Everything works for you.

- **Phase 2 (Agents Reboot)**: expected by `2027-2028`. Agents have struggled in the past because failure is expensive.
  However, **when the cost of inference is close to zero, the cost of experimentation and failure also becomes zero**.
  Agents can start working together in parallel to explore hundreds of possible solutions to a problem without costs
  spiraling out of control.

- **Phase 3 (Symbiotes)**: expected by `2028-2030`. With the cost of training and inference close to zero, we can build
  hyper-personalized agents (called symbiotes) that are paired with individuals for life, **continuously learning** and
  evolving with them. If you are a professional (e.g. a surgeon, engineer or architect), your symbiote learns from you
  until it becomes a professional in the same field and can assist you in your life's work.

- **Phase 4 (Embodied Symbiotes)**: expected by `2030-2036`. To cover the full spectrum of human knowledge and skills,
  symbiotes will gain physical embodiments outside phones and computers, such as humanoid robots, self-driving cars,
  drones, submarines, etc. **Your embodied symbiote allows you to be in multiple places at once** and carry out physical
  tasks (e.g. a mechanic symbiote can repair multiple cars at the same time under the supervision of its human partner).

Some of the features required to achieve the above vision already exist in prototype form within `AmaniGPT` today (e.g.
it is natively multimodal which should be useful when building symbiotes that can see, hear, speak, and move).

The mission over the next 10 years is to **validate** the architecture, **optimize** it for speed and reliability, and
**build an accessible ecosystem** so everyone can contribute. We welcome you to join us on this ambitious journey and
help us build AI that makes our daily lives more productive, enjoyable, and meaningful.

# Acknowledgements

- Thanks to Aaron Gokaslan, Vanya Cohen, Ellie Pavlick and Stefanie Tellex at Brown University for putting together the
[OpenWebText](https://zenodo.org/records/3834942) dataset and to [Zenodo](https://zenodo.org/) for hosting it. This
dataset is used to train `AmaniGPT` models for research and demonstration purposes.

- Thanks to the [SharpCompress](https://github.com/adamhathcock/sharpcompress) project which allows `AmaniGPT` to process
the XZ compression format used by the OpenWebText dataset.

- Thanks to the [C#](https://github.com/dotnet/csharplang) and [dotnet](https://github.com/dotnet/runtime) teams for
providing free, open-source **programming tools and libraries that make it possible to build high-performance CPU-only
AI engines** like `AmaniGPT`.

- Thanks to the mysterious team behind the legendary [Visual Studio](https://learn.microsoft.com/visualstudio/debugger/)
debugger which makes it possible to "look into the mind" of an `AmaniGPT` model with millions of parameters and make sense
of how it predicts the next token during inference.

**NOTE:** `AmaniGPT` is an independent project and is NOT officially affiliated with or endorsed by the above individuals,
teams, and organizations. All trademarks and names are the property of their respective owners.

# Contact

Eric Mutta (the creator of `AmaniGPT`) is a tech entrepreneur and software engineer with 27 years of experience. He
has a passion for tackling seemingly impossible problems and is assembling a team to prepare `AmaniGPT` for general
availability by `November 2026`.

For media, licensing, and pre-order inquiries, please contact: **eric@amanigpt.com**

