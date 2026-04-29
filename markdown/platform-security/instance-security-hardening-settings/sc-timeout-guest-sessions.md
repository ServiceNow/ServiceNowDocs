---
title: Timeout Guest Sessions
description: Use a system property to control the inactive session timeout for unauthenticated users.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business Logic, Hardening settings, Platform Security]
---

# Timeout Guest Sessions

Use a system property to control the inactive session timeout for unauthenticated users.

Use the **glide.guest.session\_timeout** system property to control the inactive session timeout for unauthenticated users. By default, the value of this property is 30 minutes. If there are availability concerns from persisting too many sessions in memory, the value of this property can be lowered to 5. Avoid setting this property greater than 30, as large timeout values increase the number of sessions persisted by the instance, and may cause minor availability concerns.

Ensure that the **glide.guest.session\_timeout** system property is configured to the default value of 30. In the rare case there are availability concerns from persisting too many sessions in memory, the value of this property can be lowered to 5.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.guest.session\_timeout**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Integer \(in minutes\)

</td></tr><tr><td>

Recommended value

</td><td>

30

</td></tr><tr><td>

Default value

</td><td>

30

</td></tr><tr><td>

Fallback value

</td><td>

0

</td></tr><tr><td>

Category

</td><td>

[Business Logic](sc-business-logic.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score:4.3
-   CVSS score: Medium
-   Security risk details: Avoid setting this property greater than 30. Large timeout values increase the number of sessions persisted by the instance, and may cause minor availability concerns.

</td></tr><tr><td>

Functional Impact

</td><td>

Small timeout values can result in an undesirable user experience as sessions expire too rapidly. If there are availability concerns from persisting too many sessions in memory, the value of this property can be lowered to 5.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Business Logic](sc-business-logic.md)

