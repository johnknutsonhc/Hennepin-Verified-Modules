---
draft: false
title: Introduction
linktitle: Introduction
type: default
weight: 1
description: Introduction to the Hennepin Verified Modules (HVM) program
---


## What is Hennepin Verified Modules?

Hennepin Verified Modules (HVM) are a concept borrowed from Azure Verified Modules (AVM) From Microsoft. They say:

As "One Microsoft", we want to provide and define the single definition of what a good IaC module is;

- How they should be constructed and built
  - Enforcing consistency and testing where possible
- How they are to be consumed
- What they deliver for consumers in terms of resources deployed and configured
- And where appropriate aligned across IaC languages (e.g. Bicep, Terraform, etc.).

{{% notice style="tip" title="Mission Statement" icon="heart" %}}
Our mission is to deliver a comprehensive Hennepin Verified Modules library in multiple IaC languages, following the principles of the well-architected framework, serving as the trusted Microsoft source of truth. Supported by Microsoft, HVM will accelerate deployment time for Azure resources and architectural patterns, empowering every person and organization on the planet on their IaC journey.
{{% /notice %}}

### Definition of "Verified" Summary

- The modules are supported as described in [Module Support]({{% siteparam base %}}/help-support/module-support/)
- Modules are aligned to clear specifications that enforces consistency between all HVM modules. *See the 'Specifications & Definitions' section in the menu*
- Modules will continue to stay up-to-date with product/service roadmaps owned by the module owners and contributors
- Modules will align to WAF high priority recommendations. *See ['What does HVM mean by "WAF Aligned"?']({{% siteparam base %}}/faq/#what-does-avm-mean-by-waf-aligned)*
- Modules will provide clear documentation alongside examples to promote self-service consumption
- Modules will be tested to ensure they comply with the specifications for HVM and their examples deploy as intended

## How will we create, support and enforce Hennepin Verified Modules?

Hennepin Verified Modules will achieve this, and its mission statement, by implementing and enforcing the following; driven by the Cloud Operations Team:

1. Publishing HVM modules to Hennepin private registries for consumption
    - For Terraform this will be the [Hennepin Private Terraform Registry](https://stgapi.hennepincounty.gov/)
2. Creating, publishing and maintaining the Hennepin Verified Modules specifications (this site)
    - Including IaC language specific specifications (today Terraform, possibly Ansible soon)
3. Creating easy to follow HVM module contribution and publishing guidance for each IaC language
4. Encouraging tests for each HVM module is compliant with the HVM specifications, where possible, via Unit and Integration tests
5. Encouraging End-to-End Deployment tests of each HVM module
