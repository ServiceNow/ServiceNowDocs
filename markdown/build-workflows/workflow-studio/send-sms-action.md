---
title: Send SMS action
description: Send an email-based SMS text message to specified users or groups using your instance email server. Recipients must have an SMS device configured to receive the message.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Send SMS action

Send an email-based SMS text message to specified users or groups using your instance email server. Recipients must have an SMS device configured to receive the message.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Deprecation of email-to-text gateway

Email-to-text service is now deprecated and no longer supported by service providers such as AT&amp;T and Verizon. It is recommended to use Notify for sending SMS notifications.

Notify provides support for sending SMS notifications through integration of third-party services, such as Twilio, and requires configuration of supporting workflows. For more information, see [How to setup a SMS email notification in ServiceNow \[KB0712569\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0712569) knowledge base article.

## Fields

<table id="table_mfy_dzy_2lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recipients

</td><td>

Recipients of the SMS text message. Specify a user or group by dragging a pill from the data panel.**Note:** Hard-coded addresses are not supported.

</td></tr><tr><td>

Message

</td><td>

Content of the SMS text message. You can enter text directly or drag a pill from the data panel.

</td></tr></tbody>
</table>## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Recipients**

    Data type: **String**

    Recipients of the SMS text message. Specify a user or group by dragging a pill from the data panel.

-   **Message**

    Data type: **String**

    Content of the SMS text message. You can enter text directly or drag a pill from the data panel.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Email**

    Data type: **Record**

    The Email record created for the SMS message.


## Error messages

|Error|Description|
|-----|-----------|
|`Recipients are required to send SMS`|Appears when no user or group is entered in the recipients field.|
|`Message is required to send SMS`|Appears when no message is entered in the message field.|
|`While parsing the recipients, found hardcoded addresses: %s which were ignored as they are not supported`|Appears when hard-coded address is entered in the recipients field.|
|`While parsing the recipients, no active users or groups were found for sys_id(s): %s`|Appears when one or more inactive users or groups are entered in the recipients field.|
|`No active SMS device was found for users(s) with sys_id(s): %s`|Appears when no SMS device is configured and found for one or more recipients.|
|`Email sending is currently disabled. Please enable it via the property to send SMS using email gateway`|Appears when email sending is disabled.|

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

