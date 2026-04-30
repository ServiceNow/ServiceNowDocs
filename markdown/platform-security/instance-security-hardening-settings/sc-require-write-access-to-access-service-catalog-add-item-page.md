---
title: Require write access to access service catalog add item page \[New in Security Center 1.3\]
description: Use the glide.sc.request.add\_item\_write\_access property to prevent unauthorized operations from being performed on catalog items.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Require write access to access service catalog add item page \[New in Security Center 1.3\]

Use the **glide.sc.request.add\_item\_write\_access** property to prevent unauthorized operations from being performed on catalog items.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sc.request.add\_item\_write\_access**

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

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: When the **glide.sc.request.add\_item\_write\_access** property is set to false, any logged in user can access the Add Catalog Item UI page. This could result in unauthorized operations performed on catalog items. To remediate this security risk, set this property to true.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

When the property is true, the user must have write access to the record in the context of the UI page.

</td></tr></tbody>
</table>**Parent Topic:**[Configuration](sc-configuration.md)

