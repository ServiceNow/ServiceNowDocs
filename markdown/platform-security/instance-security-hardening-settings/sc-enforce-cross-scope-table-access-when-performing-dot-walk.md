---
title: Enforce cross-scope table access when performing dot-walk
description: The glide.script.dot\_walk.enforce\_cross\_scope\_access\_all\_tables property defines the base access control decision for all table data accessed through dot-walk when the access is cross-scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-cross-scope-table-access-when-performing-dot-walk.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [dot-walk, cross-scope, access control, security]
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce cross-scope table access when performing dot-walk

The **glide.script.dot\_walk.enforce\_cross\_scope\_access\_all\_tables** property defines the base access control decision for all table data accessed through dot-walk when the access is cross-scope.

This property controls whether authorization checks are performed for all table data accesses that are cross-scope through dot-walk. When set to `true`, authorization checks are performed for all cross-scope table data accesses unless a table has explicitly set the **enforce\_dot\_walk\_cross\_scope\_access** dictionary attribute to `false`.

When set to `false`, no authorization checks are performed for cross-scope table data accesses unless a table has explicitly set the **enforce\_dot\_walk\_cross\_scope\_access** dictionary attribute to `true`.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Set the **glide.script.dot\_walk.enforce\_cross\_scope\_access\_all\_tables** property to `true`.

## More information

<table id="table_property_details-enforce-cross-scope-table-access"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.script.dot\_walk.enforce\_cross\_scope\_access\_all\_tables**

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

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

Access Control

</td></tr><tr><td>

Security risk

</td><td>

-   Security risk rating: Medium
-   Security score: 6.4
-   Security risk details: When this property is set to `false`, no authorization checks are performed for cross-scope table data accesses unless a table has explicitly set the **enforce\_dot\_walk\_cross\_scope\_access** dictionary attribute to `true`.

Without authorization checks, dot-walk can be used by an application to access tables that are outside the application scope, potentially exposing sensitive data.


</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

When the **glide.script.dot\_walk.log\_and\_allow\_violations** property is set to `true`, it supersedes this property. No enforcement of access control for cross-scope dot-walk occurs, regardless of this property value. The enforcement for cross-scope access control when using dot-walk is controlled by this property when **glide.script.dot\_walk.log\_and\_allow\_violations** is set to `false`.

</td></tr><tr><td>

Functional impact

</td><td>

When set to `true`, authorization checks are performed for all cross-scope table data accesses unless a table has explicitly set the **enforce\_dot\_walk\_cross\_scope\_access** dictionary attribute to `false`. Because dot-walk access control was not enforced cross-scope before the Zurich release, this may cause some applications to not function correctly if they attempt to access tables outside of their scope through dot-walk.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

