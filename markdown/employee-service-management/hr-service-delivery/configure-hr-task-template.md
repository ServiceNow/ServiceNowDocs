---
title: Configure an HR task template
description: Create or modify an HR task template to automatically populate fields on the HR task form when that task is generated. You can configure an HR task template for an HR service or lifecycle event activity.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [HR templates, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure an HR task template

Create or modify an HR task template to automatically populate fields on the HR task form when that task is generated. You can configure an HR task template for an HR service or lifecycle event activity.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Choose one of the following.

<table id="choicetable_vvj_tvs_mgb"><thead><tr><th align="left" id="d779374e51">

Option

</th><th align="left" id="d779374e54">

Description

</th></tr></thead><tbody><tr><td id="d779374e60">

**HR service activity**

</td><td>

1.  Navigate to **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**, and open the HR service.

**Note:** Make sure **Fulfillment type** is set to `Service Activity`.

2.  In the **Service Activities** list at the bottom of the HR service form, open the service activity.

**Note:** Make sure **Activity type** is set to `Task`.

3.  In the **Child task template** field, click the Lookup icon.


</td></tr><tr><td id="d779374e115">

**\( Enterprise Onboarding and Transitions only\) Lifecycle event activity**

</td><td>

1.  Navigate to **Lifecycle Events** &gt; **Administration** &gt; **Activities**, and open the lifecycle event activity.

**Note:** Make sure **Activity type** is set to `Employee` or `Fulfiller`. For fulfiller types, make sure **Fulfiller activity** is set to `HR Task`.

2.  In the **HR task template** field, click the Lookup icon.


</td></tr></tbody>
</table>2.  Click **New** or open a record.

3.  Fill in the fields on the form, as appropriate.

<table id="table_rkf_vbl_mfb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td colspan="2">

Name of the HR task template.

</td></tr><tr><td>

Active

</td><td colspan="2">

Option to activate the HR task template for use.

</td></tr><tr><td>

Owning group

</td><td colspan="2">

Group that is responsible for the HR task template.

</td></tr><tr><td>

Short Description

</td><td colspan="2">

Short description that appears on the HR task form when the task is generated.

</td></tr><tr><td>

Optional

</td><td colspan="2">

Option to mark the HR task as optional.In the Tasks/To-Dos the Type indicator lets you filter the tasks based on the Required or Optional selection.

</td></tr><tr><td rowspan="15">

HR task type

</td><td colspan="2">

Type of the HR task. Select one of the following:

</td></tr><tr><td>

HR Service

</td><td>

An HR service fulfills the HR task. In the **HR Service** field, select an HR service.

</td></tr><tr><td>

Submit Catalog Item

</td><td>

A catalog item fulfills the HR task. In the **Catalog Item** field, select an active catalog item.

</td></tr><tr><td>

Submit Order Guide

</td><td>

An order guide fulfills the HR task. In the **Order Guide** field, select an order guide.

</td></tr><tr><td>

Collect employee input

</td><td>

Collects information from employees. In the **Employee form** field, select the employee form that the user will fill out or verify.**Note:** Employee forms are questionnaires built using the survey designer to collect information from employees. See [Collect employee input](../concept/employee-form-configuration.md) for more information.

</td></tr><tr><td>

Checklist

</td><td>

In the **Checklist Items** field, provide the checklist items.

</td></tr><tr><td>

E-signature

</td><td>

User electronically signs a document. In the **E-signature template** field, select the e-signature template to use.**Note:**

-   E-signature is a scoped application that enables users to sign managed documents, knowledge articles, or HR document templates with their typed or drawn signature, credentials, or as an acknowledgment. See [HR e-signature](../concept/hr-e-signature.md) for more information.
-   If HR document template is the document type of the e-signature template, you must select the HR document template that the signatory will sign on the HR case form. See [Select an HR document template for an e-signature task](select-hr-document-template-for-e-signature-task.md) for more information.


</td></tr><tr><td>

Credential

</td><td>

Prompts the user to login with their credentials to acknowledge conditions and terms related to their signature. To add text that explains what their login credentials mean, add the **Acknowledgment text** field. To add a document, add the **Acknowledgment document** field.**Note:**

-   This option is only available for existing customers that have not yet migrated to e-signature. See [Migrate existing HR task templates and open HR tasks to e-signature](migrate-existing-tasks-to-scoped-e-signature.md) for more information.
-   Starting with the Australia release, the HR task type: Credential will be hidden, but will continue to be supported. E-signature provides the latest experience for this functionality.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

E-Signature

</td><td>

Prompts the user to sign a document. To add text that explains what their signature means, add the **Acknowledgment text** field. To add a document, add the **Acknowledgment document** field.**Note:**

-   This option is only available for existing customers that have not yet migrated to e-signature. See [Migrate existing HR task templates and open HR tasks to e-signature](migrate-existing-tasks-to-scoped-e-signature.md) for more information.
-   Starting with the Australia release, the HR task type: E-signature \(e\_signature\) will be hidden, but will continue to be supported. E-signature provides the latest experience for this functionality.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

Mark When Complete

</td><td>

Notify the user a **Completed** button appears on the HR Service Portal. Use the **Short description** field to provide details about this task.**Note:** **Mark When Complete** changes the state of the task to **Closed Complete**.

</td></tr><tr><td>

Sign Document

</td><td>

Requests the subject person to edit or sign a document. An example is sending an education agreement to be signed for tuition reimbursement.This option is only available for existing customers that have not yet migrated to e-signature. See [Migrate existing HR task templates and open HR tasks to e-signature](migrate-existing-tasks-to-scoped-e-signature.md) for more information.

**Note:** The document must be included in the HR case template in the **PDF Template** field. See [Configure an HR case template](configure-hr-case-template.md).

To add text that explains what their signature means, add the **Acknowledgment text** field. To add a document, add the **Acknowledgment document** field.

Acknowledgment text entered on the HR document template overrides text written here. See  or .

**Note:**

Starting with the Australia release, HR task type: Sign Document will be hidden, but will continue to be supported. E-signature provides the latest experience for this functionality.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

Take Survey

</td><td>

In the **Survey** field, select a survey that the user is assigned to take.

</td></tr><tr><td>

Upload Documents

</td><td>

Requests the person assigned to the task to upload documents. Examples are receipts, course registration, or transcripts for tuition reimbursement. Use the **Short description** field to provide instructions.**Note:** The task must be in **Ready** or **Work in Progress**.

</td></tr><tr><td>

URL

</td><td>

In the **URL** field, provide a URL that the user acknowledges when accessed.

</td></tr><tr><td>

View Video

</td><td>

In the **URL** field, embed code/URL that the user is requested to view.

</td></tr><tr><td rowspan="3">

Assignment type

</td><td colspan="2">

Assignment of the HR task when the task is generated. You can assign the HR task to the employee or fulfiller. Select one of the following:

</td></tr><tr><td>

Employee

</td><td>

Select one of the following:-   Parent case subject person: Assign the task to the subject person of the parent case.
-   Parent case opened for: Assign the task to the opened for person on the parent case.
-   User from case: Assign the task to a user from the case.
-   Named user: Assign the task to a specific user.


</td></tr><tr><td>

Fulfiller

</td><td>

Select one of the following:-   Parent case assigned to: Assign the task to the person the parent case is assigned to.
-   Named user: Assign the task to a specific user
-   User from case: Assign the task to a user from the case.
-   Skills/Assignment group: Select the skills and group you want assigned to the task.


</td></tr><tr><td>

Due date

</td><td colspan="2">

Due date of the HR task. Select one of the following:-   Based on task assignment date
-   Based on parent case table


</td></tr><tr><td>

Set reminder

</td><td colspan="2">

Select to configure a reminder to send to the assignee.

</td></tr><tr><td>

Reminder template

</td><td colspan="2">

Select a relevant mail template.

</td></tr><tr><td>

When to send \(days\)

</td><td colspan="2">

Specify the number of days before the due date to send the initial reminder.

</td></tr><tr><td>

Interval \(days\)

</td><td colspan="2">

Enter the number of days between each reminder.

</td></tr><tr><td>

State

</td><td colspan="2">

State of the HR task when the task is generated. Select one of the following:-   Draft
-   Ready
-   Work in Progress
-   Closed Complete
-   Closed Incomplete
-   Cancelled
-   Skipped


</td></tr><tr><td rowspan="4">

Task support team

</td><td colspan="2">

Task support team for the HR task. The Task support team field defines the HR agent or queue that picks up any communication about the task when a user selects the Ask a question link. Select one of the following:

</td></tr><tr><td>

None

</td><td>

No task support team.

</td></tr><tr><td>

Users and groups

</td><td>

Select users from the parent case or HR groups as the task support team for the HR task.

</td></tr><tr><td>

Queue

</td><td>

Select a chat queue as the task support team for the HR task.

</td></tr><tr><td>

Use global descriptions for translations

</td><td colspan="2">

Option to enable the use of global descriptions for translations. If selected, you can provide the short description and description for the HR task template in one or more languages. See [Translations for HR cases and tasks](../concept/translation-of-hr-cases-and-tasks.md#) for more information.Check to show the **Global short description** and **Global description** fields. You can select a table \(top, right\) from the list and the associated dynamic variables from that table appear. You can add dynamic variables when creating your text to personalize the task. To use dynamic variables in the **Global short description** field, copy and paste the dynamic variables from the **Global description** field.

**Note:** Because some dynamic variables might provide personal information, use the sn\_hr\_core.task\_template\_variable\_ignore system property to ensure privacy. For example, social security number \(ssn\) is excluded by default. You can add other variables to this system property to disable them but ensure they are comma separated with no spaces between each variable.

</td></tr><tr><td>

Add field

</td><td colspan="2">

Fields to automatically populate on the HR task form when the task is generated. Select one or more fields from the **Add field** list and provide the desired values.When you add **Rich Description**, you can select a table \(top, right\) and the associated dynamic variables from that table appear. You can add dynamic variables when creating your text to personalize the task.

 **Note:** Because some dynamic variables might provide personal information, use the sn\_hr\_core.task\_template\_variable\_ignore system property to ensure privacy. For example, social security number \(ssn\) is excluded by default. You can add other variables to this system property to disable them but ensure they are comma separated with no spaces between each variable.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


