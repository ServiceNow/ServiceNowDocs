---
title: Approve the library import task
description: Approve the library import task by using the Library import task form in the GRC: Policy and Compliance integrator application.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [GRC: Policy and Compliance integrator, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Approve the library import task

Approve the library import task by using the Library import task form in the GRC: Policy and Compliance integrator application.

## Before you begin

Role required: sn\_compliance.manager

## Procedure

1.  Navigate to **All** &gt; **Policy and compliance integrator** &gt; **Content integrator** &gt; **Library import task**.

2.  Review the library import task and the related lists for the authority document staging records, citation staging records, control objective staging records, and content onboarding tasks.

3.  In the application navigator, go to Recommendations and review the recommendations that are provided by the application for the task.

4.  On the form, click **Import** or **Reject**.

    Review the details of the library import task and either import or reject the record as shown in the following example.

    ![Import or reject a library import task.](../image/import-or-reject-lit.png "Import or reject a library import task")

    Clicking **Import** imports the record that is associated with the library import task into the GRC: Policy and Compliance Management staging tables.

    Clicking **Reject** rejects the record that is associated with the library import task. As a result, the data is not imported into the GRC: Policy and Compliance Management staging tables.

5.  Click **Submit for approval**.

    The task is submitted to the compliance managers group for approval. The state of the library import task is updated to Submitted for approval as shown in the following example.

    ![Task submitted for approval.](../image/lit-submitted-for-approval.png "Task submitted for approval")

6.  Review the library import task and click **Approve**.

    This action moves the library import task to Ready for import state.

    **Note:** Clicking **Reject** rejects the library import task and moves it to New state again as shown in the following example.

    ![Library import task in Ready for import state.](../image/lit-ready-for-import.png "Library import task in Ready for import state")

    When the task is in the Ready for import state, the Import action is displayed as shown in the following example.

    ![Task to be imported.](../image/lit-import.png "Task to be imported")

7.  Click **Import**.

    This action imports the staging records under the library import task into the GRC: Policy and Compliance Management tables. You can view the tables by navigating to the authority document tables, citation tables, or control objectives tables in the GRC: Policy and Compliance Management application. See the sample Authority documents table as shown in the following example.

    ![Authority documents table.](../image/lit-authority-documents.png "Authority documents table")

    When you click an authority document, such as AD0020004 that is displayed in the table, it displays the details of the authority document staging record. In the staging record, the Document status field on the form displays information on the current document status. When the document status field value is New or Update, the Import or Reject actions are available for the record, and the import task can be imported or rejected as shown in the following example.

    ![Import or reject actions for a new document.](../image/import-reject-import-actions.png "Import or reject actions for a new document")

    When the document status field value is No change, only the Ignore option is available in the Import action for the record. The import task can be ignored as shown in the following example.

    ![Ignore action for no change in the document status.](../image/ignore-import-action.png "Ignore action for no change in the document status")

    See the following table for the criteria of the Document status field values.

    |Field|Description|
    |-----|-----------|
    |Document status = New|Record that is not found in the GRC: Policy and Compliance Management tables.|
    |Document status = No change|**Source last modified date** of the existing record in the GRC: Policy and Compliance Management table that is later than the incoming staging record date. The document status does not change.|
    |Document status = Update|**Source last modified date** of the existing record in the GRC: Policy and Compliance Management table that is earlier than the incoming staging record date. The document status is updated.|

    After the workflow is completed, the Compliance staging processor flow automatically updates the status of the library import task to Completed.

    **Note:**

    If an error occurs in the processing of the flow, the Compliance staging processor flow updates the state of the library import task to Completed with errors. This error can happen due to one of the following reasons:

    -   The taxonomy value mappings of the record are not found and the automap value of the provider taxonomy configuration is false.
    -   The parent of the record is ignored.
    The record with the error is rejected by the Compliance staging processor flow.

    When the status of the library import task is Completed, the import task summary and the related links of the import sets are displayed only to the users with the import\_transformer role as shown in the following example. The import\_transformer role is a global role.



    The import\_transformer role view summary is not available to any other users of the GRC: Policy and Compliance integrator application.


## Result

The library import task is now in the Completed state and the content is imported into the Policy and Compliance Management application.

