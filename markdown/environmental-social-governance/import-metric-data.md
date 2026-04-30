---
title: Import historical metric data and tasks
description: Import historical metric data with or without corresponding metric data tasks.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Importing historical metric data, Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Import historical metric data and tasks

Import historical metric data with or without corresponding metric data tasks.

## Before you begin

Download the metric template and follow the instructions to fill it out. You must use this .xlsx template for importing historical metric data. For more information on creating a metric data template, see [Download a metric import template](create-metric-data-template.md).

Role required: sn\_esg.metric\_manager or esg.program\_manager

## About this task

Importing historical metric data enables program managers and metric managers to manage and analyze past performance, identify trends, and make informed decisions. This process includes downloading a template, filling it with necessary data, and uploading it back into the system, which then creates metric data tasks.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Lists** &gt; **Metric Import jobs**.

2.  Select **New** to create a new metric import job.

3.  Fill in the form and then select **Save**.

<table id="table_krg_p53_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Provide a name for the metric data import job.

</td></tr><tr><td>

Description

</td><td>

Provide a brief description of the metric data import job.

</td></tr><tr><td>

State

</td><td>

The state of a job is updated as the metric import job is processed.-   Draft
-   In progress
-   Completed with errors
-   Completed


</td></tr></tbody>
</table>4.  Attach the completed template file by selecting the attachments icon ![Attachment icon.](../../esg-management-reporting/images/attachment-icon.png) and selecting the file from your local hard drive.

    **Important:** The questionnaire template is downloaded in the .xlsx format and after being completed must be uploaded in the same format.

5.  Select **Save**.

    The template file has been uploaded and a metric import job has been created.

6.  Navigate to the **Transform history** tab and **Import log** tab to review potential errors, the number of metrics processed, ignored, or skipped, error messages, and their levels of severity, and so on.

    1.  Correct any errors in the Microsoft Excel spreadsheet.

    2.  Attach the updated template file by selecting the attachments icon ![Attachment icon.](../../esg-management-reporting/images/attachment-icon.png) and selecting the file from your local hard drive.

    3.  Select **Re-import** and repeat until all errors are resolved and the import metrics job is completed successfully.

        Select the help icon ![Help icon.](../image/help-icon.png) for additional instructions on re-importing a metric job.

    The metrics are imported and their associated metric data task records are created.

    **Note:** Metric data tasks are assigned based on the state of the metric data and the approval requirements. If data is provided, the state of the metric data task moves to Work In Progress. You must submit the task for the state to update to Awaiting approval or closed. Approval records are created and assigned according to the metric definition approval. If approval is not required, the task is created in a new state. Additionally, if the metric data is completed, a metadata task is created for audit purposes.


**Parent Topic:**[Importing historical metric data](../concept/importing-metric-data.md)

