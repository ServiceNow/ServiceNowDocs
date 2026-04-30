---
title: Map a use case for contract metadata extraction
description: Map a use case to specific tables, and define conditions to apply the use case for metadata extraction.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Contract metadata extraction, Contract use case mapping, Metadata extraction use case mapping, Now Assist use case mapping, Now Assist in contract management pro, Now Assist for contract management pro, AI for contract management pro]
breadcrumb: [Configure metadata extraction, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Map a use case for contract metadata extraction

Map a use case to specific tables, and define conditions to apply the use case for metadata extraction.

## About this task

The following video walks you through the process of mapping use cases for the contract metadata extraction skill.Video explaining how to map use cases for contract metadata extraction. 

## Before you begin

Ensure that the application is in the Global or Now Assist in Contract Management scope. If you are configuring the use case mapping in a different application scope, add the scoped ACL to the Use Case Mapping table \(sn\_cm\_gen\_ai\_usecase\_configuration\).

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  Select **Activate skill** on the skill that you want to activate.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

4.  In the General details page, view the skill details and select **Save and continue**.

5.  In the Use case page, select **Save and continue**.

    For more information on creating a use case, see [Create use cases for contract metadata extraction](cmpro-na-usecase-me.md).

6.  In the Use case mappings page, select **New**.

7.  On the Create new use case mapping form, fill in the fields.

    For a description of the field values, see [Contract metadata extraction use case mapping form](../reference/cmpro-na-use-case-map-form-me.md).

8.  Select **Save**.


## Result

The use case is mapped to specific tables and conditions, and it is applied for metadata extraction when the conditions are met.

-   **[Contract metadata extraction use case mapping form](../reference/cmpro-na-use-case-map-form-me.md)**  
Use the Create use case mapping form in the contract metadata extraction skill to map the use case to specific tables and conditions.

**Parent Topic:**[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

**Related topics**  


[Create use cases for contract metadata extraction](cmpro-na-usecase-me.md)

[Configure system properties for contract metadata extraction](cncore-conf-sys-prop-na.md)

[Enable notification for contract metadata extraction](cncore-config-notf-na-metadata.md)

[Configure the workspace URL for contract metadata extraction notifications](cncore-config-ext-wrkspc-email.md)

[Configure an extension point to add contract metadata](config-ext-pt-to-add-metadata.md)

[Create use cases for contract metadata extraction](cmpro-na-usecase-me.md)

