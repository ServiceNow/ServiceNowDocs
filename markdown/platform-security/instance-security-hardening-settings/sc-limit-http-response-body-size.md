---
title: Limit HTTP response body size \[New in Security Center 1.3 and updated in 1.5\]
description: Configure the glide.http.response.get\_body.limit.enabled and glide.http.response.get\_body.limit properties to protect your instance against OutOfMemoryExceptions.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Limit HTTP response body size \[New in Security Center 1.3 and updated in 1.5\]

Configure the **glide.http.response.get\_body.limit.enabled** and **glide.http.response.get\_body.limit** properties to protect your instance against OutOfMemoryExceptions.

Prevent `OutOfMemoryExceptions` that can result from a request response body being too large using the **glide.http.response.get\_body.limit.enabled** and **glide.http.response.get\_body.limit** system properties. These exceptions can cause denial of service \(DOS\) attacks as well as other issues that may aid attackers in compromising an instance. Not setting these properties to the recommended values could make your instance vulnerable to OutOfMemoryExceptions and denial of service attacks.

To protect your instance against these security vulnerabilities:

-   Set the **glide.http.response.get\_body.limit.enabled** system property to **true**.
-   Ensure that the **glide.http.response.get\_body.limit** system property set to no more than 524,288,000 megabytes \(500 MB\).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.http.response.get\_body.limit.enabled**
-   **glide.http.response.get\_body.limit**

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

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.1
-   Security risk details: Not setting these properties to the recommended values could make your instance vulnerable to OutOfMemoryExceptions and denial of service attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property reduces the chances of an OutOfMemoryException due to a customer accidentally loading a large file into memory.

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

