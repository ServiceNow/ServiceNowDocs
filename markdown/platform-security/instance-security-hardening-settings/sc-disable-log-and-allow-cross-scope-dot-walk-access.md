---
title: Disable log-and-allow mode for cross-scope dot-walk access
description: The glide.script.dot\_walk.log\_and\_allow\_violations property controls logging and enforcement of access violations when dot-walk is used cross-scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-disable-log-and-allow-cross-scope-dot-walk-access.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [dot-walk, cross-scope, access control, security]
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Disable log-and-allow mode for cross-scope dot-walk access

The **glide.script.dot\_walk.log\_and\_allow\_violations** property controls logging and enforcement of access violations when dot-walk is used cross-scope.

This property determines whether access violations are logged when dot-walk is used to access table data cross-scope. When enabled, this property logs violations without preventing cross-scope table access through dot-walk.

When set to `true`, access violations are logged but not enforced. When set to `false`, logging is turned off and enforcement is controlled by the **glide.script.dot\_walk.enforce\_cross\_scope\_access\_all\_tables** property.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the instance.
2.  Confirm the **glide.script.dot\_walk.log\_and\_allow\_violations** property doesn't exist in the sys\_properties table or is set to `false`.

## More information

<table id="table_property_details-allow-enforcement-cross-scope-table-access"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.script.dot\_walk.log\_and\_allow\_violations**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

true \| false

</td></tr><tr><td>

Recommended value

</td><td>

false

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

-   Severity score: 6.4
-   CVSS rating: Medium
-   Security risk details: When this property is set to `true`, authorization checks aren't performed for dot-walk occurring cross-scope. Without authorization checks, dot-walk can be used by an application to access tables that are outside the application scope, potentially exposing sensitive data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

When set to `true`, this property supersedes the **glide.script.dot\_walk.enforce\_cross\_scope\_access\_all\_tables** property. No enforcement of access control for cross-scope dot-walk occurs, regardless of the other property value. When set to `false`, enforcement for cross-scope access control when using dot-walk is controlled by the **glide.script.dot\_walk.enforce\_cross\_scope\_access\_all\_tables** property.

</td></tr><tr><td>

Functional impact

</td><td>

When set to `true`, this property logs access violations, but does not enforce access control for cross-scope dot-walk, similar to the behavior of prior releases. When set to `false`, logging is turned off, and enforcement is controlled by the **glide.script.dot\_walk.enforce\_cross\_scope\_access\_all\_tables** property. There is no functional impact on application behavior when toggling this property.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

