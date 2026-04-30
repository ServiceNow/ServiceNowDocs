---
title: Limit max comments per user per day
description: Configure the sn\_kb\_social\_qa.max\_comments\_per\_user\_daily property to restrict the number of QA comments per day.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Business Logic, Hardening settings, Platform Security]
---

# Limit max comments per user per day

Configure the **sn\_kb\_social\_qa.max\_comments\_per\_user\_daily** property to restrict the number of QA comments per day.

If this property is not set to the recommended value of **500** or less, there is no restriction on the number of QA comments per day which could lead to resource exhaustion.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_kb\_social\_qa.max\_comments\_per\_user\_daily**

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
-   Security risk details: Not setting the recommended value of this property to 500 or less places no limit on QA comments per day which could lead to resource exhaustion.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Business Logic](sc-business-logic.md)

