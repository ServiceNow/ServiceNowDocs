---
title: Set guest user for soap requests
description: Configure this property to control the level of access of unauthenticated SOAP requests.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Set guest user for soap requests

Configure this property to control the level of access of unauthenticated SOAP requests.

Use the **com.glide.soap.guest\_user** system property to control the access level of unauthenticated SOAP requests. If this property isn't set to the recommended value of `soap.guest` or is set to a user with limited privileges, then SOAP requests execute on behalf of this user.

Ensure the property is set to `soap.guest` to ensure an appropriate level of access for unauthenticated SOAP requests.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

****

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

soap.guest

</td></tr><tr><td>

Default value

</td><td>

soap.guest

</td></tr><tr><td>

Fallback value

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
-   Security risk details: Unauthenticated SOAP requests can allow unauthorized access if not properly restricted. Evaluating these requests against a minimally privileged user helps reduce the risk of exposing sensitive operations. Failure to enforce this control may result in elevated access and compromise system integrity.

</td></tr><tr><td>

Functional impact

</td><td>

SOAP requests are restricted to the permissions of the soap.guest user. If an integration relies on a resource that does not have the appropriate ACLs for soap.guest, those requests will result in permission denials.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

