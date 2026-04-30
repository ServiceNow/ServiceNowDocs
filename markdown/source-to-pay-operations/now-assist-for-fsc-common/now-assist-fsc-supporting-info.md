---
title: Supporting information for Now Assist for Common Finance and Supply Chain features
description: Get a quick overview of the important information that is related to the Now Assist for Sourcing and Procurement Operations \(SPO\) application.
locale: en-US
release: zurich
product: Now Assist for FSC Common
classification: now-assist-for-fsc-common
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Now Assist for FSC Common, Now Assist for Finance and Supply Chain, Finance and Supply Chain]
---

# Supporting information for Now Assist for Common Finance and Supply Chain features

Get a quick overview of the important information that is related to the Now Assist for Sourcing and Procurement Operations \(SPO\) application.

## Supported versions

Now Assist for Common Finance and Supply Chain features is supported starting with Yokohama.

## Supported user interfaces

The Now Assist for Common Finance and Supply Chain features application includes the skills that are listed in the following table.

<table id="table_trn_hm4_1fc"><thead><tr><th>

Interface

</th><th>

Skills

</th></tr></thead><tbody><tr><td>

Source-to-Pay Workspace

</td><td>

-   Purchase order summarization for fulfillers
-   Supplier summarization for fulfillers

</td></tr></tbody>
</table>## Required roles

To use Now Assist for Common Finance and Supply Chain features, you need the roles listed in the following table.

<table id="table_i31_lm4_1fc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

admin

</td><td>

Installs the Now Assist for SPO, Now Assist for SLO, or Now Assist for APO plugins, and activates the Purchase order summarization for fulfillers and Supplier summarization for fulfillers skills.

</td></tr><tr><td>

sn\_fsc\_genai.now\_assist\_fulfiller

</td><td>

Generates summaries for purchase orders in the Source-to-Pay Workspace workspace.

</td></tr><tr><td>

sn\_fsc\_genai.now\_assist\_fulfiller

</td><td>

Generates summaries for suppliers in the Source-to-Pay Workspace workspace depending on the user persona:-   SPO: sn\_shop.procurement\_specialist with sn\_spend\_gen\_ai.now\_assist\_fulfiller role
-   SLO: sn\_slm.manager with sn\_supplier\_gen\_ai.now\_assist\_fulfiller role
-   APO: sn\_ap\_apm.accounts\_payable\_specialist with sn\_ap\_gen\_ai.now\_assist\_fulfiller role

</td></tr></tbody>
</table>## Application information

The Now Assist for FSC Common store app \(sn\_fsc\_genai\) includes the Purchase order summarization for fulfillers skill.

To use Now Assist for FSC Common \(sn\_fsc\_genai\) with SPO, SLO, or APO, install the corresponding plugins as required:

-   Now Assist for SPO \(sn\_spend\_gen\_ai\).
-   Now Assist for SLO \(sn\_supplier\_gen\_ai\)
-   Now Assist for APO \(sn\_ap\_gen\_ai\)

For more information, see [Configuring Now Assist for Common Finance and Supply Chain features](../task/configure-now-assist-fsc.md).

**Parent Topic:**[Explore Now Assist for Common Finance and Supply Chain Features](now-assist-fsc-exploring.md)

**Related topics**  


[Roles for Now Assist for FSC Common](now-assist-common-roles.md)

[Now Assist for Sourcing and Procurement Operations \(SPO\)](now-assist-spo.md)

[Now Assist for Supplier Lifecycle Operations \(SLO\)](../../supplier-lifecycle-operations/concept/now-assist-slo.md)

[Now Assist for Accounts Payable Operations \(APO\)](../../accounts-payable-operations/concept/now-assist-apo.md)

