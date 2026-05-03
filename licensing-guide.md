
# Read This First

We are an engineering-led company which means `AmaniGPT` is bought not sold:

1. We don't have a sales team.
1. We don't do sales calls.
1. We don't play pricing games.
1. **We are email-first people.**

All `AmaniGPT` licenses offer the following guarantees across all editions:

1. **No metering**: usage is not tracked or billed based on consumption.
1. **No telemetry**: `AmaniGPT` does not transmit usage or system data.
1. **No revenue sharing**: you retain 100% of your revenue from applications built with `AmaniGPT`.
1. **No ownership claim**: you retain full ownership of all models and outputs you create using `AmaniGPT`.
1. **No activation**: `AmaniGPT` installs and runs fully offline with no "phone home" requirements.
1. **No audits**: we do not perform routine audits or licensing compliance inspections.

If that resonates with you and you are **feeling the strain of AI-related capital and operational expenditures**, then
we'd love to work with you!

Make sure you have reviewed our [README](README.md) to understand what `AmaniGPT` is and why it can save you money.

Review the rest of this licensing guide so you can **make a purchasing decision at your own pace**. 

When you are satisfied that `AmaniGPT` is a good fit and are ready to start the purchasing process, please get in touch
via: `start@amanigpt.com`

**IMPORTANT**: this guide is provided for **informational purposes only**. Final license terms will be discussed during
the purchasing process which we always aim to **complete within 30 days or less from first contact.**

# Licensing At A Glance

`AmaniGPT` gives you control over the rising and unsustainable costs of AI. It is licensed based on current AI spend:

| AI Spend (USD)   | Best Edition | Price (USD)    | Max CPU Cores | Max Tokens | Source Code Access |
| -----------------| ------------ | ---------------| ------------- | ---------- | ------------------ |
| Up to $200/month | Community    | Free           | 32            | Unlimited  | No                 |
| Up to $10M/year  | Enterprise   | $1M lifetime   | 128+          | Unlimited  | No                 |
| Up to $200B/year | Hyperscale   | $100M lifetime | Unlimited     | Unlimited  | No                 |
| Up to $200B/year | Sovereign    | $500M lifetime | Unlimited     | Unlimited  | Yes                |

**NOTES:**
- **`AmaniGPT` runs on your own hardware using standard CPUs so there are no token limits.**
- Multiple Enterprise licenses can be purchased as needed, each granting another 128 CPU cores.
- Best-effort support is provided free for the Community Edition using public channels and documentation.
- Private and dedicated support is available for the paid editions at 10% of the license fee per year.
- Customers can pre-order Enterprise, Hyperscale, or Sovereign licenses by paying 10% of the license fee.
- The Sovereign Edition **TCO is $1B over 10 years** with source code, dedicated support, and unlimited compute.

# AmaniGPT Licensing Guide

## Overview

`AmaniGPT` is an AI engine which allows training and inference on commodity CPU clusters. It is offered in four editions:

1. Community Edition.
1. Enterprise Edition.
1. Hyperscale Edition.
1. Sovereign Edition.

All editions provide access to the same basic functionality. The difference is in the maximum amount of CPU cores that
can be used, the level of support provided, and availability of source code.

---

## Definitions

1. **Software** means all standalone (EXE) and in-process (DLL) binaries, along with any official documentation, SDKs,
and related materials provided to the licensee as part of `AmaniGPT`.

1. **Organization** means any legal entity, person, or team of individuals that uses the Software. It includes but is not
limited to businesses, academic institutions, government agencies, non-profits, individual developers, and hobbyists.

1. **Application** means any product, service, system, or project that incorporates or depends on the Software for AI
training, inference, or related purposes. This applies regardless of whether the Application is developed internally
by the Organization, obtained from a third party, or made available to third parties commercially or non-commercially.

1. **Controlled Compute** means any computing resources where an Organization can install and run Applications. This
includes servers, desktops, mobile devices, network devices, virtual machines, containers or similar resources. Control
applies regardless of whether the resources are made, owned, bought, sold, leased, rented by, to or from the Organization
and is aggregated across all environments and affiliated entities under common ownership or control of the Organization.

1. **CPU Core** means a physical or virtual processing unit capable of independently executing Applications. CPU core
count is determined as the maximum value reported by the runtime environment (e.g. `Environment.ProcessorCount` in .NET)
on all systems where the Software is installed or stored (even if not actively executing).

