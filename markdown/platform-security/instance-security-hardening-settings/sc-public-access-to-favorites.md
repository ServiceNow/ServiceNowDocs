---
title: Disable public access to favorites
description: Use the glide.ui.magellan.favorites.allow\_public to specify whether unauthenticated users are allowed to see Favorites in the navigator.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Disable public access to favorites

Use the **glide.ui.magellan.favorites.allow\_public** to specify whether unauthenticated users are allowed to see **Favorites** in the navigator.

If the **glide.ui.magellan.favorites.allow\_public** system property is not set to the recommended value of **false**, then all unauthenticated users can access favorites of the same "Guest" user in the navigator.

Ensure the property **glide.ui.magellan.favorites.allow\_public** is set to "**false**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.magellan.favorites.allow\_public**

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

false

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

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS rating: Medium
-   Security risk details: Unauthenticated users are allowed to access and potentially manipulate the Favorites of the shared "Guest" user, increasing the risk of unauthorized UI customization, data exposure, and user interface misuse.

</td></tr><tr><td>

Functional impact

</td><td>

Enabling this property acts as a layer of protection from unauthorized users.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

