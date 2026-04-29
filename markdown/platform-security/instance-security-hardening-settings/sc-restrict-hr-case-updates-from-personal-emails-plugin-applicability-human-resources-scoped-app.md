---
title: Restrict HR case updates from personal emails
description: Use the sn\_hr\_core.restrict\_guest\_email property to control whether a user can respond back to a HR case with their personal email.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data protection, Hardening settings, Platform Security]
---

# Restrict HR case updates from personal emails

Use the **sn\_hr\_core.restrict\_guest\_email** property to control whether a user can respond back to a HR case with their personal email.

When the **sn\_hr\_core.restrict\_guest\_email** system property is not set to **true**, a user can send an email from a personal account referencing the HR case to be included in the worknotes. This could result in minor confidentiality or integrity issues if the personal email is compromised or communicating insecurely. An admin may want to restrict the ability of users to respond to HR cases via their personal email, since they can't be confident of the user accessing the personal email account.

Set the property **sn\_hr\_core.restrict\_guest\_email** to '**true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_hr\_core.restrict\_guest\_email**

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
-   CVSS score: Low
-   This creates a risk of minor confidentiality and integrity issues because personal email accounts may be insecure or compromised, and administrators cannot verify the identity or security posture of those accounts. Allowing this behavior weakens control over sensitive HR communications and increases exposure to data leakage.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property controls whether or not a reply from a personal email address will update an HR Case. Set to true, any reply from personal email will be added to the case notes. If false, the case and notes will not be updated.

</td></tr></tbody>
</table>**Parent Topic:**[Data protection](sc-data-protection.md)

