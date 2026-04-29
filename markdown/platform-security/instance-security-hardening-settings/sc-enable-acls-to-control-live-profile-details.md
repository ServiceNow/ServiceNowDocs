---
title: Enable ACLs to Control Live Profile Details
description: Use the glide.live\_profile.details property to designate whether a user should be able to view all detail fields, such as company name and phone numbers, in a live profile.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable ACLs to Control Live Profile Details

Use the **glide.live\_profile.details** property to designate whether a user should be able to view all detail fields, such as company name and phone numbers, in a live profile.

Use the **glide.live\_profile.details** system property to designate whether a user should be able to view all detail fields, such as company name and phone numbers, in a live profile under the live feed feature.

If **glide.live\_profile.details** is set to the value of `hide`, then no live profile information is visible to user. If it is set to `show`, all information is visible. When **glide.live\_profile.details** is set to the value of `ACL`, information is visible based on the user's profile ACLs.

Ensure the property **glide.live\_profile.details** is set to `ACL`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.live\_profile.details**

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

ACL

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

ACL

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS rating: Medium
-   Security risk details: Exposing sensitive user information such as company affiliation and contact details to unauthorized users increases the risk of data leakage and violating privacy controls if ACLs are not enforced.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

