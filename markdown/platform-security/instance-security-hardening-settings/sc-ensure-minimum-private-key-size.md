---
title: Ensure minimum private key size
description: Use a system property to determine the minimum size of the private key used for Certificate Signing Request \(CSR\) generation with the Certificate Inventory Management application.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Ensure minimum private key size

Use a system property to determine the minimum size of the private key used for Certificate Signing Request \(CSR\) generation with the Certificate Inventory Management application.

The **sn\_disco\_certmgmt.private\_key\_size** system property determines the minimum size of the private key used for CSR generation with the Certificate Inventory Management application. Valid choices are 512, 1024, 2048, or 4096.

Verify that this property is set to a value of 2048 or higher. Valid choices for this property are 512, 1024, 2048, or 4096. If the property doesn’t exist in the System Properties \[sys\_properties\] table, or the value is invalid, the value is 2048 by default.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_disco\_certmgmt.private\_key\_size**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Integer, representing the size of the private key generated. Use values of 512, 1024, 2048, or 4096.

</td></tr><tr><td>

Recommended value

</td><td>

2048

</td></tr><tr><td>

Default value

</td><td>

2048

</td></tr><tr><td>

Fallback value

</td><td>

2048

</td></tr><tr><td>

Category

</td><td>

[Communications](sc-communications.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.1
-   CVSS score: Low
-   Security Risk: Using keys smaller than 2048 can result in future information disclosure in the event the key is brute forced. Use a valid value greater than or equal to 2048 to future proof the key for a longer time period.

</td></tr><tr><td>

Functional impact

</td><td>

Legacy systems and applications may not handle keys greater than or equal to 2048.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Configuration](sc-configuration.md)

