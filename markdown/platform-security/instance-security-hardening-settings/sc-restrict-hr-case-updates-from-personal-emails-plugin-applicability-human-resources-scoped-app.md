---
title: Restrict HR case updates from personal emails \[New in Security Center 1.3 and updated in 1.5\]
description: Use thesn\_hr\_core.restrict\_guest\_email property to control whether a user can respond back to a HR case with their personal email.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data protection, Hardening settings, Platform Security]
---

# Restrict HR case updates from personal emails \[New in Security Center 1.3and updated in 1.5\]

Use the**sn\_hr\_core.restrict\_guest\_email** property to control whether a user can respond back to a HR case with their personal email.

When the **sn\_hr\_core.restrict\_guest\_email** property is not set to true, a user can send an email from a personal account referencing the HR case to be included in the work notes. This could result in minor confidentiality or integrity issues if the personal email is compromised or communicating insecurely. An admin may want to restrict the ability of users to respond to HR cases from their personal email, since they cannot be confident of the user accessing the personal email account.

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

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Data protection](sc-data-protection.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.5
-   CVSS score: Low
-   Security risk details: Not having this property set to true could result in minor confidentiality or integrity issues if the personal email is compromised or communicating insecurely.

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

