---
title: Import models and templates in JSON format
description: Create an import request to import your collection of models and templates in JSON format, and streamline the workflow using the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Import models and templates, Use, Telecommunications Network Inventory]
---

# Import models and templates in JSON format

Create an import request to import your collection of models and templates in JSON format, and streamline the workflow using the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin

## About this task

After you create an import template request, a detailed summary is generated that categorizes the processed records, such as total records, skipped, inserted, ignored, updated, and failed records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Import** &gt; **Imports**.

3.  Select **New**.

4.  On the Select an Import File Type window, select **Import Models and Templates \(JSON\)** from the list.

5.  On the **Details** tab, fill in the general information.

    The following table lists the fields that are unique to the import model request.

<table id="table_xxp_hq1_dtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Identification of the import model or template.

</td></tr><tr><td>

Description

</td><td>

Short description of the import models or templates.

</td></tr><tr><td>

File

</td><td>

Select **Attach File** to attach the import model file in JSON format.**Note:**

-   Models import is only for **Equipment Model**, **Equipment Holder Model**, **Card Model**, and **Interface Model**.
-   Import doesn’t support images.


</td></tr></tbody>
</table>6.  Download the demo data and model template by selecting **Create Excel Template**.

7.  Select **Import**.

    -   During the data import procedure:
        -   Integration Commons for CMDB: The plugin is automatically activated and by default. To learn more, see [Integration Commons for CMDB](https://www.servicenow.com/docs/access?context=integration-commons-for-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
        -   Normalization Data Service Client \(Optional\): If installed and configured, the following normalization rules are applied.
            -   Removes special characters from the **Manufacturer** name.
            -   The new value is replaced if it matches with five characters of the existing value.
            -   Downloads standard and variant company names.
            -   Replaces company names with their standard equivalents. To learn more, see [Normalization data services](https://www.servicenow.com/docs/access?context=c_NormalizationOverview&version=australia&pubname=australia-platform-administration&ft:locale=en-US). To customize the normalization rules, see [Normalized company names table](https://www.servicenow.com/docs/access?context=r_NormalizedCompanyNames&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    -   The generation of a record triggers its automatic addition to the **Import Results**. From this tab, you can see the import status and can select the generated model.
    -   A dedicated inventory template is generated for every rack/cabinet equipment holders, equipment models, and card models. Moreover, the related templates are generated based on the defined model relationship.

**Parent Topic:**[Import models and templates](../concept/import-models-and-templates.md)

