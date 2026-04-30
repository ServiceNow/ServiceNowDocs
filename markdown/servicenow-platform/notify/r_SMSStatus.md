---
title: SMS Statuses
description: Every Twilio SMS message request has a status value which describes the current state of the message. Use this information for troubleshooting SMS related incidents/ issues. Here are few descriptions of possible statuses of SMS sent from Notify through Twilio REST API.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Notify with SMS, Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# SMS Statuses

Every Twilio SMS message request has a status value which describes the current state of the message. Use this information for troubleshooting SMS related incidents/ issues. Here are few descriptions of possible statuses of SMS sent from Notify through Twilio REST API.

<table id="table_yv2_51g_xfb"><thead><tr><th align="left">

Status

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

queued

</td><td>

The message has been queued by the provider to be sent to the carrier network.

</td></tr><tr><td>

accepted

</td><td>

The message is being processed by the provider before sending it to the carrier network.

</td></tr><tr><td>

sending

</td><td>

The message is being forwarded to the carrier network.

</td></tr><tr><td>

sent

</td><td>

The message has been successfully forwarded to the carrier network.

</td></tr><tr><td>

receiving

</td><td>

The provider has received an incoming message from the carrier network and is processing it.

</td></tr><tr><td>

received

</td><td>

ServiceNow has received the incoming message from the provider.

</td></tr><tr><td>

delivered

</td><td>

The message has been delivered to the target device.**Note:** A provider may not be able to report this status if the upstream carrier does not report this.

</td></tr><tr><td>

undelivered

</td><td>

The message could not be delivered to the target device.**Note:** A provider may not be able to report this status if the upstream carrier does not report this.

</td></tr><tr><td>

failed

</td><td>

The message failed to be forwarded to the carrier network.

</td></tr><tr><td>

unknown

</td><td>

The driver does not support the status

</td></tr></tbody>
</table>**Parent Topic:**[Using Notify with SMS](../concept/c_NotifySMS.md)

