---
title: Contract metadata extraction use case mapping form
description: Use the Create use case mapping form in the contract metadata extraction skill to map the use case to specific tables and conditions.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Map a use case, Configure metadata extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract metadata extraction use case mapping form

Use the Create use case mapping form in the contract metadata extraction skill to map the use case to specific tables and conditions.

<table id="table_lxd_sm1_wcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the use case mapping.

</td></tr><tr><td>

Use case

</td><td>

The use case used to extract metadata from a signed contract.**Note:** Only active use cases for Contract metadata extraction are displayed in the list.

The **CM Pro - Contract Metadata Extraction** use case is available with the Now Assist in Contract Management base system.

</td></tr><tr><td>

Contract repository table

</td><td>

The contract repository table where the contract records are created. The extracted metadata will be added in this table.

</td></tr><tr><td>

Order

</td><td>

Order in which the use case will apply.If multiple use cases meet the same conditions, the use case with the lowest order number is applied first.

</td></tr><tr><td>

Contracts created from contract request

</td><td>

Option to apply the use case to contracts initiated from a contract request.When the check box is cleared, the use case applies to contracts that are directly uploaded on a contract record, without a contract request. The check box is selected by default.**Note:** The check box appears only when the Now Assist in Contract Management \(sn\_cm\_gen\_ai\) and Contracts core \(sn\_cm\_core\) plugins are installed.

</td></tr><tr><td>

Contract type

</td><td>

The contract type for which the use case will apply.**Note:** Only active contract types are displayed in the list.

This field appears only when the **Contracts created from contract request** check box is selected.

</td></tr><tr><td>

Request table

</td><td>

The Contract Request table \[sn\_cm\_core\_contract\_request\] is selected by default to centralize the configuration on a single table and improve reusability across product lines. You can choose to configure the use case mapping on a different table.This field appears only when the **Contracts created from contract request** check box is selected.

</td></tr><tr><td>

Request conditions

</td><td>

Conditions under which the use case applies on the request table.The field appears only when the **Contracts created from contract request** check box and the request table are selected.

For more information on using the condition builder, see Create a condition statement using the condition builder.

</td></tr><tr><td>

Repository conditions

</td><td>

Conditions under which the use case applies on the repository table. The field appears only when a table is selected in the **Contract repository table** field.

For more information on using the condition builder, see Create a condition statement using the condition builder.

</td></tr></tbody>
</table>**Parent Topic:**[Map a use case for contract metadata extraction](../task/cmpro-na-usecase-mappings-me.md)

