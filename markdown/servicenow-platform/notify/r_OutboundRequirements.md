---
title: Outbound communication requirements
description: Outbound communications initiated through Notify, such as phone calls and SMS messages, must satisfy recipient number requirements.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Notify with SMS, Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Outbound communication requirements

Outbound communications initiated through Notify, such as phone calls and SMS messages, must satisfy recipient number requirements.

## Recipient number requirements

These requirements apply to any number that receives a Notify phone call or message.

-   The number must be E.164 compliant.
-   The number must be different than the phone number used to initiate the call or message.

These requirements apply to all outbound communication initiated through Notify, such as by using Notify workflow activities or the Notify JavaScript API.

Invalid numbers prevent Notify workflows from running and cause an error to be logged. Set the **glide.notify.debug** property to true to create detailed error logs.

**Parent Topic:**[Using Notify with SMS](../concept/c_NotifySMS.md)

