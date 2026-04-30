---
title: Send Email activity
description: Create an email from previously gathered or generated data. Use this activity to send an email. This activity requires the playbook author to define who the email should be sent to, the subject, and the body. This activity surfaces the pre-defined content for the email to the end user so that the end user can confirm before sending the email.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Interactive activities, Playbooks reference, Reference, Workflow Studio, Build workflows]
---

# Send Email activity

Create an email from previously gathered or generated data. Use this activity to send an email. This activity requires the playbook author to define who the email should be sent to, the subject, and the body. This activity surfaces the pre-defined content for the email to the end user so that the end user can confirm before sending the email.

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

<table id="table_ajt_sr3_plb"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

String

</td><td>

Title to display as activity and playbook card.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Information to display about activity usage or outcome.

</td></tr><tr><td>

Run condition

</td><td>

Condition Builder

</td><td>

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Start Rule

</td><td>

Choice

</td><td>

Under **Schedule** &gt; **Start Rule**, select a start rule for when your stage should start running:-   **When process starts**: Your stage starts running as soon as the playbook starts.
-   **After specific stages**: Your stage starts running after specified stage\(s\) have finished running.

Under Schedule &gt; Start Rule, select a start rule for when your activity should start running:-   **When stage starts**: Your activity starts running as soon as its stage starts running. Your stage starts running when your playbook is triggered.
-   **After specific activities**: Your activity starts running after specified activities have finished running.

</td></tr><tr><td>

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](start-with-delay-properties.md).**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

To

</td><td>

List of Users

</td><td>

Recipient list for the email. There are 2 ways to configure this field:-   Enter email addresses as strings if you want the emails to go to the same addresses every time.
-   When the email address value varies, use the pill picker to indicate where to find the recipient email address. For example, you would use the pill picker if you wanted to automatically notify credit card applicants of a rejection, because each applicant has a different email.

You would select the customer record from the trigger \(when the application was submitted\), because that is where the applicant's email address is found.

![Using the pill picker to reference the email address.](../images/send-to-customer-pillpicker.png)


</td></tr><tr><td>

Cc

</td><td>

List of Users

</td><td>

Cc recipient list for the email.

</td></tr><tr><td>

Subject

</td><td>

String

</td><td>

Subject of the email.

</td></tr><tr><td>

Body

</td><td>

HTML

</td><td>

Body of the email.**Tip:** You can use both text and multiple pills in your message, and any other rich text or HTML field.

</td></tr><tr><td>

Wait for user input

</td><td>

Choice

</td><td id="wait-process">

Option to pause the playbook until the end user manually completes or skips the activity. Only users with the playbook.admin role can edit this field. By default, the activity waits for user action or data before it completes.

</td></tr><tr><td>

Tagline

</td><td>

String

</td><td>

Activity tagline to display to end users.

</td></tr><tr><td>

Record fields

</td><td>

Reference

</td><td>

Any additional record fields you want in the email.**Note:** This field cannot be edited during a playbook run.

</td></tr><tr><td>

Footer

</td><td>

String

</td><td>

Footer content for your email. You can enter a footer as a string, or use the pill picker to reference data \(e.g. a timestamp\) that you want to display at the bottom of the email.**Note:** This field cannot be edited during a playbook run.

</td></tr><tr><td>

Form View

</td><td>

String

</td><td>

Form view to use for sending an email. If you don't provide a form view, the system uses the default view. Use the **new tab** button ![a button that opens a new tab](../images/new-tab-button.png)to open and edit a form view with Form Builder in a new Workflow Studio tab.**Note:** Many form views are not supported in Workspace.

</td></tr><tr><td>

Form fields

</td><td>

Reference

</td><td>

Any additional fields you want in the playbook activity card.**Note:** This field cannot be edited during a playbook run.

</td></tr></tbody>
</table>## Advanced inputs

After configuring the required inputs for your activity, you can also choose to configure additional inputs. In the side panel, select **Show additional options** to display these advanced inputs. For more information, see [Activity experience](../concept/activity-definitions.md#activity-experience).

<table id="table_cjj_sr3_plb"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assigned To

</td><td>

Reference.User \[sys\_user\]

</td><td>

User responsible for completing the task associated with the activity.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Assignment Group

</td><td>

Reference.Group \[sys\_user\_group\]

</td><td>

Group responsible for completing the task associated with the activity.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

To Email Address

</td><td>

String

</td><td>

Comma-separated list of email addresses.

</td></tr><tr><td>

Cc Email Address

</td><td>

String

</td><td>

Comma-separated list of copied email addresses.

</td></tr><tr><td>

Bcc

</td><td>

List of Users

</td><td>

Bcc blind copy recipient list for the email.

</td></tr><tr><td>

Bcc Email Address

</td><td>

String

</td><td>

Comma-separated list of blind copied email addresses.

</td></tr><tr><td>

Target Record

</td><td>

Reference.Task \[task\]

</td><td>

Reference to the record that the system attaches the email to.

</td></tr><tr><td>

Table

</td><td>

Table Name

</td><td>

Table containing activity or playbook data.

</td></tr></tbody>
</table>## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Automated|True/False|Whether the flow automatically completes or requires user input. If set to **True**, the activity card in Playbook Experience displays a **Automated Task** tagline.|
|Record|Reference.Task\[task\]|Reference to record created.|
|Email|Reference.Notification\[sysevent\_email\_action\]|Reference to the newly created email notification record|

**Parent Topic:**[Interactive activities](../concept/interactive-activities.md)

