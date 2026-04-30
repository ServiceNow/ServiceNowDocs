---
title: Notification workflow activity
description: The Notification activity sends an email or SMS message to specified users or groups.
locale: en-US
release: xanadu
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow notification activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Notification workflow activity

The **Notification** activity sends an email or SMS message to specified users or groups.

## Input variables

Update the recipients list or delete the activity from the workflow if you want to stop the notifications.

<table id="table_edm_z4l_gh"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="subhead" colspan="2">

Addressees

</td></tr><tr><td>

To

</td><td>

The users who will be recipients of the email.

</td></tr><tr><td>

To \(groups\)

</td><td>

The members of the groups that will be recipients of the email.

</td></tr><tr><td>

Advanced

</td><td>

If selected, the script in the **To \(script\)** field is called to specify additional recipients of the email.

</td></tr><tr><td>

To \(script\)

</td><td>

If **Advanced** is selected, this script is called and should set the variable *answer* to a comma-separated list of user or group sys\_ids that you want to add as recipients of the email.

</td></tr><tr><td class="subhead" colspan="2">

Message

</td></tr><tr><td>

Subject

</td><td>

The subject line of the email.

</td></tr><tr><td>

Message

</td><td>

The email body that is sent. To include the value of a field in the message body, place the cursor at the point in the text where you want the field's value inserted. Then click the + icon next to **Fields** and select the field you want.

</td></tr></tbody>
</table>## States

The activity state tells the workflow engine what to do with the activity.

|Field|Description|
|-----|-----------|
|Executing|The workflow engine knows to start the `run` function of the activity.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|

