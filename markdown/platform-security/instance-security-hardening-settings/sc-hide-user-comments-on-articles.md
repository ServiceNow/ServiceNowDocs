---
title: Hide user comments on articles \[New in Security Center 1.3\]
description: Use the glide.knowman.show\_user\_feedback property to control whether feedback comments are visible.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Hide user comments on articles \[New in Security Center 1.3\]

Use the **glide.knowman.show\_user\_feedback** property to control whether feedback comments are visible.

When **glide.knowman.show\_user\_feedback** is not set to never, feedback comments will be visible on knowledge base \(KB\) articles to users with roles defined in the Glide property, **glide.knowman.show\_user\_feedback.roles**. As feedback comments may contain sensitive information, you may not want the feedback to be visible. If this property is not set to never, there could be confidentiality impacts if sensitive information is disclosed in feedback.

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
-   Security risk details: Not setting this property to never could lead to sensitive information being disclosed in feedback comments.

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

