---
title: Restrict access to emails with empty target table
description: Activate the glide.email.email\_with\_no\_target\_visible\_to\_all property to restrict user access to emails, unless they were the one who sent the email or have an admin role.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict access to emails with empty target table

Activate the **glide.email.email\_with\_no\_target\_visible\_to\_all** property to restrict user access to emails, unless they were the one who sent the email or have an admin role.

If the **glide.email.email\_with\_no\_target\_visible\_to\_all** system property isn't set to the recommended value of **false**, then low level users will have access to emails which are not their own.

Ensure that the property **glide.email.email\_with\_no\_target\_visible\_to\_all** is set to **false**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.email.email\_with\_no\_target\_visible\_to\_all**

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

false

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

-   Severity score: 6.5
-   CVSS rating: Medium
-   Security risk details: Emails that lack a specific target record may become visible to all users, resulting in unauthorized access to potentially sensitive communication and violating principles of least privilege and data confidentiality.

</td></tr><tr><td>

Functional impact

</td><td>

Users are no longer able to see emails where target table is empty unless they are an admin or were the sender of the email.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

