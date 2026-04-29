---
title: Hide user comments on articles
description: Use the glide.knowman.show\_user\_feedback property to control whether feedback comments are visible.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Hide user comments on articles

Use the **glide.knowman.show\_user\_feedback** property to control whether feedback comments are visible.

When the **glide.knowman.show\_user\_feedback** system property isn't set to `never`, feedback comments will be visible on knowledge articles to users with the roles defined in the **glide.knowman.show\_user\_feedback.roles** property. Due to the potentially sensitive information in a feedback comment, an instance admin may not want the feedback to be visible.

Set the property **glide.knowman.show\_user\_feedback.roles** to `never`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.knowman.show\_user\_feedback**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

choicelist

</td></tr><tr><td>

Recommended value

</td><td>

never

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

onload

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.5
-   CVSS score: Low
-   Security risk details: If this property isn't set to `never`, there could be confidentiality impacts if sensitive information is disclosed in feedback.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Shows user comments on KB articles based on choices mentioned in the configuration.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

