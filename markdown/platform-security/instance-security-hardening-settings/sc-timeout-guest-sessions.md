---
title: Timeout Guest Sessions
description: Use a system property to control the inactive session timeout for unauthenticated users.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Business Logic, Hardening settings, Platform Security]
---

# Timeout Guest Sessions

Use a system property to control the inactive session timeout for unauthenticated users.

Use the **glide.guest.session\_timeout** system property to set the inactive session timeout duration \(in minutes\) for unauthenticated users. Raise the value of this property to extend the time your instance persists sessions beyond the default of 30 minutes. Avoid large timeout values, which can increase the number of sessions persisted by the instance, and cause minor availability concerns.

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
-   Security risk details: Large timeout values can increase the number of concurrent sessions on your instance, causing minor availability concerns.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Business Logic](sc-business-logic.md)

