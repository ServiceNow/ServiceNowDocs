---
title: Map a use case for contract obligation extraction
description: Map a use case to specific tables, and define conditions to apply the use case for obligation extraction.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 3
keywords: [Obligation extraction use case mapping]
breadcrumb: [Configure obligation extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Map a use case for contract obligation extraction

Map a use case to specific tables, and define conditions to apply the use case for obligation extraction.

## Before you begin

Ensure that the application scope is in Global or Now Assist in Contract Management scope. If you’re configuring the use case mapping in a different application scope, add the scoped ACL to the Use Case Mapping table \(sn\_cm\_gen\_ai\_usecase\_configuration\).

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  On the tile for your skill, select **Activate skill**.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

4.  In the General details page, view the skill details and select **Save and continue**.

5.  In the Use case page, select **Save and continue**.

    For more information on creating a use case, see [Create use cases for contract obligation extraction](cmpro-na-use-case-obext.md).

6.  In the Use case mappings page, select **New**.

7.  On the form, fill in the fields.

    ![Create new use case mapping form to map obligations with request tables and repository tables.](../image/cmpro-na-ob-map.png "Create new use case mapping form")

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

The use case used to extract obligations from a signed contract.**Note:** Only active use cases for the contract obligation extraction skill are displayed in the list.

The **CM Pro - Contract Obligation Extraction** use case is available with the Now Assist in Contract Management base system.

</td></tr><tr><td>

Contract type

</td><td>

The contract type for which the use case applies.**Note:** Only active contract types are displayed in the list.

</td></tr><tr><td>

Order

</td><td>

Order in which the use case will apply.If multiple use cases meet the same conditions, the use case with the lowest order number is applied first.

</td></tr><tr><td>

Request table

</td><td>

The table from which contract requests are created. The use case applies to contracts created from the selected table.The Contract Request table \[sn\_cm\_core\_contract\_request\] is selected by default to centralize the configuration on a single table and improve reusability across product lines. You can choose to configure the use case mapping on a different table.

</td></tr><tr><td>

Contract repository table

</td><td>

The repository table where the contract records are created. The use case applies to contracts stored in the selected table.

</td></tr><tr><td>

Request conditions

</td><td>

Conditions under which the use case applies on the request table.The field appears only when the request table is selected.

For more information on using the condition builder, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Repository conditions

</td><td>

Conditions under which the use case applies on the repository table. The field appears only when a table is selected in the **Contract repository table** field.

For more information on using the condition builder, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>8.  Select **Save**.


## Result

The use case is mapped to specific tables and conditions, and it’s applied for obligation extraction when the conditions are met.

## What to do next

[Activate business rules for the Manage contract repository agentic workflow](conf-repository-agentic-ai.md)

**Parent Topic:**[Configuring contract obligation extraction](cncore-conf-obligation-extraction.md)

**Related topics**  


[Create use cases for contract obligation extraction](cmpro-na-use-case-obext.md)

