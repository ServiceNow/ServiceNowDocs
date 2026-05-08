---
title: Adding an HR task to an HR case
description: You can add, view, or work on HR tasks assigned to HR cases.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Work an HR case, Use HR Case Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Adding an HR task to an HR case

You can add, view, or work on HR tasks assigned to HR cases.

## Before you begin

Role required: sn\_hr\_core.basic or sn\_hr\_core.case\_writer

## About this task

You can view HR tasks from the parent HR case or by going to **HR Case Management** &gt; **HR Tasks**.

## Procedure

1.  Open an HR case.

2.  Scroll to **Related Links** and click **Add Task**.

    -   HR Task: Select to add an HR task.
    -   Facilities Request: Select to create a facilities request such as desk or office space.
3.  To create an HR Task, complete:

<table id="table_jst_j1g_jr"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td colspan="2">

The auto-assigned task ID.**Note:** You cannot change this value.

</td></tr><tr><td>

Parent

</td><td colspan="2">

The case number you are creating the task for.

</td></tr><tr><td>

Location

</td><td colspan="2">

Select the location of the employee you are creating the task for.Location determines the HR agent assigned to the task.

**Note:** For onboarding cases that task selecting an office or desk, the location determines the building map that shows.

</td></tr><tr><td>

Template

</td><td colspan="2">

Click and select the HR Task template for this task. The HR Task template can auto-populate fields like the HR task type, short description, and the group or person the task is assigned to.

</td></tr><tr><td>

Stage

</td><td colspan="2">

