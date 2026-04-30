---
title: Enforce production instance behavior \[Updated in Security Center 1.3 and 1.5\]
description: Configure whether your instance should be handled like a production or non-production instance.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce production instance behavior \[Updated in Security Center 1.3 and 1.5\]

Configure whether your instance should be handled like a production or non-production instance.

If the **glide.installation.production** property is not set to the recommended value of **true**, the instance is not treated as a production instance, therefore permitting zboot and other potentially dangerous scripts to run. Enabling a production instance to be evaluated as a non-production instance can lead to information leakages or Denial of Service \(DoS\) attacks.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.installation.production**

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

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.3
-   CVSS score: Medium
-   Security risk details: Setting this property value to **false** causes the instance to be treated as a non-production instance which enables zboot and other potentially dangerous scripts to run.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

