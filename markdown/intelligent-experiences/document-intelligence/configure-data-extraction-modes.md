---
title: Configure data extraction modes
description: Configure the extraction modes for use cases to define how Document Intelligence extracts fields from documents.
locale: en-US
release: xanadu
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up document extraction use cases, Configuring Document Intelligence, Document Intelligence, Enable AI experiences]
---

# Configure data extraction modes

Configure the extraction modes for use cases to define how Document Intelligence extracts fields from documents.

## Before you begin

Role required: sn\_docintel.manager

## About this task

Extraction modes determine how the data is extracted in the document task and how the task is processed. The mode changes the behavior of the fields in the Document Intelligence workspace.

DocIntel uses the following extraction modes.

<table id="table_pmc_dqx_qbc"><thead><tr><th>

Extraction mode

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recommendation

</td><td>

DocIntel provides recommendations for the fields in the Document Intelligence workspace. Choose the recommendation or manually enter the value. All fields must be reviewed.

 Recommendations are ordered based on how confident the AI is in the prediction. As DocIntel continues processing your documents, recommendations improve over time.

</td></tr><tr><td>

Auto-fill

</td><td>

DocIntel auto-fills the fields in the Document Intelligence workspace. All fields must be reviewed.

 Auto-fill works only if the AI has enough confidence to make the prediction. You can change the confidence threshold by updating the **Auto-fill threshold** field in the use case.

</td></tr><tr><td>

Fully automated

 \(Straight-through processing\)

</td><td>

DocIntel automatically extracts the data for all fields and processes the document task if the confidence scores for all required fields are above the defined confidence threshold. Fields don’t need to be reviewed.

 DocIntel becomes more confident over time, as it processes more and more documents. Choose Fully automated mode for frequently processed documents or if you’re confident in the system.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction Administration** &gt; **Use Cases**.

2.  Select the use case that you would like to configure.

3.  Select the settings icon \(![Use case settings icon](../image/icon-docintel-settings-gear.png)\).

4.  Select the extraction mode for the use case.

    -   If the DocIntel AI model needs further training to make recommendations with higher confidence scores, leave the default recommendation mode in place without selecting any other mode.
    -   If DocIntel provides recommendations with confidence scores above the specified threshold, select the **Auto-fill mode** option.
    -   If DocIntel auto-fills the required fields with very high confidence scores, select the **Fully Automated mode** option.
5.  Adjust the auto-fill threshold and warning threshold for Auto-fill mode.

    -   **Auto-fill threshold**: DocIntel only auto-fills the fields if the confidence score of the top recommendation is at or above the percentage you define.

        Fields with a confidence score lower than the threshold are left empty in the Document Intelligence workspace, and the recommendation mode is available to extract these fields.

    -   **Warning threshold**: DocIntel shows a warning for empty fields and auto-filled fields with a confidence score at or below the percentage that you define.

6.  Adjust the confidence threshold for required fields in Fully automated mode.

    -   DocIntel automatically completes and submits the document task if all required fields have a confidence score at or above the percentage you define in the **Fully-automated threshold** field.

    -   If any required field is below the threshold, the document task isn’t submitted automatically and requires agent review. Fields that aren’t required may be left empty or unreviewed.

    -   If there are no fields defined as required for the document task, then DocIntel automatically completes and submits the document task.

7.  Select **Save**.


