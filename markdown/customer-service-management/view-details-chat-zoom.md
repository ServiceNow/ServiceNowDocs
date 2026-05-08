---
title: View details for Zoom meetings initiated from chats
description: View details for a Zoom meeting initiated from a chat by accessing the associated interaction record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Chat Zoom Connector, Manage cases, Use, Customer Service Management]
---

# View details for Zoom meetings initiated from chats

View details for a Zoom meeting initiated from a chat by accessing the associated interaction record.

## Before you begin

Role required: sn\_customerservice\_manager

## About this task

This task provides steps for a user with the sn\_customerservice\_manager role to access Zoom meeting details from an interaction record. For information about how users with other Notify roles view Zoom meeting details, see [Using Chat Zoom Connector](../concept/using-chat-zoom-connector.md).

## Procedure

1.  Navigate to **Interaction** &gt; **All**.

2.  In the Interactions list, click the link to an interaction record of type Zoom from the **Number** column.


## Result

The recording URL of the Zoom meeting, if available, is added as a work note and displayed in the activity stream of the Interaction form.

On the Interaction form, you can view the details for a Zoom meeting.

**Note:** Your administrator might have configured the interaction record to show different application-specific field values.

<table id="table_m3g_pjy_jdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number to identify the interaction record.

</td></tr><tr><td>

Type

</td><td>

Type of channel communication. For a Zoom meeting, the field is automatically set to **Zoom**.

</td></tr><tr><td>

State

</td><td>

Different states through which the interaction proceeds for a resolution.

</td></tr><tr><td>

Opened for

</td><td>

Customer contact or consumer for whom the Zoom meeting was initiated. This field is automatically set to the **Opened for** field value from the chat interaction record from which the Zoom meeting was initiated.

</td></tr><tr><td>

Assigned to

</td><td>

Agent the interaction record is assigned to. This field is automatically set to the **Assigned to** field value from the chat interaction record from which the Zoom meeting was initiated.

</td></tr><tr><td>

Parent

</td><td>

Number of the chat interaction record from which this Zoom meeting was initiated. This field is automatically set to the number of the chat interaction record.

 You may need to configure the form to add this field. For more information, see Configure the form layout.

</td></tr><tr><td>

Channel Metadata Record

</td><td>

Number of the Notify conference call. This field is automatically set to a conference call number associated with this meeting and stored in the Notify Conference Calls \[notify\_conference\_call\] table.

 **Note:** To view more details such as the meeting URL and participant details, click the preview this record icon \(![Preview this record icon.](../image/preview-record.png)\) for this field.

 You may need to configure the form to add this field. For more information, see Configure the form layout.

</td></tr><tr><td>

Channel Metadata Table

</td><td>

Table containing a list of conference calls started using Notify. This field is automatically set to **Notify Conference Calls \[notify\_conference\_call\]**.

 You may need to configure the form to add this field. For more information, see Configure the form layout.

</td></tr><tr><td>

Consumer

</td><td>

Consumer’s account automatically set to the **Consumer** field value from the chat interaction record from which the Zoom meeting was initiated. You may need to configure the form to add this field. For more information, see Configure the form layout.

</td></tr><tr><td>

Contact

</td><td>

Customer contact automatically set to the **Contact** field value from the chat interaction record from which the Zoom meeting was initiated. You may need to configure the form to add this field. For more information, see Configure the form layout.

</td></tr><tr><td>

Account

</td><td>

User's account automatically set to the **Account** field value from the chat interaction record from which the Zoom meeting was initiated. You may need to configure the form to add this field. For more information, see Configure the form layout.

</td></tr><tr><td>

Short Description

</td><td>

Short description of the interaction. **Note:** The short description field is empty for a Zoom meeting.

</td></tr></tbody>
</table>**Related topics**  


[Initiate Zoom meetings from chats](initiate-chat-zoom.md)

