---
title: Hennepin Verified Modules
linktitle: Hennepin Verified Modules
type: home
description: 'Hennepin Verified Modules - The Hennepin County IaC Module Strategy'
---

## Introduction

Welcome. Here you will find Terraform modules verified for use at Hennepin County.

This site was copied from the [Azure Verified Modules](https://github.com/Azure/Azure-Verified-Modules) repository. It is still being updated for Hennepin County, so you may come across outdated references, links, etc. You can report any issues by [creating an issue](https://github.com/johnknutsonhc/Hennepin-Verified-Modules/issues)

## Value Proposition

<table style="border: none; border-collapse: collapse; margin:0; padding:0;">
  <tr>
    <td style="border: none; padding:0; margin:0; width:65%">

Hennepin Verified Modules (HVM) is an initiative to consolidate and set the standards for what a good Infrastructure-as-Code module looks like.

Modules will then align to these standards, across languages (Terraform, Ansible, etc.) and will then be classified as HVMs and available from their respective language specific registries.

HVM is a common code base, a toolkit for our Customers, our Partners, and Microsoft. It's an official, Microsoft driven initiative, with a devolved ownership approach to develop modules, leveraging internal & external communities.

Hennepin Verified Modules enable and accelerate consistent solution development and delivery of cloud-native or migrated applications and their supporting infrastructure by codifying Microsoft guidance (WAF), with best practice configurations.

  </td>
    <td style="border: none; margin:0; padding: 0;">
      <img src="{{%siteparam base%}}/images/avm_cycle.png" width=65% alt="HVM development cycle" style="margin:0 auto;padding: 0;">
    </td>
  </tr>
</table>

## Modules

<table style="border: none; border-collapse: collapse; margin: 0; padding: 0;">
  <tr>
    <td style="border: none; padding: 0; width:55%">
        <img src="{{%siteparam base%}}/images/avm_modules.png" width=80% alt="HVM module classifications">
    </td>
    <td style="border: none; padding: 0;">
Hennepin Verified Modules provides two types of modules: Resource and Pattern modules.

HVM modules are used to deploy Azure resources and their extensions, as well as reusable architectural patterns consistently.

Modules are composable building blocks that encapsulate groups of resources dedicated to one task.

- Flexible, generalized, multi-purpose
- Integrates child resources
- Integrates extension resources

HVM improves code quality and provides a unified customer experience.
    </td>
  </tr>
</table>

## Next Steps

<table style="border: none; border-collapse: collapse; margin: 0; padding: 0;">
  <tr>
    <td style="border: none; padding: 0; width:60%">

1. Review [Overview]({{% siteparam base %}}/overview/introduction)
2. Review the [Module Classification Definitions]({{% siteparam base %}}/specs/shared/module-classifications/)
3. Review the [Specifications]({{% siteparam base %}}/specs/module-specs/)
4. Review the [FAQ]({{% siteparam base %}}/faq/)
5. Learn how to [contribute to HVM]({{% siteparam base %}}/contributing/)
    </td>
    <td style="border: none; padding: 0;">

    ![HVM]({{%siteparam base%}}/images/avm_logo.png?width=10vw "HVM")

    </td>

  </tr>
</table>