1. **General Availability (GA)** means the date when the Software is officially released and made available for download
and purchase by the general public. The expected GA date is `November 2026` but is subject to change based on
development progress and market conditions.

---

## Licensing Responsibility

Each Organization is independently responsible for obtaining a license based on its own use of the Software.

An Organization must have an appropriate paid license if it develops and or operates any Application on Controlled
Compute exceeding the limits of the Community Edition, regardless of whether:

- The Application was developed internally.
- The Application was obtained from a third party.
- The Application is used for internal purposes.
- The Application is provided as a product or service to third parties.

Example scenarios:

| Scenario       | Developer creates Application on | User runs Application on | Who needs a paid license |
|----------------|----------------------------------|--------------------------|--------------------------|
| Small To Big   | A laptop (8 cores)               | More than 32 cores       | Only the user            |
| Big To Small   | A 500-core cluster               | A laptop/phone (8 cores) | Only the developer       |
| Big To Big     | A 500-core cluster               | A 500-core cluster       | Both developer and user  |
| Small To Small | A laptop (8 cores)               | A laptop/phone (8 cores) | Neither (free for both)  |

**NOTE:** the words **Developer** and **User** are for illustration and fall under the definition of **Organization**.

---

## Editions

### Community Edition

The Community Edition is available free of charge. The target audience includes but is not limited to:

- Individual developers.
- Academic research.
- Startups and small Organizations.
- Evaluation and experimentation.

The Community Edition permits operation of the Software on up to **32 CPU cores of Controlled Compute.**

For context, 32 CPU cores can be achieved with:

- A team of 4 developers using laptops with 8 cores each.
- A cluster of 8 medium VM instances in the cloud with 4 cores each.
- A cluster of 16 small VM instances in the cloud with 2 cores each.

An Organization that operates the Software on more than 32 CPU cores of Controlled Compute must obtain a paid license.

---

### Enterprise Edition

The Enterprise Edition requires a paid license. The target audience is Organizations that:

- Want to deploy at a significant scale exceeding Community Edition limits.
- Require commercial support and on-going maintenance for smooth production use.
- Have **compliance, privacy, and security requirements** that demand customized on-premises AI models.

The Enterprise Edition permits operation of the Software on up to **128 CPU cores of Controlled Compute.**

For context, 128 CPU cores can be achieved with:

- A team of 16 developers using laptops with 8 cores each.
- A single high-end server (e.g. an AMD EPYC 9654 CPU with 96 cores).
- A cluster of 32 medium VM instances in the cloud with 4 cores each.
- A cluster of 64 small VM instances in the cloud with 2 cores each.

The Enterprise Edition is offered for a **one-time license fee of USD $1M (one million USD).**

Annual maintenance and support is available at **10% of the license fee per year (i.e. $100K/year).**

---

### Hyperscale Edition

The Hyperscale Edition requires a paid license. The target audience includes but is not limited to:

- Organizations that want to integrate unlimited AI into **hyperscale online services** that run on millions of CPU cores.
- Organizations that want to integrate unlimited AI into **hardware ecosystems with millions to billions of CPU cores**.

The Hyperscale Edition permits operation of the Software on **Unlimited Controlled Compute.**

The Hyperscale Edition is offered for a **one-time license fee of USD $100M (one hundred million USD).**

Annual maintenance and support is available at **10% of the license fee per year (i.e. $10M/year).**

The Hyperscale Edition allows Organizations to:

1. **Eliminate up to 99% of current AI-related costs** by using commodity CPU clusters.
1. **Restore shareholder confidence** through improved cash flow and profitability.
1. **Rebuild employee morale** through cost-effective AI that empowers rather than replaces them.
1. **Expand market leadership** through new products and services powered by unlimited AI.

---

### Sovereign Edition

The Sovereign Edition requires a paid license. The target audience includes but is not limited to:

- National and governmental institutions requiring **full autonomy, privacy and control** over their AI infrastructure.
- Organizations that want deep **integration into mission-critical products and services** with reduced vendor dependencies.
- Organizations with **non-negotiable security and safety requirements** where source access allows auditing and verification.

The Sovereign Edition **includes source code access** under the following terms:

1. Source code is provided **strictly for internal use** and cannot be sublicensed, leased, sold or redistributed.
1. Source code is **only provided for the in-process library (DLL)** which is the core component of the Software.
1. Source code is **NOT transferable under any circumstances**. Changes in control require acquisition of a new license.
1. Licensees must **designate 3 to 5 named personnel** who will receive training to ensure business process continuity.
1. Licensees will receive **quarterly snapshots of the source code** and are responsible for merging updates as needed.
1. Licensees will receive the **first source code snapshot upon GA** and after full payment of the license fee.
1. Licensees have **perpetual rights to source snapshots**. New snapshots require annual maintenance and support payments.
1. Licensees are permitted to **port the source code to other programming languages** already used by their core offerings.
1. Licensees are permitted to **develop hardware accelerators** under separate terms that will be negotiated as needed.
1. Licensees are **NOT permitted to use the source code to build competing products or services** for use by third parties.

The Sovereign Edition permits operation of the Software on **Unlimited Controlled Compute.**

The Sovereign Edition is offered for a **one-time license fee of USD $500M (five hundred million USD).**

Annual maintenance and support is available at **10% of the license fee per year (i.e. $50M/year).**

**IMPORTANT:** due to the sensitive nature of source code access and the long-term strategic relationship required for
the Sovereign Edition, **the number of licenses issued will be limited and granted on a case-by-case basis**. There are
no eligibility requirements for the Hyperscale Edition beyond the ability to pay the license and maintenance fees, so
most Organizations can still enjoy the benefits of unlimited AI even if they do not qualify for the Sovereign Edition.

---

## Common Terms & Conditions

1. All fees are final, non-refundable, and subject to applicable sales and other taxes.
1. The Software provides significant cost savings compared to GPU-based alternatives. Further discounts are not available.
1. The Software cannot be sublicensed, leased, sold, or redistributed except as part of a larger Application.
1. The one-time license fee is payable in full within 30 days of contract signing.
1. Multiple Enterprise licenses can be purchased as needed, each granting another 128 CPU cores of Controlled Compute.
1. There is no need for multiple licenses under editions that permit unlimited Controlled Compute.
1. The license is perpetual, non-exclusive, non-transferable and royalty-free, subject to the terms of this agreement.
1. The license conveys no equity, acquisition, IP transfer, governance/information rights or employment arrangements.
1. The license is immediately suspended if licensee initiates legal action and remains suspended until case resolution.
1. Licensee must commit to protecting the dignity and value of human life when building advanced AI using the Software.
1. Issued licenses are irrevocable, but ongoing maintenance and support is conditional on compliance with the license.
1. Using any edition of the Software beyond its limits is a violation of your license and may result in legal action.

## Pre-ordering Terms & Conditions

1. Prior to GA, customers can pre-order Enterprise, Hyperscale, or Sovereign licenses by paying 10% of the license fee.
1. Pre-ordering guarantees access to the respective license post-GA at the currently stated terms and price.
1. Pre-ordering is safe even if GA is delayed since licenses are perpetual and post-paid support only starts after GA.
1. The pre-order fee is non-refundable but will be credited towards the full license fee for up to 30 days after GA.

## Maintenance Terms & Conditions

Community Edition:

1. Best-effort maintenance and support is provided free through public channels and documentation.
1. Bug fixes and updates are provided for the latest major version of the Software only.
1. More comprehensive maintenance and support is available for Organizations that obtain a paid license.

Enterprise, Hyperscale, and Sovereign Editions:

1. Maintenance fees are post-paid annually from the effective start date of the license.
1. If you purchase multiple Enterprise licenses, the annual maintenance fee is 10% of the total license fees to date.
1. Maintenance and support is provided for 3 of the most recent major versions of the Software.
1. Private channels for dedicated technical support are available for issues related to the Software.
1. Private guidance on integration and deployment best practices is provided to ensure successful adoption.
1. Guaranteed response times for production issues caused directly by the Software are provided:
   - Enterprise Edition: same day response time.
   - Hyperscale Edition: 1 hour response time.
   - Sovereign Edition: 30 minute response time.
1. Maintenance and support requires a minimum commitment with autorenewal unless cancelled 3 months prior:
   - Enterprise Edition: 3 year commitment (i.e. $300K total over 3 years).
   - Hyperscale Edition: 5 year commitment (i.e. $50M total over 5 years).
   - Sovereign Edition: 10 year commitment (i.e. $500M total over 10 years).
1. Maintenance and support does not cover issues caused by modifications to the source code for the Sovereign Edition.
1. If payment lapses for more than 6 months, a new license must be purchased at the current price to resume support.

## Feedback

We want to offer **the most refreshing licensing experience in the industry** and welcome your feedback so we can continue
to improve this guide as we approach general availability (GA). Please email any suggestions and questions you may have
to: `licensing@amanigpt.com`