The stage \(bundle\) of a lifecycle event case.Use this field to define what activity set in a lifecycle event case you want to add an ad hoc task to.

 For more information, see [Ad hoc cases and tasks for lifecycle event cases](../concept/le-ad-hoc-task.md#).

</td></tr><tr><td>

Due date

</td><td colspan="2">

Select the date the task is to be completed.

</td></tr><tr><td>

Set reminder

</td><td colspan="2">

Check to send an email notification based on the **Due date calculation** entries.**Note:** Reminders can also be set up on the **HR Task Template** to automatically populate.

</td></tr><tr><td>

Reminder template

</td><td colspan="2">

Select the email template used for reminder notifications. Email templates are set up from **HR Administration** &gt; **Email Content**.Refer to [Add or modify email content for notifications](CreateModEmailTemplate.md).

</td></tr><tr><td>

When to send \(days\)

</td><td colspan="2">

Enter the number of days before the task due date to send the reminder email.

</td></tr><tr><td>

Interval \(days\)

</td><td colspan="2">

Enter the number of days the reminder email should be sent on an interval.

</td></tr><tr><td rowspan="15">

HR task type

</td><td colspan="2">

When assigning a task to an employee, you can request how the employee acknowledges completion of the task. The tasks appear on the HR Service Portal for the employee.**Note:** The short description comes from the template, but you can add or modify it. It shows on the HR Service Portal.

</td></tr><tr><td>

HR Service

</td><td>

An HR service fulfills the HR task. In the **HR Service** field, select an HR service.**Note:** **Bulk Parent Case** does not appear as a selection because it is only used when creating a parent case for child bulk cases. Refer to [Create a bulk case request](t_CreateBulkCases.md).

</td></tr><tr><td>

Submit Catalog Item

</td><td>

A catalog item fulfills the HR task. In the **Catalog Item** field, select an active catalog item.

</td></tr><tr><td>

Submit Order Guide

</td><td>

An order guide fulfills the HR task. In the **Order Guide** field, select an order guide.

</td></tr><tr><td>

Collect Employee Input

</td><td>

Collects information from employees. In the **Employee form** field, select the employee form that the user fills out or verifies.**Note:** Employee forms are questionnaires built using the survey designer to collect information from employees. See [Collect employee input](../concept/employee-form-configuration.md) for more information.

</td></tr><tr><td>

Checklist

</td><td>

In the **Checklist Items** field, provide the checklist items.

</td></tr><tr><td>

E-signature

</td><td>

User electronically signs a document. In the **E-signature template** field, select the e-signature template to use.**Note:**

-   E-signature is a scoped application that enables you to sign managed documents, knowledge articles, or HR document templates. You can type or draw your signature, credentials, or acknowledgment. See [HR e-signature](../concept/hr-e-signature.md) for more information.
-   If HR document template has a document type of e-signature template, select the HR document template that the signatory signs on the HR case form. See [Select an HR document template for an e-signature task](select-hr-document-template-for-e-signature-task.md) for more information.


</td></tr><tr><td>

Credential

</td><td>

Indicates that you want the user to acknowledge reading a document by logging in with their login credentials. The **Acknowledgment text** and **Acknowledgement document** fields appear. Using these fields shows a check box and text above the login credentials. In the Acknowledgement document field, select a document that the user is asked to read.**Note:** This option is only available for existing customers that have not yet migrated to e-signature. See [Migrate existing HR task templates and open HR tasks to e-signature](migrate-existing-tasks-to-scoped-e-signature.md) for more information.

</td></tr><tr><td>

E-Signature

</td><td>

Indicates that you want the user to provide an e-signature to acknowledge or validate a document. The **Acknowledgment text** and **Acknowledgement document** fields appear. Using these fields shows a check box and text above the e-signature.**Note:** This option is only available for existing customers that have not yet migrated to e-signature. See [Migrate existing HR task templates and open HR tasks to e-signature](migrate-existing-tasks-to-scoped-e-signature.md) for more information.

</td></tr><tr><td>

Mark When Complete

</td><td>

Notify the user a **Completed** button appears on the HR Service Portal. Use the **Short description** to provide details about this task. **Note:** **Mark When Complete** changes the state of the task to **Closed Complete**.

</td></tr><tr><td>

Sign Document

</td><td>

Requests the user to sign a document. An example is sending an education agreement to be signed for tuition reimbursement. The **Acknowledgment text** field appears. Using this field shows a check box and text above the signature.**Note:** This option is only available for existing customers that have not yet migrated to e-signature. See [Migrate existing HR task templates and open HR tasks to e-signature](migrate-existing-tasks-to-scoped-e-signature.md) for more information.

 After the user signs the document, the document is generated with the signature and attached to the task. The task is closed complete and the document is attached to the case.

</td></tr><tr><td>

Take Survey

</td><td>

In the **Survey** field, select a survey that the user is assigned to take.**Note:** For lifecycle event cases, this feature also works if the subject person or anyone that has access to the original lifecycle event case can answer the survey question. For more information, see [Triggering an activity from upstream activities](configure-hr-lifecycle-event-activity.md#).

</td></tr><tr><td>

Upload Documents

</td><td>

Requests the person assigned to the task to upload documents. Examples are receipts, course registration, or transcripts for tuition reimbursement. Use the **Short description** field to provide instructions.**Note:** The task must be in **Ready** or **Work in Progress**.

</td></tr><tr><td>

URL

</td><td>

The **URL** field appears. Enter a URL link that the user acknowledges when accessed.

</td></tr><tr><td>

View Video

</td><td>

The **URL** field appears. Requests the person assigned to the task to view a video.

</td></tr><tr><td>

Activity

</td><td colspan="2">

Shows when an employee responds or completes a task and shows task activities by employee and assigned HR agent.

</td></tr><tr><td>

Optional

</td><td colspan="2">

Check to make the task optional. The **Skip** button appears for a task in the **Open Case** page. The **Subject person** can skip the task or do nothing and the HR agent can close complete the case.

</td></tr><tr><td>

State

</td><td colspan="2">

The work status of the case. The states are:

-   Draft
-   Ready
-   Work in Progress
-   Closed Complete
-   Closed Incomplete
-   Cancelled
-   Skipped
-   **Note:** Change the state to **Ready** or **Work in Progress** for the employee to see the task that you created.

</td></tr><tr><td>

Assignment group

</td><td colspan="2">

The HR group the case is assigned to. If the group is not set automatically, assign an HR group to provide a selection of HR users in the **Assigned to** field.

 Assignment groups are restricted to those groups with a type of human\_resources.

**Note:** To change the **Assignment group**, the **Assigned to** agent must be a member of the new group.

 This field also determines when Virtual Agent or Connect Support is used for the Ask a question feature.

-   Agent Workspace: Virtual Agent
-   Users and groups: Connect Support


</td></tr><tr><td>

Assigned to

</td><td colspan="2">

The user assigned to work on this case. If the user is not auto-assigned, click the lookup icon to select a user who is a member of the selected assignment group.

**Note:** To change the **Assigned to** HR agent, the agent must be a member of the **Assignment group**.

 You can also use this field to assign a task to the **Subject person** of the case. For example, if you want the **Subject person** to sign and return a document or make a task optional.

</td></tr><tr><td rowspan="4">

Task support team

</td><td colspan="2">

The point of contact within your company for questions.**Note:** To use, activate the Connect Service Portal Widgets \(com.glide.connect.sp\_widgets\) plugin.

</td></tr><tr><td>

Users and groups

</td><td>

Select when you want specific users or groups assigned to the HR case or task to be the primary support for this HR task. You can select from fields on the HR case or task such as the Opened by, Opened for, and others or you can select from different groups. You can further filter by selecting specific skills.

</td></tr><tr><td>

Connect

</td><td>

Selecting Connect indicates your company is using ServiceNow Connect messaging. After you select Queue, the Queue field appears below it. Select a chat queue you want to support the task you are creating. You can further filter by selecting specific skills.In previous releases, this field was labelled Queue.

 **Note:** The Connect support \(com.glide.connect.support\) plugin was deprecated. For more information, see [Activate Connect Support](https://www.servicenow.com/docs/access?context=t_ActivateConnectSupport&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Agent Workspace

</td><td>

Supports Agent Workspace for chat. Selecting Agent Workspace indicates your company uses Virtual Agent conversations for chat. After you select Agent Workspace, the AWA Queue field appears below it. Select the Advanced Work Assignment chat queue you want to support the task you are creating. You can further filter by selecting specific skills

</td></tr><tr><td>

Parent case users

</td><td colspan="2">

Appears when **Users and groups** are selected from **Task support team**.Select fields like Opened by, Opened for, and others from the parent HR case that you want to support this HR task.

</td></tr><tr><td>

Groups

</td><td colspan="2">

Appears when **Users and groups** are selected from **Task support team**.Select a group associated to the HR case or task to be the support for this HR task.

</td></tr><tr><td>

Queue

</td><td colspan="2">

Appears when **Queue** is selected from **Task support team**.Select the chat queue you want this HR task to be routed to for questions or help.

**Note:** What you select here must match the value in the **HR Queue** field on the Chat Setup form under Collaboration. If these values don't match, an error occurs.

</td></tr><tr><td>

Skills

</td><td colspan="2">

The required skills of the person assigned to this category of HR case.

</td></tr><tr><td>

Watch list

</td><td colspan="2">

The list of users who receive notifications regarding this case. Click the lock icon to add users. Click the **Add me** icon to include yourself.

</td></tr><tr><td>

Short description

</td><td colspan="2">

Short descriptions populate from the HR task template selected and can be overwritten.Enter information that prompts the user about the task request. The short description appears on the HR Service Portal to the employee.

</td></tr><tr><td>

Description

</td><td colspan="2">

A longer, detailed description of the case. Use the Rich Text Format \(RTF\) tools to format your text.Rich text formatting also appears for a case or task description on the Employee Service Center or service portal.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td colspan="2">

Enter comments, updates, or information about the task that is visible to the **Subject person** on the case.**Note:** Translate the text in your preferred language using the **Translate** option. For configuring the dynamic translation framework, see [Dynamic translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Work notes

</td><td colspan="2">

Enter notes about the case to correspond with other HR agents. These notes are not visible to the **Subject person**. **Note:** Translate the text in your preferred language using the **Translate** option. For configuring the dynamic translation framework, see [Dynamic translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>4.  You can:

    -   Click **Save** from the **Content menu** to save the task and remain on the **Task** form.
    -   Click **Submit** to save the task and return to the **HR Case** form.
    -   Click **Ready for Work** to save the task and change the state to **Ready** and remain on the **Task** form.
    -   Click **View Responses** to view the feedback submitted by an employee via the form sent through the HR task of type **Collect Employee Input**.
5.  Perform any of the following actions.

<table id="choicetable_fp3_2wv_rr"><thead><tr><th align="left" id="d201048e1002">

Action

</th><th align="left" id="d201048e1005">

Description

</th></tr></thead><tbody><tr><td id="d201048e1011">

**Assign to me**

</td><td>

Click

</td></tr><tr><td id="d201048e1020">

**Close a task**

</td><td>

Enter information in the **Work notes** field and other fields as needed, and change the **State** to **Closed Complete**.**Note:** All HR tasks must be closed before the parent HR case can be closed.

</td></tr><tr><td id="d201048e1041">

**Clone task**

</td><td>

Click the **Clone Task** related link. Enter the new task information in the task form and click **Update**.

</td></tr><tr><td id="d201048e1056">

**Cancel the task**

</td><td>

Click **Cancel Task** in the form header.

</td></tr><tr><td id="d201048e1069">

**Review the progress of sibling tasks**

</td><td>

The **Sibling Tasks** tab shows all tasks under the same case. Click a task number to see the details.

</td></tr><tr><td id="d201048e1081">

**HR Document Acknowledgement**

</td><td>

Lists HR document acknowledgement types returned from an employee. You can filter by type:-   User
-   Document revision
-   Signature
-   Updated


</td></tr></tbody>
</table>    When all tasks are closed for an HR case, an email notification is sent to the HR agent who is assigned to the case.

    **Note:** When you close the parent case, all child tasks are assigned the Closed Incomplete state.

6.  Click the attachment icon at the top of the form, to add a document attachment

    Attachments to tasks are available on the parent case.

7.  Click **Update**.


-   **[Create Office Space Request Task](HRTaskOfficeSpaceReq.md)**  
As part of the onboarding process, you can find and reserve an office space for a new hire.

**Parent Topic:**[Work an HR case](t_CreateAnHRCase.md)

