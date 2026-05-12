
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

When you are satisfied that `AmaniGPT` is a good fit and are ready to start the [purchasing process](#purchasing-process),
please get in touch via: `start@amanigpt.com`

**IMPORTANT**: this guide is provided for **informational purposes only**. Final license terms will be discussed during
the [purchasing process](#purchasing-process).

# Licensing At A Glance

`AmaniGPT` gives you control over the rising and unsustainable costs of AI. It is licensed based on current AI spend:

| AI Spend (USD)   | Best Edition | Price (USD)    | Max CPU Cores | Max Tokens | Source Code Access |
| -----------------| ------------ | ---------------| ------------- | ---------- | ------------------ |
| Up to $200/month | Community    | Free           | 32            | Unlimited  | No                 |
| Up to $10M/year  | Enterprise   | $1M lifetime   | 128+          | Unlimited  | No                 |
| Up to $50B/year  | Hyperscale   | $100M lifetime | Unlimited     | Unlimited  | No                 |
| Up to $200B/year | Sovereign    | $500M lifetime | Unlimited     | Unlimited  | Yes                |

**NOTES:**
- **`AmaniGPT` runs on your own hardware using ordinary CPUs so there are no token limits.**
- Multiple Enterprise licenses can be purchased as needed, each granting another 128 CPU cores.
- Best-effort support is provided free for the Community Edition using public channels and documentation.
- Private and dedicated support is available for the paid editions at 10% of the license fee per year.
- Customers can pre-order Enterprise, Hyperscale, or Sovereign licenses by paying 10% of the license fee.
- **The Sovereign Edition TCO is $1B over 10 years offering source code, dedicated support, and unlimited compute.**

# Purchasing Process

The `AmaniGPT` purchasing process is designed with two goals in mind:

1. **Transparency**: everything you need to know is out in the open. No hidden fees, no fine print, no nasty surprises.
1. **Speed**: the entire process, from first contact to signed contract, **should be complete in 30 days or less**.

The process works in two phases:

1. **Evaluation:** this is fully self-service and self-paced. No sales calls, no demos, no meetings.
1. **Adoption:** this is collaborative, done mostly via email, and involves just two scheduled calls.

**TIP:** the Community Edition does not require following the purchasing process since it is free. Just download and
[start using it](owt-use.md)!

**Phase 1: Evaluation**

1. **Understand the product, benefits, and roadmap** by reviewing our [README](README.md).
1. **Understand the licensing model and terms** by reviewing this [licensing guide](#amanigpt-licensing-guide).
1. **Request clarification or more information** by sending an email to `licensing@amanigpt.com`.
1. **Appoint an internal sponsor** to "run everything up the chain" and obtain preliminary purchase approval.
1. **Start the purchasing process** by sending an email to `start@amanigpt.com` if you are the internal sponsor.

The email you send as the internal sponsor should contain the following information:

1. Confirmation that all of the above steps have been completed.
1. Confirmation that preliminary purchase approval has been obtained.
1. The edition you intend to purchase (Enterprise, Hyperscale, or Sovereign).
1. Any special conditions or requirements for getting full purchase approval.
1. An estimate of the expected internal timeline for completing the process.

**Phase 2: Adoption**

1. **Breaking the ice:** we will schedule a short, friendly, non-technical call to put a face to each email address :smile:
1. **Finalize contract:** using this guide as a baseline, we will work with legal to draft the final license agreement.
1. **Sign contract:** we will schedule a final call to review and sign the contract with key stakeholders in attendance.
1. **Pay pre-order fee:** we will send an invoice for the pre-order fee as agreed, so finance can process the payment.
1. **Prepare for GA:** we will work with your teams to prioritize pre-agreed features as we finalize `AmaniGPT` for GA.
1. **Transition to GA:** once `AmaniGPT` is generally available, we will start the maintenance and support relationship.

**TIP:** the purchasing process is less about software and more about philosophical fit. If your organization values
minimalism, attention to detail, and a no-nonsense approach to business, then **we are going to do legendary things
together :muscle:**

# AmaniGPT Licensing Guide

## Overview

`AmaniGPT` is an AI engine which allows training and inference on ordinary CPUs. It is offered in four editions:

1. [Community Edition](#community-edition)
1. [Enterprise Edition](#enterprise-edition)
1. [Hyperscale Edition](#hyperscale-edition)
1. [Sovereign Edition](#sovereign-edition)

All editions provide access to the same basic functionality. The difference is in the maximum amount of CPU cores that
can be used, the level of support provided, and availability of source code.

---

## Definitions

1. **Software** means all standalone (EXE) and in-process (DLL) binaries, along with any official documentation, SDKs,
and related materials provided to the licensee as part of `AmaniGPT`. Source code used to build the Software does NOT
form part of the Software and is governed by the `Source Access Terms & Conditions` section of this guide.

1. **Organization** means any legal entity, person, or team of individuals that uses the Software. It includes but is not
limited to businesses, academic institutions, government agencies, non-profits, individual developers, and hobbyists.

1. **Application** means any product, service, system, or project that incorporates or depends on the Software for AI
training, inference, or related purposes. This applies regardless of whether the Application is developed internally
by the Organization, obtained from a third party, or made available to third parties commercially or non-commercially.

1. **Controlled Compute** means any computing resources where an Organization can install and run Applications. This
includes servers, desktops, mobile devices, gaming consoles, IoT devices, network devices, virtual machines, containers,
or similar resources. Control is determined solely by the "install and run" test, so it applies to any resource regardless
of ownership, access method, deployment environment, financial considerations, geographic location, or corporate structure.

1. **CPU Core** means a physical or virtual processing unit capable of independently executing Applications. CPU core
count is determined as the maximum value reported by the runtime environment (e.g. `Environment.ProcessorCount` in .NET)
on all systems where the Software is installed or stored (even if not actively executing).

1. **General Availability (GA)** means the date when the Software is officially released and made available for download
and purchase by the general public. The expected GA date is `November 2026` but is subject to change based on
development progress and market conditions.

**NOTE:** plural forms of the above terms (e.g. "Organizations", "Applications", "CPU Cores") shall retain the same
meaning as their singular forms for the purposes of this licensing guide.

---

## Licensing Responsibility

Each Organization is independently responsible for obtaining an appropriate paid license if it develops and or operates
any Application on Controlled Compute exceeding the limits of the Community Edition. Example scenarios:

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

The Community Edition permits development and operation of Applications on up to **32 CPU cores of Controlled Compute.**

For context, 32 CPU cores can be achieved with:

- A team of 4 developers using laptops with 8 cores each.
- A cluster of 8 medium VM instances in the cloud with 4 cores each.
- A cluster of 16 small VM instances in the cloud with 2 cores each.

An Organization that develops or operates Applications on more than 32 CPU cores of Controlled Compute must obtain a
paid license.

---

### Enterprise Edition

The Enterprise Edition requires a paid license. The target audience is Organizations that:

- Want to deploy at a significant scale exceeding Community Edition limits.
- Require commercial support and on-going maintenance for smooth production use.
- Have **compliance, privacy, and security requirements** that demand customized on-premises AI models.

The Enterprise Edition permits development and operation of Applications on up to **128 CPU cores of Controlled Compute.**

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

The Hyperscale Edition permits development and operation of Applications on **Unlimited Controlled Compute.**

The Hyperscale Edition is offered for a **one-time license fee of USD $100M (one hundred million USD).**

Annual maintenance and support is available at **10% of the license fee per year (i.e. $10M/year).**

The Hyperscale Edition allows Organizations to:

1. **Eliminate up to 99% of current AI-related costs** by using ordinary CPU clusters.
1. **Restore shareholder confidence** through improved cash flow and profitability.
1. **Rebuild employee morale** through cost-effective AI that empowers rather than replaces them.
1. **Expand market leadership** through new products and services powered by unlimited AI.

---

### Sovereign Edition

The Sovereign Edition requires a paid license. The target audience includes but is not limited to:

- National and governmental institutions requiring **full autonomy, privacy and control** over their AI infrastructure.
- Organizations that want deep **integration into mission-critical products and services** with reduced vendor dependencies.
- Organizations with **non-negotiable security and safety requirements** where source access allows auditing and verification.
- Organizations that need source access to build **hardware accelerators** for [Embodied Symbiotes](README.md#roadmap).

The Sovereign Edition **includes source code access** as described in the `Source Access Terms & Conditions` section.

The Sovereign Edition permits development and operation of Applications on **Unlimited Controlled Compute.**

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
1. The license requires a written commitment to [protecting the dignity and value of human life](#human-dignity) when using the Software.
1. Using any edition of the Software beyond its limits is a violation of your license and may result in legal action.

## Pre-ordering Terms & Conditions

1. Prior to GA, Organizations can pre-order licenses for paid editions by paying 10% of the respective license fee.
1. Pre-ordering guarantees access to the respective license post-GA at the currently stated terms and price.
1. Pre-ordering is safe even if GA is delayed since licenses are perpetual and post-paid support only starts after GA.
1. The pre-order fee is non-refundable but will be credited towards the full license fee for up to 30 days after GA.
1. Upon GA, pre-order customers are expected but not required to pay the remaining license fee and obtain their license.

## Maintenance Terms & Conditions

Community Edition:

1. Best-effort maintenance and support is provided free through public channels and documentation.
1. Bug fixes and updates are provided for the latest major version of the Software only.
1. More comprehensive maintenance and support is available for Organizations that obtain a paid license.

Enterprise, Hyperscale, and Sovereign Editions:

1. Maintenance fees are post-paid annually from the effective start date of the license.
1. If you purchase multiple Enterprise licenses, the annual maintenance fee is 10% of the total license fees paid to date.
1. Maintenance and support is provided for 3 of the most recent major versions of the Software.
1. Private channels for dedicated technical support are available for issues related to the Software.
1. Private guidance on integration and deployment best practices is provided to ensure successful adoption.
1. Guaranteed response times for production issues caused directly by the Software are provided:
   - Enterprise Edition: **same day response time**.
   - Hyperscale Edition: **1 hour response time**.
   - Sovereign Edition: **30 minute response time**.
1. Maintenance and support requires a minimum commitment with automatic renewal unless cancelled 3 months prior:
   - Enterprise Edition: **3 year commitment (i.e. $300K total over 3 years)**.
   - Hyperscale Edition: **5 year commitment (i.e. $50M total over 5 years)**.
   - Sovereign Edition: **10 year commitment (i.e. $500M total over 10 years)**.
1. Maintenance and support does not cover issues caused by modifications to the source code for the Sovereign Edition.
1. If payment lapses for more than 6 months, a new license must be purchased at the current price to resume support.

**NOTE:** for all editions, maintenance and support is conditional on continued compliance with the terms of the license.

## Source Access Terms & Conditions

1. Source code is provided **strictly for internal use** and cannot be sublicensed, leased, sold, or redistributed in
any form. For the purposes of this section, **internal use** refers to use solely within the named licensee Organization
as it existed at the time of contract signing, and does not extend to subsidiaries, affiliates, parent companies, or any
other entities regardless of their relationship to the licensee.

1. Source code is **only provided for the in-process library (DLL)**, which is the core component of the Software that
enables training and inference on ordinary CPUs. Source code for the standalone executable (EXE) and other materials
provided as part of the Software is NOT included in the source code provided to licensees.

1. Source code is **NOT transferable under any circumstances**, including through corporate transactions such as mergers,
acquisitions, divestitures, or changes in ownership. Any Organization that needs source code access but was not party to
the original license agreement must acquire a new license for its own use.

1. Licensees must **designate up to 5 named personnel** who will receive training to ensure business process continuity.
Named personnel will be selected, approved, and replaced by mutual written agreement between us and the licensee. Named
personnel are bound by the same terms and conditions as the licensee Organization during the term of the license, and
for a period of 10 years after termination or expiration of the license.

1. Licensees who **want source code access without the complexity and responsibility of designating named personnel, can
opt to hold the source code in escrow** under the custody of a mutually agreed-upon third party, then let us handle the
ongoing maintenance and support of the source code as part of routine maintenance and support of the Software for all
licensees.

1. Licensees will receive **quarterly snapshots of the source code** and are responsible for merging updates as needed.
The **first source code snapshot will be provided upon GA** and after full payment of the license fee.

1. Licensees have **perpetual rights to source snapshots already received**, provided they remain in compliance with the
terms of the license. Delivery of new snapshots requires continued annual maintenance and support payments. 

1. Licensees are **NOT permitted to use the source code and or Software to build products or services that compete with
the Software's core functionality of AI training and inference on ordinary CPUs**. This condition applies regardless of
whether the competing products or services are intended for internal use or for use by third parties. It also applies to
disclosures of any kind (including research papers, blog posts, talks, interviews, and discussions), as well as Application
messages, logs, or tooling (including tools for monitoring, debugging, or optimizing training and inference) that
intentionally or inadvertently expose implementation details that can only be known or derived through access to the
source code, whether those details are shared internally beyond named personnel or externally with third parties.

1. Licensees are permitted to **create derivative works of the source code by porting it to other programming languages
or creating hardware accelerators**. All derivative works are subject to the same terms and conditions as the original
source code unless otherwise mutually agreed-upon in writing (e.g. to allow co-development and commercialization of
derivative works that add significant value to the broader `AmaniGPT` ecosystem).

## Human Dignity

We require all licensees to commit to using `AmaniGPT` in a manner that **protects the dignity and value of human life**.

To make the concept actionable, we propose (and adopt for our own use) the PIT and PAT tests:

> **PIT (Personal Impact Test)**: would I support this Application if I were directly and equally affected by it?
>
> **PAT (Public Accountability Test)**: would I be willing to publicly answer for the consequences of this Application?

The two questions should be asked and answered in the affirmative when approving, funding, endorsing, designing,
developing, deploying, procuring, or using Applications built with `AmaniGPT`.

The PIT and PAT tests discourage negative uses. Consider the example of a lethal autonomous weapons system:

> **PIT**: would I support the development of lethal autonomous weapons if they could open fire at me without human intervention?
>
> **PAT**: would I be willing to publicly answer for the consequences of lethal autonomous weapons that I authorized or supported?

The PIT and PAT tests also encourage positive uses. Consider the example of an autonomous medical triage system:

> **PIT**: would I support the deployment of an autonomous medical triage system if I were a critically ill patient in
> an understaffed hospital with no access to a doctor?
>
> **PAT**: would I be willing to publicly answer for the benefits of an autonomous medical triage system that saved
> lives which would have otherwise been lost?

Applications that pass both tests with a confident **YES**, are the ones worth building with `AmaniGPT` and we look
forward to partnering with Organizations that will do truly legendary things for humanity :rocket:

## Feedback

We want to offer **the most refreshing licensing experience in the industry** and welcome your feedback so we can continue
to improve this guide as we approach general availability. Please email any suggestions and questions you may have to:
`licensing@amanigpt.com`

