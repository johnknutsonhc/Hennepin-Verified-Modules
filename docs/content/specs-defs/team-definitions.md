---
title: Team Definitions & RACI
url: /specs/shared/team-definitions/
description: Team Definitions & RACI for the Hennepin Verified Modules (HVM) program
---

## Teams

In HVM there will be multiple different teams involved throughout the initiatives lifecycle and ongoing long-term support. These teams will be listed below alongside their definitions.

{{% notice style="important" %}}

Individuals can be members of multiple teams, at once, that are defined below.

{{% /notice %}}

### HVM Core Team

GitHub Team: [`@Azure/avm-core-team`](https://github.com/orgs/Azure/teams/avm-core-team)

The HVM core team are responsible for:

- Specifications
  - Shared
  - Language Specific
- Contribution Guidance
- Test Frameworks & Tooling
- Initiative Governance
  - Module Lifecycle
  - Test Enforcement
  - Module Support SLAs
- Anything else not defined below for another team or in the RACI 👍

The team is made up of both technical and non-technical team members that are all Microsoft FTEs.

### Module Owners

{{% notice style="important" %}}

Today, module owners **MUST** be Microsoft FTEs. This is to ensure that within HVM the long-term support for each module can be upheld and honoured.

{{% /notice %}}

Module owners are responsible for:

- Module Creation
- Module Maintenance (proactive & reactive)
- Module Issue/Pull Request Triage & Resolution
- Module Feature Request Triage & Additions
- Managing Module Contributors

Ideally there **SHOULD** be at least 2 module owners per module and **MUST** be in a [GitHub Team in the `Azure` organization.](https://github.com/orgs/Azure/teams/)

### Module Contributors

{{% notice style="important" %}}

Module Contributors can be anyone in any organization. However, they must be an active contributor and supporting the Module Owners.

{{% /notice %}}

Module Contributors are responsible for:

- Assisting the Module Owners with their responsibilities

Module Contributors **MUST** be in a separate [GitHub Team in the `Azure` organization](https://github.com/orgs/Azure/teams/), that the Module Owners manage and are maintainers of.

### Product Groups

GitHub Teams:

- [`@Azure/bicep-admins`](https://github.com/orgs/Azure/teams/bicep-admins) = Bicep PG team
- [`@Azure/terraform-avm`](https://github.com/orgs/Azure/teams/terraform-avm) = Azure Terraform PG

The Azure Bicep & Terraform Product Groups are responsible for:

- Backup/Additional support for orphaned modules to the HVM Core Team
- Providing inputs and feedback on HVM
- Taking on feedback and feature requests on their products, Bicep & Terraform, from HVM usage

{{% notice style="note" %}}

We are investigating working with all Azure Product Groups as a future investment area that they take on ownership, or contribute to, the HVM modules for their service/product.

{{% /notice %}}

## RACI

{{% notice style="note" title="RACI Definition" %}}

**R = Responsible** – Those who do the work to complete the task/responsibility.

**A = Accountable** – The one answerable for the correct and thorough completion of the task. There must be only one accountable person per task/responsibility. Typically has 'sign-off'.

**C = Consulted** – Those whose opinions are sought.

**I = Informed** – Those who are kept up to date on progress.

{{% /notice %}}

The below table defines a RACI that is proposed to be adopted by HVM and all parties referenced in the table. This will give consumers faith and trust in these modules so that they can consume and contribute to the initiative at scale.

| Action/Task/Responsibility                                                                       | Module Owners | Module Contributors | HVM Core Team | Product Groups | Notes |
| ------------------------------------------------------------------------------------------------ | ------------- | ------------------- | ------------- | -------------- | ----- |
| Build/Construct an HVM Module                                                                    | R, A          | R, C                | C, I          | I              |       |
| Publish a Bicep HVM Module to the Bicep Public Registry                                          | R, A          | C, I                | C, I          | I              |       |
| Publish a Terraform HVM Module to the Terraform Registry                                         | R, A          | C, I                | C, I          | I              |       |
| Manage and maintain tooling/testing frameworks pertaining to module quality                      | C, I          | C, I                | R, A          | C, I           |       |
| Manage/run the HVM central backlog (module proposals, orphaned modules, test enhancements, etc.) | C, I          | C, I                | R, A          | C, I           |       |
| Provide day-to-day (BAU) module support                                                          | R, A          | R, C                | I             | I              |       |
| Provide security fixes for orphaned modules                                                      | N/A           | N/A                 | R, A          | R, C, I        |       |
