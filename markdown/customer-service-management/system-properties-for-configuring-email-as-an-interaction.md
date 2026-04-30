---
title: System properties for configuring Email Interaction
description: You can manage certain workflows based on the system properties, such as enabling or disabling the creation of email interactions for guest users. You can set an inactivity period after which email interactions are automatically closed.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Email Interaction for CSM]
breadcrumb: [Email Interaction, Configuring the email channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# System properties for configuring Email Interaction

You can manage certain workflows based on the system properties, such as enabling or disabling the creation of email interactions for guest users. You can set an inactivity period after which email interactions are automatically closed.

Navigate to **All****&gt;System Properties****&gt;All Properties** .

Alternatively, in your instance, enter `sys_properties.list` in the filter navigator and customize the Email Interaction system properties.

<table id="table_qbv_3d4_pwb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_eaai\_csm.create\_interaction\_for\_non\_matched\_user**

</td><td>

Enable or disable interaction creation for a non-matched user.-   Type: Boolean \(true \| false\)
-   Value: true
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr><tr><td>

**sn\_eaai\_csm.period\_of\_customer\_inactivity\_to\_close\_interaction**

</td><td>

Set the inactivity period \(in days\) after which an interaction is closed if no email is received from the customer.-   Type: Integer
-   Value: 5
-   Location: **All****&gt; System Properties****&gt; All Properties**.

</td></tr></tbody>
</table>