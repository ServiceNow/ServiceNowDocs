---
title: Require write access to access service catalog add item page
description: Use the glide.sc.request.add\_item\_write\_access property to prevent unauthorized operations from being performed on catalog items.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Require write access to access service catalog add item page

Use the **glide.sc.request.add\_item\_write\_access** property to prevent unauthorized operations from being performed on catalog items.

When the **glide.sc.request.add\_item\_write\_access** system property is not set to **true**, any logged in user can access the **Add Catalog Item** UI page. This could result in unauthorized operations performed on catalog items.

Set **glide.sc.request.add\_item\_write\_access** property to **true**.

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
-   Security risk details: This creates a risk of unauthorized modifications or additions to catalog items, potentially leading to service disruption, fraudulent requests, or exposure of sensitive data. Misconfigured access controls in catalog management can undermine system integrity.

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

