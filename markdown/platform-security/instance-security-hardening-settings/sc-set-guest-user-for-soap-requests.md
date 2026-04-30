---
title: Set guest user for soap requests \[Updated in Security Center 1.3 and 2.0\]
description: Configure this property to control the level of access of unauthenticated SOAP requests.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Set guest user for soap requests \[Updated in Security Center 1.3 and 2.0\]

Configure this property to control the level of access of unauthenticated SOAP requests.

This property controls the level of access of unauthenticated SOAP requests. If it is not set to the recommended value of **soap.guest**, or is set to a user with limited privileges, then SOAP requests will execute on behalf of the user. If this property is blank, then it enables unauthenticated access to administrator or maintenance level operations which negates all security controls within the instance.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.soap.guest\_user**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

soap.guest

</td></tr><tr><td>

Default value

</td><td>

soap.guest

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS score: High
-   Security risk details: Setting this property to blank enables unauthenticated access to administrator or maintenance level operations.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

