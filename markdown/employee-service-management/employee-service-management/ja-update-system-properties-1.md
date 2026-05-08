---
title: Update system properties for Microsoft Exchange Online in the Journey Accelerator app
description: Update the Journey Accelerator app system properties to use with Microsoft Exchange Online features support by Journey Accelerator.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Update system properties for Microsoft Exchange Online in the Journey Accelerator app

Update the Journey Accelerator app system properties to use with Microsoft Exchange Online features support by Journey Accelerator.

## Before you begin

Complete all the steps required for setting up Microsoft Exchange Online Spoke v2.0.2 Microsoft Exchange Online before updating the system properties for the Journey Accelerator app.

See, [Microsoft Exchange Online setup for Journey Accelerator](../concept/ja-ms-exchange-online-setup-1.md) for a list of required spokes supported for different versions of Journey Accelerator.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  Search **Application** for `Journey Accelerator`.

3.  Locate and update the following fields:

    |Name|Value|
    |----|-----|
    |sn\_ja.calendar\_provider\_option|`exchangeOnline`|
    |sn\_ja.ex\_online\_dummy\_account\_id|`<Outlook dummy account for querying meeting times>`|
    |sn\_ja.ex\_online\_service\_account\_id|`<Outlook service account or delegator for calendar management>`|
    |sn\_ja.ex\_online\_notification\_url|`<webhook URL from Microsoft Exchange Online Spoke>`|

    Double-click the **Value** to edit.

    **Note:** When using Microsoft Exchange Online spoke v.2.0.2 with the Retry Handler Framework, the scripted rest API for the retry handler framework is used as the webhook URL.


**Parent Topic:**[Journey Accelerator integrations](../concept/ja-integrations.md)

