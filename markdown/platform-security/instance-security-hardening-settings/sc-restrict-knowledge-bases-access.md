---
title: Restrict knowledge bases access
description: The glide.knowman.block\_access\_with\_no\_user\_criteria property is used to control the read/write access of users on knowledge based articles.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict knowledge bases access

The **glide.knowman.block\_access\_with\_no\_user\_criteria** property is used to control the read/write access of users on knowledge based articles.

The **glide.knowman.block\_access\_with\_no\_user\_criteria** system property is used in knowledge record user criteria security. If **glide.knowman.block\_access\_with\_no\_user\_criteria** isn't set to the recommended value of **true**, then knowledge bases without can read or can contribute user criteria become readable and writable by all users.

Ensure the property **glide.knowman.block\_access\_with\_no\_user\_criteria** is set to **true**.

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

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

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
-   Security risk details: Knowledge bases lacking explicit "can read" or "can contribute" user criteria may become accessible and editable by all users, potentially leading to unauthorized access and modification of sensitive knowledge content.

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

