---
title: Prevent unauthenticated roleless ACL in scripted ACLs
description: The glide.security.allow\_unauth\_roleless\_acl property controls whether scripted Access Control Lists \(ACLs\) can grant access to unauthenticated users when the ACL is otherwise roleless.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-prevent-unauthenticated-roleless-acl-in-scripted-acls.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [ACL, access control, unauthenticated, security, roleless]
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Prevent unauthenticated roleless ACL in scripted ACLs

The **glide.security.allow\_unauth\_roleless\_acl** property controls whether scripted Access Control Lists \(ACLs\) can grant access to unauthenticated users when the ACL is otherwise roleless.

When set to `true`, ACLs containing script may grant access to unauthenticated users. Setting this property to `false` prevents unauthenticated users from accessing resources protected by roleless scripted ACLs.

Confirm that the property **glide.security.allow\_unauth\_roleless\_acl** is set to `false`.

## More information

<table id="table_property_details-prevent-unauth-roleless-acl"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.allow\_unauth\_roleless\_acl**

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

`false`

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS rating:High
-   Security risk details: When set to `true`, unauthenticated users unauthenticated users can view, create, or delete information that should be restricted to logged-in users.

</td></tr><tr><td>

Functional impact

</td><td>

When set to `true`, anonymous or guest visitors bypass login for pages, records, or actions. Setting it to `false` keeps the login requirement in place for roleless ACLs.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

