---
title: Apply domain separation on dot walked fields \[Updated in Security Center 1.3, 1.5, and 2.0\]
description: The glide.sys.domain.include\_domain\_condition\_on\_join property controls whether join queries are given domain separated conditions or not in order to ensure they apply domain separation functionality for dot walked fields.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Apply domain separation on dot walked fields \[Updated in Security Center 1.3, 1.5, and 2.0\]

The **glide.sys.domain.include\_domain\_condition\_on\_join** property controls whether join queries are given domain separated conditions or not in order to ensure they apply domain separation functionality for dot walked fields.

This property controls whether join queries are given domain separated conditions or not, in order to ensure they apply domain separation functionality for dot walked fields. If **glide.sys.domain.include\_domain\_condition\_on\_join** is not set to the recommended value of true on an instance using domain separation, then sensitive information could be disclosed that is not to be shared with a specific domain. There may be moderate functional impact to the instance if components are reliant on the unsafe cross domain queries. Instances should be tested in subproduction environments before enabling.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.sys.domain.include\_domain\_condition\_on\_join**

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

True, when domain separation is installed, otherwise the property won't exist.

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

Controls whether join queries are given domain separated conditions or not, in order to ensure they apply domain separation functionality for dot walked fields.

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS score: Medium
-   Security risk details: If **glide.sys.domain.include\_domain\_condition\_on\_join** is not set to the recommended value of **true**, then sensitive information could be disclosed that is not to be shared with a specific domain.

</td></tr><tr><td>

References

</td><td>

[Domain separation for service providers](../../company-and-domain-separation/reference/domain-sep-landing-page.md)

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

