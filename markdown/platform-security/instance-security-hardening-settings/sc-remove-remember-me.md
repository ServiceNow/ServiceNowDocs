---
title: Remove remember me
description: Use the glide.ui.forgetme property to remove the Remember Me check box from the login page to prevent login information from being cached.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data protection, Hardening settings, Platform Security]
---

# Remove remember me

Use the **glide.ui.forgetme** property to remove the **Remember Me** check box from the login page to prevent login information from being cached.

The **glide.ui.forgetme** system property controls the **Remember Me** check box from the login page to prevent login information from being cached when set to **true**. If the value is set to **false**, caching of authentication information is allowed and the **Remember Me** checkbox is displayed.

Ensure that the property **glide.ui.forgetme** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.forgetme**

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

true

</td></tr><tr><td>

Category

</td><td>

[Data protection](sc-data-protection.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.5
-   CVSS rating: Low
-   Security risk details: This increases the risk of unauthorized access if the device is shared, lost, or compromised, as cached credentials can allow attackers to bypass authentication.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see Add a system property

**Parent Topic:**[Data protection](sc-data-protection.md)

