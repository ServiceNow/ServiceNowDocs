---
title: Transform settings
description: Configure the transform settings for your Integration Hub - Import integration. Specify batch size and empty-field handling, enable verbose mode, or run a script before or after the integration.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration Hub - Import, Importing and streaming data in Integration Hub, Integration Hub, Data and Automation]
---

# Transform settings

Configure the transform settings for your Integration Hub - Import integration. Specify batch size and empty-field handling, enable verbose mode, or run a script before or after the integration.

## Configure transform settings

You can configure the transform settings for your integration by selecting the **Transform Settings** button at the top of the Map to target page in Integration Hub - Import.

**Note:** The **Transform Settings** button doesn't appear until you've added at least one target table to the Map to target page. For more information, see [Map source data to a target table](../tasks/map-source-data-target.md).

<table id="table_snt_djm_3xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Batch Size

</td><td>

Number of items to transform in each batch.

 Default value: 10

</td></tr><tr><td>

Verbose

</td><td>

Option to enable transform logs with details on transform operations, transformer rules, and transforms with multiple target tables.

 Default value: false

</td></tr><tr><td>

Copy Empty Fields

</td><td>

Option to copy any empty values in the source fields to the target fields.

 When this field is selected, empty source values are copied. When it's not selected, empty source values are not copied to the target fields.

 Default value: true

</td></tr><tr><td class="sub-head" colspan="2">

Scripts

</td></tr><tr><td>

Execute OnBefore Script

</td><td>

Option to run a script before inserting or updating data. Send notifications, modify data, or perform other actions before the integration begins.

 The onBefore script has three parameters.

-   **source**: The source data from the import record.
-   **target**: The transformed data from the import record. In the onBefore script, this parameter accesses transformed data before it's inserted into the target table.
-   **importLog**: The log that records information about data import activity.

 The onBefore script has two variables.

-   **ignore**. Type: Boolean. When **true**, the specified import set row is ignored.
-   **ignore\_reason**. Type: String. Message describing why the import set row was ignored.

</td></tr><tr><td>

Execute OnAfter Script

</td><td>

Option to run a script after inserting or updating data. Send notifications, calculate summaries, or perform other actions after the integration completes.

 The onAfter script has three parameters.

-   **source**: The source data from the import record.
-   **target**: The transformed data from the import record. In the onAfter script, this parameter accesses transformed data after it's inserted into the target table. Once a record is inserted or updated, it has a sys\_id.
-   **importLog**: The log that records information about data import activity.

</td></tr></tbody>
</table>**Parent Topic:**[Integration Hub - Import](../concept/integrationhub-imports.md)

