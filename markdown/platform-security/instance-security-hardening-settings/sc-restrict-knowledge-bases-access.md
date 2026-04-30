---
title: Restrict knowledge bases access \[New in Security Center 1.3\]
description: The glide.knowman.block\_access\_with\_no\_user\_criteria property is used to control the read/write access of users on knowledge based articles.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict knowledge bases access \[New in Security Center 1.3\]

The **glide.knowman.block\_access\_with\_no\_user\_criteria** property is used to control the read/write access of users on knowledge based articles.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.knowman.block\_access\_with\_no\_user\_criteria**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 9.1
-   CVSS score: Critical
-   Security risk details: If this property is not set to the recommended value of true, then any user can read and contribute to a KB.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Denies access to a knowledge base when either Can Read or Can Contribute isn't specified.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

