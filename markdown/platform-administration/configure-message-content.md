---
title: Configure message content
description: Create a message in the Message Contents \[messaging\_content\] table that you can use in multiple notifications. Messages can be informative, or they can request action from an individual Slack or Teams user. For example, the Approval Request message includes Approve and Reject buttons to take the associated action in ServiceNow.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Notifications in messaging applications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure message content

Create a message in the Message Contents \[messaging\_content\] table that you can use in multiple notifications. Messages can be informative, or they can request action from an individual Slack or Teams user. For example, the Approval Request message includes Approve and Reject buttons to take the associated action in ServiceNow.

## Before you begin

Role required: admin or messaging\_admin

## About this task

To enable users to take actions in Slack or Teams, use the Buttons message type and define scripted behavior. Only users that have linked their Slack or Teams account with their ServiceNow account can take action in ServiceNow from the third-party application.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Messaging Content**.

2.  Open an existing notification record or click **New** to create a new record.

3.  Fill in or modify the fields as appropriate.

<table id="table_ywj_n2t_pdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the message.

</td></tr><tr><td>

Type

</td><td>

Select a type of message. -   **Simple**: Send an informative message to an entire Team or Slack channel.
-   **Buttons**: Send a message to an individual user in Slack or Teams and define the desired behavior in the **Script** field. Associate buttons in the message with actions in ServiceNow. Use the Approval Request as an example.


</td></tr><tr><td>

Target table

</td><td>

To use record content in your message, select the appropriate table. **Note:** Notifications running on the Task \[task\] table are not supported. Instead, use a table extended from task.

</td></tr><tr><td>

Fields

</td><td>

Select which fields from the **Target table** appear in a simple message. Changing the order of the fields changes the display order in the notification.

</td></tr><tr><td>

Message heading

</td><td>

Enter text to appear at the top of the message.

</td></tr><tr><td>

Message

</td><td>

Enter the content of the message. Use notification variables to include dynamic information in your message. For example, use `Incident ${number}` to include the incident number in the message. For available variables, see [Notification variables](../concept/notification-variables.md).

</td></tr><tr><td>

Buttons

</td><td>

Select or create buttons to use on the form. After selecting or creating a button, you must define button behavior in the **Script** field.

 Only visible when Buttons is selected in the **Type** field

</td></tr><tr><td>

Script

</td><td>

This field is only visible when Buttons is selected in the **Type** field.

 Enter a script to define what happens in your instance when a user selects a button in Slack or Microsoft Teams. Use the `actions.get` method to return the name of the button selected by the user.

 ```
if (actions.get('button') == 'Approve') {
		target.state = 'approved';
		target.update();
	}
```

 In this example, the script conditionally executes when the "Approve" button is selected.

 Use the method `sn_notification.Messaging.send` to send information to the messaging window.

 ```
var content = new GlideRecord("messaging_content");
content.get("1bb10839572213007f004758ef94f9c4"));
sn_notification.Messaging.send(application, userId, content, target);
```

 In this example, the script stores a Message Content record in the `content` variable. It then posts a message from that Message Content record.

</td></tr><tr><td>

Application

</td><td>

Select the application scope for this notification.

</td></tr></tbody>
</table>4.  Click **Submit**


## Example

This example shows the output of a message in Microsoft Teams. This message is of the buttons type, which shows buttons and performs scripted actions based on the user selection. In this case, the script uses the `sn_notification.Messaging.send`method to display the change in state for the record.

![Buttons type message](../../virtual-agent/images/va-response-example.png)

## What to do next

Use the message in a notification. For more information about creating notifications, see [Create a messaging notification](create-messaging-notification.md).

**Parent Topic:**[Notifications in messaging applications](../concept/messaging-integration.md)

