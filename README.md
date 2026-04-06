
# Overview

`AmaniGPT` is an experimental LLM architecture **designed to work efficiently on commodity CPU clusters in order to 
reduce the need for powerful but expensive GPUs**. It takes familiar transformer concepts (token embeddings, self 
attention, positional encoding, nonlinear activations) and reimagines them using CPU-friendly algorithms and data
structures.

This is the community repo where you can:
- File bug reports, make feature requests, and ask questions.
- Read our handy guides on [using](use-model.md) and [training](train-model.md) your own `AmaniGPT` models.

# Licensing

`AmaniGPT` is currently (as of `April 2026`) in preview and can be used for non-production evaluation purposes only.
When it becomes generally available (expected by `November 2026`), it will be offered under the following editions:

- **Community Edition**: free for commercial and non-commercial use on up to `XXX` CPU cores.
- **Enterprise Edition**: paid for use on more than `XXX` CPU cores. Includes priority support and maintenance.
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

`AmaniGPT` is part of a broader vision to democratize AI and transform society over the next 10 years in multiple phases:

- **Phase 0 (Preview)**: we are here now. The goal is to finalize and validate CPU-only LLMs as a more reliable and 
  sustainable alternative to GPU-based LLMs.

- **Phase 1 (General Availability)**: expected by `November 2026`. `AmaniGPT` should be generally available and offer
  fast, offline, unlimited, privacy-preserving training and inference on commodity CPU clusters. At this point, the
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
should be useful when building symbiotes that can see, hear, speak, and move). The main task over the next 10 years is
to validate the architecture, optimize it for speed and reliability, and build an accessible ecosystem so others can
contribute. Get in touch if you want to be part of our Early Adopter Program and help us build AI that makes everyday
life better in meaningful ways!

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

