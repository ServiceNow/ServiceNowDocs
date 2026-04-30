---
title: Create a task for a case using Agent Workspace for HR Case Management
description: Choose a task type when creating a task within a case. When assigning the task to an employee on Employee Center, you can also request how the employee acknowledges completion of that task.
locale: en-US
release: xanadu
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Using Agent Workspace for HR Case Management, Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# Create a task for a case using Agent Workspace for HR Case Management

Choose a task type when creating a task within a case. When assigning the task to an employee on Employee Center, you can also request how the employee acknowledges completion of that task.

## Before you begin

Role required: sn\_hr\_core.case\_writer

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Agent Workspace for HR Case Management** and select a case you want to add a task to.

2.  From the Child tabs above the Case details section, select the **HR Tasks** tab.

3.  Select **New**.

4.  Select an **HR task type**.

    The different task types you can select are:

<table id="table_c1w_mw2_kjb"><thead><tr><th>

Task type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HR Service:

</td><td>

An HR service fulfills the HR task. In the **HR Service** field, select an HR service.**Note:** **Bulk Parent Case** only appears as a selection when creating a parent case for child bulk cases. Refer to [Create a bulk case request](t_CreateBulkCases.md).

</td></tr><tr><td>

Submit Catalog Item:

</td><td>

A catalog item fulfills the HR task. In the **Catalog Item** field, select a catalog item.

</td></tr><tr><td>

Submit Order Guide:

</td><td>

An order guide fulfills the HR task. In the **Order Guide** field, select an order guide.

</td></tr><tr><td>

Collect Employee Input:

</td><td>

Collects information from employees. In the **Employee form** field, select the employee form that the user fills out or verifies.**Note:** Employee forms are questionnaires built using the survey designer to collect information from employees. See [Collect employee input](../concept/employee-form-configuration.md) for more information.

</td></tr><tr><td>

Checklist:

</td><td>

In the **Checklist Items** field, provide the checklist items. Checklists are instructions or steps on how to complete the task.**Note:** For more information, see [Using checklists in HR Service Delivery Agent Workspace](../concept/agent-ws-hr-checklists.md).

</td></tr><tr><td>

Credential:

</td><td>

Indicates that you want the user to acknowledge reading a document by logging in with their login credentials. The **Acknowledgment text** and **Acknowledgment document** fields appear. Using these fields shows a check box and text above the login credentials. In the Acknowledgment document field, select a document you want the user to read.**Note:** This option is only available for existing customers that have not yet migrated to e-signature. For more information, see [Migrate existing HR task templates and open HR tasks to e-signature](migrate-existing-tasks-to-scoped-e-signature.md).

</td></tr><tr><td>

E-signature:

</td><td>

User electronically signs a document. In the **E-signature template** field, select the e-signature template to use.**Note:**

-   E-signature is a scoped application that enables you to sign managed documents, knowledge articles, or HR document templates. You can type or draw your signature, credentials, or acknowledgment. For more information, see [HR e-signature](../concept/hr-e-signature.md).
-   If HR document template has a document type of e-signature template, select the HR document template that the signatory signs on the HR case form. For more information, see [Select an HR document template for an e-signature task](select-hr-document-template-for-e-signature-task.md).


</td></tr><tr><td>

Mark When Complete:

</td><td>

Notify the user a **Completed** button appears on the HR Service Portal. Use the **Short description** to provide details about this task.**Note:** **Mark When Complete** changes the state of the task to **Closed Complete**.

</td></tr><tr><td>

Sign Document:

</td><td>

Requests the user to sign a document. An example is sending an education agreement for signature on a tuition reimbursement. The **Acknowledgment text** field appears. Using this field shows a check box and text above the signature.**Note:**

-   This option is only available for existing customers that have not yet migrated to e-signature. For more information see [Migrate existing HR task templates and open HR tasks to e-signature](migrate-existing-tasks-to-scoped-e-signature.md).
-   After the user signs the document, the document generates with the signature and attaches to the task. The task closes and the document is attached to the case.


</td></tr><tr><td>

Schedule a meeting

</td><td>

Enables you to create a meeting invite for an employee while you are working on an HR case. For example, you can schedule a meeting with a new hire as part of the onboarding process. -   You can view the available slots of an employee and schedule a meeting. The employee will receive a meeting invite on Microsoft Outlook.
-   You can also send the meeting invite to external attendees.
**Note:** For the meeting invite and scheduling capability, you must install the ServiceNow Microsoft Exchange Online Spoke.

</td></tr><tr><td>

Take Survey:

</td><td>

In the **Survey** field, select a survey that the user is assigned to take.

</td></tr><tr><td>

Upload Documents:

</td><td>

Requests the person assigned to the task to upload documents. Examples are receipts, course registration, or transcripts for tuition reimbursement. Use the **Short description** field to provide instructions.**Note:** The task must be in **Ready** or **Work in Progress**.

</td></tr><tr><td>

URL:

</td><td>

The **URL** field appears. Enter a URL link that the user acknowledges when accessed.

</td></tr><tr><td>

View Video:

</td><td>

The **URL** field appears. Requests the person assigned to the task to view a video.

</td></tr></tbody>
</table>    **Note:** For information on all the fields, see [Adding an HR task to an HR case](t_ViewAnHRTask.md).

5.  Select **Save**.

    You can also add a task by selecting **Add Task** from the ![More icon](../reference/images/more-icon.png) from **Details**.


