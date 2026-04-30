---
title: Limit max subscriptions per user per day
description: Configure the sn\_kb\_social\_qa.max\_subscriptions\_per\_user\_daily property to limit the max number subscriptions a user can subscribe to in a day.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Business Logic, Hardening settings, Platform Security]
---

# Limit max subscriptions per user per day

Configure the **sn\_kb\_social\_qa.max\_subscriptions\_per\_user\_daily** property to limit the max number subscriptions a user can subscribe to in a day.

If this property is not set to the recommended value of **500** or less, there is no restriction on the maximum number of Q&amp;A questions that a user can subscribe to in a day. This no limitation could lead to resource exhaustion and impact the availability of your instance.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_kb\_social\_qa.max\_subscriptions\_per\_user\_daily**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

integer

</td></tr><tr><td>

Recommended value

</td><td>

500

</td></tr><tr><td>

Default value

</td><td>

500

</td></tr><tr><td>

Category

</td><td>

[Business Logic](sc-business-logic.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: Set the property value to 500 or less to prevent resource exhaustion.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Business Logic](sc-business-logic.md)

