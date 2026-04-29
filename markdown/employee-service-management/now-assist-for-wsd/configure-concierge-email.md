---
title: Configure the Workplace Concierge email address
description: Configure the email address that is used for the Workplace Concierge.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2026-03-30"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Configure the Workplace Concierge email address

Configure the email address that is used for the Workplace Concierge.

## Before you begin

Role required: admin

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the System Properties list, select the **sn\_wsd\_concierge.concierge\_inbound\_email** system property.

3.  In the **Value** field, enter the email address to be used for the Workplace Concierge.

4.  Save the system property record.


## Result

The Workplace Concierge is configured. Users with the `sn_wsd_core.workplace_user` role can add the email address to a calendar invite or email thread and use the Workplace Concierge to create visits and invite visitors. For more information about using Workplace Concierge, see [Use Workplace Concierge with email or calendar invite](use-concierge-email.md).

