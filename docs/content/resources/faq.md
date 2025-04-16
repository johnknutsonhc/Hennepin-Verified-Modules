---
title: Frequently Asked Questions (FAQ)
linktitle: FAQ
aliases: ["/faq"]
description: Frequently Asked Questions (FAQ) for the Hennepin Verified Modules (AVM) program
---

{{% notice style="tip" %}}

Got an unanswered question? Create a [GitHub Issue](https://github.com/johnknutsonhc/Hennepin-Verified-Modules/issues) so we can get it answered and added here for everyone's benefit 👍

{{% /notice %}}

## Timeline, history, plans

### When will we have a library that has a "usable" stand? Not complete, but the most important resources?

- **Bicep**: AVM evolved all modules of [CARML](https://aka.ms/CARML) (Common Azure Resource Module Library) for its Bicep resource module collection (see [here]({{% siteparam base %}}/resources/faq#carml-to-avm-evolution)). To initially populate AVM with Bicep resource modules, all existing CARML modules have been migrated to AVM. Resource modules can now be directly leveraged to support the IaC needs of a wide variety of Azure workloads. Pattern modules can also be developed building on these resource modules.
- **Terraform**: In case of Terraform, there were significantly less modules available in [TFVM](https://aka.ms/TFVM) (Terraform Verified Modules Library) compared to CARML, hence, most Terraform modules have been and are being built as people volunteer to be module owners. We've been prioritizing the development of the Terraform modules based on our learnings from former initiatives, as well as customer demand - i.e., which ones are the most frequently deployed modules.

---

### What happened to existing initiatives like CARML and TFVM?

The AVM team worked/works closely with the teams behind the following initiatives:

- [CARML (Common Azure Resource Modules Library)](https://aka.ms/CARML)
- [TFVM (Terraform Verified Modules)](https://aka.ms/TFVM)
- [BRM (Bicep Registry Modules)](https://aka.ms/BRM) - this is where the AVM Bicep modules are published.

{{% notice style="note" %}}
AVM is a straight-line evolution of CARML & TFVM.

- **All previously existing assets from these two libraries have been incorporated into AVM as resource or pattern modules.**
- All previously existing (non-AVM) modules that were published in the Public Bicep Registry (stored in the `/modules` folder of the BRM repository) have either been [retired or transformed into an AVM module](https://github.com/Azure/bicep-registry-modules?tab=readme-ov-file#%EF%B8%8F-new-standard-for-bicep-modules---avm-%EF%B8%8F) - while some are still being worked on.
  {{% /notice %}}

#### CARML to AVM Evolution

CARML can be considered AVM's predecessor. It was started by Industry Solutions Delivery (ISD) and the Customer Success Unit (CSU) and has been contributed to by many across Microsoft and has also had external contributions.

A lot of CARML's principles and architecture decisions have formed the basis for AVM. Following a small number of changes to make them AVM compliant, all CARML modules have been transitioned to AVM as resource or pattern modules.

In summary, CARML **evolved** to and has been rebranded as the Bicep version of AVM. A notice has been placed on the CARML repo redirecting users and contributors to the AVM central repository.​

#### Terraform Timeline and Approach

The Cloud Operations team is not necssarily responsible for the development or maintenance of every published module. However, they support following activities to facilitate and optimize the development process:

- Provide support and guidance for developing and/or implementing Terraform modules.
- Leveraging customer demand, telemetry and learnings from former initiatives to prioritize the development of Terraform modules.
- Providing automated tools and processes (CI environment and automated tests).
- Accelerating the build-out of the Terraform module owners' community.
- Recruiting new volunteers to build and maintain Terraform modules.

---

### Why not just use Microsoft's AVM/WAF/CAF/etc. modules?

While we lean **heavily** on some of Microsoft's code, we are generally developing our own modules and patterns that fit Hennepin County's current needs.

Many of the Azure Verified Modules (AVM) and Well/Cloud-Architected Framework (WAF/CAF) modules attempt to do everything for you, often in opinionated ways. This works well for an organization performing a greefield deployment, but would not fit well here.

---

## Definitions, comparisons

---

### What does AVM mean by "WAF Aligned"?

{{% notice style="tip" %}}

WAF == [Well-Architected Framework](https://learn.microsoft.com/en-us/azure/well-architected/) (as per our [glossary]({{% siteparam base %}}/glossary/))

{{% /notice %}}

At a high-level "WAF Aligned" means, where possible and appropriate, AVM Modules will align to recommendations and default input parameters/variables to values that algin to **high impact/priority/severity recommendations** in the following frameworks and resources:

- [Well-Architected Framework (WAF)](https://learn.microsoft.com/azure/well-architected/what-is-well-architected-framework)
- [Reliability Hub](https://learn.microsoft.com/azure/reliability/overview-reliability-guidance)
- [Azure Proactive Resiliency Library (APRL)](https://aka.ms/aprl)
  - _Only Product Group (PG) verified_

For security recommendations we will also utilize the following frameworks and resources; **again only for high impact/priority/severity recommendations**:

- [Microsoft Defender for Cloud (MDFC)](https://learn.microsoft.com/en-us/azure/defender-for-cloud/recommendations-reference)

#### Will all AVM modules be 100% "WAF Aligned" out of the box and good to go?

Not quite, but they'll certainly be on the right path. By default, modules will only have to set defaults for input parameters/variables to values that align to high impact/priority recommendations, as detailed above.

To understand this further you first must understand that some of the "WAF Aligned" recommendations, from the sources above are more than just setting a string or boolean value to something particular to meet the recommendation; some will require additional resources to be created and exist and then linked together to help satisfy the recommendation.

In these scenarios the AVM modules will not enforce the additional resources to be deployed and configured, but will provide sufficient flexibility via their input parameters/variables to be able to support the configuration, if so desired by the module consumer.

{{% notice style="tip" %}}

This is why we **only** enforce AVM module alignment to **high** impact/priority recommendations, as the the majority of recommendations that are not **high** impact/priority will require additional resources to be used together to be compliant, as the below example will show.

{{% /notice %}}

##### Some examples

| Recommendation                                                         | Will Be Set By Default in AVM Modules?                                                                            |
| ---------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| TLS version should always be set the latest/highest version TLS 1.3    | **Yes**, as string value                                                                                          |
| Key Vault should use RBAC instead of access policies for authorization | **Yes**, as string/boolean value                                                                                  |
| Container registries should use private link                           | **No**, as requires additional Private Endpoint and DNS configuration as well as, potentially, additional costs   |
| API Management services should use a virtual network                   | **No**, as requires additional Virtual Network and Subnet configuration as well as, potentially, additional costs |

{{% notice style="important" %}}

While every Well-Architected Framework pillar's recommendations should equally be considered by the module owners/contributors, within AVM we are taking an approach to prioritize reliability and security over cost optimization. This provides consumers of the AVM modules, by default, more resilient and secure resources and patterns.

However, please note these defaulted values can be altered via input parameter/variables in each of the modules so that you can meet your specific requirements.

{{% /notice %}}

---

### What is a "Primary Resource" in the context of AVM?

The definition of a Primary Resource is detailed in the [glossary]({{% siteparam base %}}/glossary/).

### How does AVM align and assist with the Secure Future Initiative (SFI)?

AVM modules are continuously being improved with the security and reliability recommendations of the Well-Architected Framework (for more details, see what AVM means by "[WAF-aligned](#what-does-avm-mean-by-waf-aligned)"). The AVM team is continuously reviewing SFI recommendations and if required rolling out updates to the AVM initiative to remain SFI compliant as well as assisting module owners to ensure their modules help their consumers align to SFI where appropriate.

---

## Contribution, module ownership

Some basic information on contribution can be found in the [Terraform contribution guide]({{% siteparam base %}}/contributing/terraform/).

### Can I contribute to AVM without being a module owner?

Yes, you can contribute to a module without being its owner, but you'll need a module owner whom you can collaborate with.

- You can propose a [new module](https://github.com/johnknutsonhc/Hennepin-Verified-Modules/issues) and provide as much context as possible under the "Module Details" section (e.g., why do you need the module, what's the business impact of not having it, etc.). The AVM core team will try to find a Microsoft FTE to be the module owner whom you can collaborate with.
- You can contact the current owner of any existing module and offer to contribute to it. You can find the current owners of all AVM modules in the [module indexes]({{% siteparam base %}}/indexes/).

---

### Can I submit a PR with new features to an existing module? If so, is this a good way to contribute too?

Of course! As all modules are inner-sourced, meaning anyone from Hennepin County can submit a PR to an existing module. But we'd suggest opening an issue first to discuss the suggested changes with the module owner before investing time in the code.

---

## Support

### Help, I'm stuck!

If you are stuck, feel free to reach out in the "Terraform Community of Practice" team in Microsoft Teams.

## Technical questions

### Should pattern modules leverage resource modules? What if (some of) the required resource modules are not available?

Ideally, pattern modules would leverage existing published HVM resource modules for the underlying resources that make up the pattern, but this is not a strict requirement.

---

### Does AVM use semantic versioning?

Yes! For generic guidance, see [SNFR17 - Semantic Versioning]({{% siteparam base %}}/spec/SNFR17).

## Using AVM

### Private registry authentication

Terraform can leverage an environment variable for authentication to a private registry. The format for the variable is `TF_TOKEN_sub_domain_com`.

The Hennepin private terraform module registry served from the stgapi.hennepincounty.gov domain, and expects a JWT issued by our Entra tenant. For example:|

```pwsh
$env:TF_TOKEN_stgapi_hennepincounty_gov=az account get-access-token --query accessToken -o tsv
```
