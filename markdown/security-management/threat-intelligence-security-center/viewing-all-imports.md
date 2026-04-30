---
title: Viewing all imports
description: Use this section to view all the imported records that are displayed in the list view for all the users.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working with Data Imports, Use, Threat Intelligence Security Center, Security Operations]
---

# Viewing all imports

Use this section to view all the imported records that are displayed in the list view for all the users.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Imports**.

2.  Select **Data Imports** &gt; **All Imports**

    This page displays all the records that are being processed for the import job.

3.  Open any record to view the status of the import process.

    **Note:** You can also click **New Import** to create a new import record. After you click this button, the application will direct you to the **Import Intelligence** page. For more information on creating new records, see [Import Intelligence in TISC](../concept/importing-threat-intelligence.md) section and proceed further with the respective import type.

4.  View the import summary.

    **Note:** The summary view is displayed only when the import record status is set to **Processed**.

    The import summary is displayed in three separate cards:

    -   **All Records**: Displays the processed records during the import run by providing a complete data view of what was included.
    -   **Dropped Records**: Lists the records that were skipped or failed validation.
    -   **Imported Records**: Displays only the records that are successfully imported into the application.
    The summary view provides you with a quick and structured overview of every record in the import process.

    Within the summary view, each record is displayed with key details such as explained in the following table:

    |Field|Description|
    |-----|-----------|
    |Record ID|The unique identifier of the processed record.|
    |Type|The type of TISC entity such as Observable, Indicator, Attack-Pattern and so on, associated with the imported record.|
    |Status|Indicates whether the record was imported successfully or dropped during import processing.|

    The cards **All Records** and **Dropped Records** provide a simplified view of each record, showing only the record ID and its status either imported or dropped.

    **Note:** The dropped records view also includes the reason for dropping the records from import processing.

    **Note:** If any records are dropped, an additional CSV attachment is provided containing the following fields:

    -   Serial Number
    -   Identifier
    -   Record Type
    -   Status
    -   Reason for Dropping
    The **Imported Records** card provides a detailed view of the source records that were created as a result of the import.

    For details on the various supported import formats, refer to the Related Links section.


**Parent Topic:**[Working with Data Imports](../concept/working-with-data-imports.md)

**Related topics**  


[Viewing my imports](viewing-my-imports.md)

[Viewing my approvals](viewing-my-approvals.md)

[Import data using structured file](import-data-using-structured-file.md)

[Import data using standard format](import-data-using-standard-format.md)

[Import data using raw text](import-data-using-pasted-text.md)

[Import data using unstructured file format](import-data-using-unstructured-file.md)

