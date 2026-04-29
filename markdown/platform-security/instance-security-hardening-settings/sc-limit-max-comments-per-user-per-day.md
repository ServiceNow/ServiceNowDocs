---
title: Limit max comments per user per day
description: Configure the sn\_kb\_social\_qa.max\_comments\_per\_user\_daily property to restrict the number of QA comments per day.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business Logic, Hardening settings, Platform Security]
---

# Limit max comments per user per day

Configure the **sn\_kb\_social\_qa.max\_comments\_per\_user\_daily** property to restrict the number of QA comments per day.

If the **sn\_kb\_social\_qa.max\_comments\_per\_user\_daily** system property is not set to the recommended value of `500` or less, then there will be no restriction on number of QA comments per day.

Ensure that the property **sn\_kb\_social\_qa.max\_comments\_per\_user\_daily** is set to `500` or less.

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

String

</td></tr><tr><td>

Recommended value

</td><td>

500

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

500

</td></tr><tr><td>

Category

</td><td>

 

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS rating: Low
-   Security risk details: Too many comments could lead to resource exhaustion.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Business Logic](sc-business-logic.md)

