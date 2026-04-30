---
title: Automated Send Email activity
description: Create an email from previously gathered or generated data without pausing the playbook to ask for user input. When the activity runs, it immediately sends the email and continues to the next activity in the playbook.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Non-Interactive activities, Playbooks reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Automated Send Email activity

Create an email from previously gathered or generated data without pausing the playbook to ask for user input. When the activity runs, it immediately sends the email and continues to the next activity in the playbook.

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

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

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** **Show additional options** to see this field.

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

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](start-with-delay-properties.md).**Note:** **Show additional options** to see this field.

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

Body of the email.

</td></tr></tbody>
</table>## Advanced inputs

After configuring the required inputs for your activity, you can also choose to configure additional inputs. In the side panel, select **Show additional options** to display these advanced inputs. For more information, see [Activity experience](../concept/activity-definitions.md#activity-experience).

|Input|Type|Description|
|-----|----|-----------|
|To Email Address|String|Comma-separated list of email addresses.|
|Cc Email Address|String|Comma-separated list of copied email addresses.|
|Bcc|List of Users|Bcc blind copy recipient list for the email.|
|Bcc Email Address|String|Comma-separated list of blind copied email addresses.|
|Target Record|Reference.Task \[task\]|Reference to the record that the system attaches the email to.|
|Table|Table Name|Table containing activity or playbook data.|

## Outputs

These outputs can provide data to other activities in your playbook. You can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Record|Reference.Task\[task\]|Reference to record created.|
|Email|Reference.Notification\[sysevent\_email\_action\]|Reference to the newly created email notification record|

**Parent Topic:**[Non-Interactive activities](../concept/non-interactive-activities.md)

