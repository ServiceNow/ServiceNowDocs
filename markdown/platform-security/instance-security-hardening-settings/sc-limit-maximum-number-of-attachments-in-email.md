---
title: Limit maximum number of attachments in email
description: Configure the number of inbound email attachments allowed per Email \[sys\_email\] record on your instance.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-01-22"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Limit maximum number of attachments in email

Configure the number of inbound email attachments allowed per Email \[sys\_email\] record on your instance.

Use the **glide.email.inbound.max\_attachment\_count** system property to control the maximum number of inbound email attachments allowed per Email \[sys\_email\] record on your instance.

Set the value of this property to **30** or less to help avoid instance performance degradation.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.email.inbound.max\_attachment\_count**

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

30 or less

</td></tr><tr><td>

Default value

</td><td>

30

</td></tr><tr><td>

Fallback value

</td><td>

50

</td></tr><tr><td>

Category

</td><td>

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS score: Medium
-   Security risk details: Setting the property value to greater than 30 can lead to degradation issues.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Email properties](https://www.servicenow.com/docs/access?context=c_EmailProperties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

