---
title: Module Lifecycle
url: /specs/shared/module-lifecycle/
description: Module Lifecycle description for the Hennepin Verified Modules (HVM) program
---
{{% notice style="note" %}}

This page is still a work in progress

{{% /notice %}}

## Request/Propose a New HVM Resource or Pattern Module

Please review the [Process Overview]({{% siteparam base %}}/contributing/process/#new-module-proposal--creation) for guidance on proposing a new HVM module.

## Orphaned HVM Modules

It is critical to the consumers experience that modules continue to be maintained. In the case where a module owner cannot continue in their role or do not respond to issues as per the defined timescale in the [Module Support page]({{% siteparam base %}}/help-support/module-support/) , the following process will apply:

1. The module owner is responsible for finding a replacement owner and providing a handover.
2. If no replacement can be found or the module owner leaves Microsoft without giving warning to the HVM core team, the HVM core team will provide essential maintenance (critical bug and security fixes), as per the [Module Support page]({{% siteparam base %}}/help-support/module-support/)
3. The HVM core team will continue to try and re-assign the module ownership.
4. While a module is in an orphaned state, only security and bug fixes **MUST** be made, no new feature development will be worked on until a new owner is found that can then lead this effort for the module.
5. An issue will be created on the central HVM repo (`Azure/Azure-Verified-Modules`) to track the finding of a new owner for a module

### Notification of a Module Becoming Orphaned

{{% notice style="important" %}}
When a module becomes orphaned, the HVM core team will communicate this through an information notice to be placed as follows.

- In case of a Bicep module, the information notice will be placed in an `ORPHANED.md` file and in the header of the module's `README.md` - both residing in the module's root.
- In case of a Terraform module, the information notice will be placed in the header of the `README.md` file, in the module's root.

The information notice will include the following statement:

{{< highlight lineNos="false" type="markdown" wrap="true" title="orphaned-module-notice.md" >}}
{{% include file="/static/includes/orphaned-module-notice.md" %}}
{{< /highlight >}}

{{% /notice %}}

Also, the HVM core team will amend the issue automation to auto reply stating that the repo is orphaned and only security/bug fixes are being handled until a new module owner is found.
