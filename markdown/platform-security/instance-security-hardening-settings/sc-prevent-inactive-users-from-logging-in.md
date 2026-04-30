---
title: Prevent inactive users from logging in \[New in Security Center 1.5\]
description: Configure this property to control if inactive users can authenticate on your instance.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-10-03"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Prevent inactive users from logging in \[New in Security Center 1.5\]

Configure this property to control if inactive users can authenticate on your instance.

When the system property **glide.authenticate.only.allow.active.user.login** is not set to a value of **true**, users in the User \[sys\_user\] table marked inactive can still login to the instance. Users may be marked inactive if they no longer have permission to login \(such as during termination from a company\). If the property is not set to **true**, then these users may still access the instance and any data they could previously access.

Set the **glide.authenticate.only.allow.active.user.login** property value to the recommended value of **true** \(recommended\), to ensures the users in the User \[sys\_user\] table marked inactive cannot log in to the instance and are locked out.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.only.allow.active.user.login**

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

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS score: High
-   Security risk details: Not setting this property to the recommended value of true, could enable inactive users like a terminated employee to still be able to access the instance and any data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

