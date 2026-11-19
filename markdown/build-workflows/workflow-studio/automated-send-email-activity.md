---
title: Send Email activity
description: Create an email from previously gathered or generated data without pausing the playbook to ask for user input. When the activity runs, it immediately sends the email and continues to the next activity in the playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/automated-send-email-activity.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Non-Interactive activities, Playbooks reference, Reference, Workflow Studio, Build workflows]
---

# Send Email activity

Create an email from previously gathered or generated data without pausing the playbook to ask for user input. When the activity runs, it immediately sends the email and continues to the next activity in the playbook.

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/dot-walking-examples.md).

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

Start Rule

</td><td>

Choice

</td><td>

Under **Schedule** &gt; **Start Rule**, select a start rule for when the activity should start running:-   **When stage starts**: The activity starts running as soon as its stage starts running.
-   **After specific activities**: The activity starts running after specified activities have finished running. You can select one more activities from the available activities. By default, the previous activity is selected.

</td></tr><tr><td>

Display order

</td><td>

Choice

</td><td>

Option to select the order in which you want to display the activity to end users at run time. From the **Playbook display order** list, select the display order for the activity.

</td></tr><tr><td>

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/start-with-delay-properties.md).**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Run condition

</td><td>

Condition Builder

</td><td>

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Restart rules

</td><td>

Choice

</td><td>

The restart rule defines how the activity runs when the playbook is restarted. Options are:-   **Skip on restart**: The stage or activity runs only during the initial run. It does not run when the playbook is restarted. Use this rule when you don't want new tasks or records to be created during a restarted run. This is important if the original execution and its resulting record are still relevant.
-   **Run always**: The activity runs during the initial run and in any restarted run.
-   **Skip on first run**: The activity runs only during a restarted run. It never runs during the initial run.

</td></tr></tbody>
</table>## Automation inputs

The following inputs are available in the Automation tab of the activity properties.

<table id="table_cjj_sr3_plb"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

To

</td><td>

List of Users

</td><td>

Recipient list for the email. There are 2 ways to configure this field:-   Enter email addresses as strings if you want the emails to go to the same addresses every time.
-   When the email address value varies, use the pill picker to indicate where to find the recipient email address. For example, you would use the pill picker if you wanted to automatically notify credit card applicants of a rejection, because each applicant has a different email.

You would select the customer record from the trigger \(when the application was submitted\), because that is where the applicant's email address is found.

\[Omitted image "send-to-customer-pillpicker.png"\] Alt text: Using the pill picker to reference the email address.


</td></tr><tr><td>

To Email Address

</td><td>

String

</td><td>

Comma-separated list of email addresses.

</td></tr><tr><td>

Cc

</td><td>

List of Users

</td><td>

Cc recipient list for the email.

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

BCC recipient list for the email.

</td></tr><tr><td>

Bcc Email Address

</td><td>

String

</td><td>

Comma-separated list of blind copied email addresses.

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

These outputs can provide data to other activities in your playbook. The outputs are available in the **Automation** tab and you can access this data as activity inputs when you configure your activity:

|Output|Type|Description|
|------|----|-----------|
|Record|Reference.Task\[task\]|Reference to record created.|
|Email|Reference.Notification\[sysevent\_email\_action\]|Reference to the newly created email notification record|

**Parent Topic:**[Non-Interactive activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/non-interactive-activities.md)

