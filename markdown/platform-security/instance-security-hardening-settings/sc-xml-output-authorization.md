---
title: Require authorization for XML output requests \[Updated in Security Center 1.3\]
description: Configure this property so that basic authorization is required for all inbound XMLOutputProcessor requests.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for XML output requests \[Updated in Security Center 1.3\]

Configure this property so that basic authorization is required for all inbound XMLOutputProcessor requests.

If the **glide.basicauth.required.xmloutputprocessor** property is not set to the recommended value of **true**, then basic authorization is not required for inbound XMLOutputProcessor requests which could lead to unauthenticated information disclosure from the instance.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.basicauth.required.xmloutputprocessor**

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

true

</td></tr><tr><td>

Category

</td><td>

[API and web service](sc-api-web-service.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS score: High
-   Security risk details: Not setting the property to the recommended value of **true** could lead to sensitive information being leaked from the instance.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

