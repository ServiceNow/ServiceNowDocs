---
title: Allowing locked out users to process inbound email actions
description: A property is available to allow locked out users to trigger inbound actions. For example, enabling the property can allow locked out users to reset their password and send email to the instance asking for assistance.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [References, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Allowing locked out users to process inbound email actions

A property is available to allow locked out users to trigger inbound actions. For example, enabling the property can allow locked out users to reset their password and send email to the instance asking for assistance.

<table id="table_fdd_zpr_n4"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.pop3.process\_locked\_out**

</td><td>

Enables \(true\) or disables \(false\) the ability for locked out users to trigger inbound actions.-   Type: true \| false
-   Default value: false
-   System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>**Warning:** Enabling this property \(**glide.pop3.process\_locked\_out**\) also enables users from untrusted domains to trigger inbound actions. The user must still be active.

**Parent Topic:**[References for Inbound email](../concept/references-inbound-email.md)

