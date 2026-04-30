---
title: Enforce secure referrer policy \[New in Security Center 1.3\]
description: Use the com.glide.security.referrerpolicy property to ensure that the Referrer-Policy HTTP header sends the appropriate level of data to each ServiceNow page to prevent data leaks.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Enforce secure referrer policy \[New in Security Center 1.3\]

Use the **com.glide.security.referrerpolicy** property to ensure that the Referrer-Policy HTTP header sends the appropriate level of data to each ServiceNow® page to prevent data leaks.

When the **com.glide.security.referrerpolicy** property is set to default, it ensures that the Referrer-Policy HTTP header is managed with the appropriate level of information sent, specifically tailored for the ServiceNow AI Platform® request page. This prevents unauthorized data leaks that could be accessible from other parts of the full URL, such as the path and query string.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.security.referrerpolicy**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

default

</td></tr><tr><td>

Default value

</td><td>

default

</td></tr><tr><td>

Category

</td><td>

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: Ensure that the **com.glide.security.referrerpolicy** property is set to default to prevent leaks of unauthorized data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Referrer-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy)

</td></tr><tr><td>

Functional impact

</td><td>

This property controls how much information is sent via the referrer header when a request is sent from a page:-   default: Instance will take care of the referrer headers
-   same-origin: Send full referrer URL within the instance/same domain and no referrer to outside origin
-   origin: Send only the origin as a referrer inside and outside the origin
-   origin-when-cross-origin: Send full referrer URL within the instance/same domain and only the origin outside the origin

</td></tr></tbody>
</table>**Parent Topic:**[Configuration](sc-configuration.md)

