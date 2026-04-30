---
title: Map a use case for contract metadata extraction
description: Map a use case to specific tables, and define conditions to apply the use case for metadata extraction.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-03-26"
reading_time_minutes: 3
breadcrumb: [Configuring contract metadata extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Map a use case for contract metadata extraction

Map a use case to specific tables, and define conditions to apply the use case for metadata extraction.

## Before you begin

Ensure that the application is in Global or Now Assist in Contract Management scope. If you are configuring the use case mapping in different application scope, add the scoped ACL to the Use Case Mapping table \(sn\_cm\_gen\_ai\_usecase\_configuration\).

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_contract\_config

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  On the tile for your skill, select **Activate skill**.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

4.  In the General details page, view the skill details and select **Save and continue**.

5.  In the Use case page, select **Save and continue**.

    For more information on creating a use case, see [Create use cases for contract metadata extraction](cmpro-na-usecase-me.md).

6.  In the Use case mappings page, select **New**.

7.  In the Create new use case mapping form, fill in the fields.

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

The use case used to extract metadata from a signed contract.**Note:** Only active use cases for contract metadata extraction are displayed in the list.

The **CM Pro - Contract Metadata Extraction** use case is available with the Now Assist in Contract Management base system.

</td></tr><tr><td>

Contract type

</td><td>

The contract type for which the use case will apply.**Note:** Only active contract types are displayed in the list.

</td></tr><tr><td>

Order

</td><td>

Order in which the use case will apply.If multiple use cases meet the same conditions, the use case with the lowest order number is applied first.

</td></tr><tr><td>

Request table

</td><td>

The Contract Request table \[sn\_cm\_core\_contract\_request\] is selected by default to centralize the configuration on a single table and improve reusability across product lines. You can choose to configure the use case mapping on a different table.

</td></tr><tr><td>

Contract repository table

</td><td>

The contract repository table where the extracted metadata will be added.

</td></tr><tr><td>

Request conditions

</td><td>

Conditions under which the use case applies on the request table.The field appears only when the request table is selected.

For more information on using the condition builder, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Repository conditions

</td><td>

Conditions under which the use case stores the extracted information on the repository table. The field appears only when the contract repository table is selected.

For more information on using the condition builder, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>8.  Select **Save**.


**Parent Topic:**[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

**Related topics**  


[Create use cases for contract metadata extraction](cmpro-na-usecase-me.md)

[Configure system properties for contract metadata extraction](cncore-conf-sys-prop-na.md)

[Enable notification for contract metadata extraction](cncore-config-notf-na-metadata.md)

[Configure the workspace URL for contract metadata extraction notifications](cncore-config-ext-wrkspc-email.md)

[Configure an extension point to add contract metadata](config-ext-pt-to-add-metadata.md)

