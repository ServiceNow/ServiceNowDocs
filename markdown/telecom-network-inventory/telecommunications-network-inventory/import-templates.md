---
title: Import templates
description: Import Template enables you to capture all required inventory details in a prescribed, predefined Excel format and upload them in bulk to the system. Create an import template request to import your inventory templates, enforce data formatting, and streamline the process using the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Import models and templates, Use, Telecommunications Network Inventory]
---

# Import templates

Import Template enables you to capture all required inventory details in a prescribed, predefined Excel format and upload them in bulk to the system. Create an import template request to import your inventory templates, enforce data formatting, and streamline the process using the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager, and sn\_ni\_core.inventory\_template\_manager

## About this task

After you create an import template request, a detailed summary is generated that categorizes the processed records, such as total records, skipped, inserted, ignored, updated, and failed records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Import** &gt; **Imports**.

3.  Select **New**.

4.  On the Select an Import File Type window, select **Import Templates \(xls\)** from the list.

5.  On the **Details** tab, fill in the general information.

    The following table lists the fields that are unique to the import template request.

    |Field|Description|
    |-----|-----------|
    |Name|Identification of the import template.|
    |Description|Short description of the import template.|
    |File|Select **Attach File** to attach the import inventory template file.|

6.  Download the demo data and the template by selecting **Create Excel Template**.

    The template is created based on the Import template template \[sn\_ni\_adv\_import\_template\_template\] table. You can customize the template and update it as required.

7.  Select **Import**.

    -   The generation of a record triggers its automatic addition to the **Import Results**. From this tab, you can see the import status and can select the generated inventory template.
    -   The related templates are generated only if the model relationship is defined, such as, for rack or equipment or card inventory template, related templates of slots are generated.

## Result

The **Import Results** tab appears next to the Details tab where you can view, add, update, and delete the import set row.

## What to do next

-   Redirect to the generated inventory template from the **Import Results** tab.
-   Delete a record. To learn more, see [Delete a record](delete-inventory-record.md).

**Parent Topic:**[Import models and templates](../concept/import-models-and-templates.md)

