---
title: Enforce secure referrer policy
description: Use the com.glide.security.referrerpolicy property to ensure that the Referrer-Policy HTTP header sends the appropriate level of data to each ServiceNow page to help prevent data leaks.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Enforce secure referrer policy

Use the **com.glide.security.referrerpolicy** property to ensure that the Referrer-Policy HTTP header sends the appropriate level of data to each ServiceNow® page to help prevent data leaks.

Use the **com.glide.security.referrerpolicy** system property to control what information is included in the referrer HTTP header across the Now Platform. The data included in the referrer header, according to the policy of this property, is the origin, path, and query strings of the full referrer URL. These values are the standardized Referrer-Policy values supported by the HTTP protocol with the addition of the value "default." Depending on the policy set by this property, the referrer header may include sensitive information about or from the entity making the request.

Ensure that the **com.glide.security.referrerpolicy** system property is set to one of the following: `default`, `same-origin`, `origin-when-cross-origin`, or `strict-origin-when-cross-origin`.

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

String

</td></tr><tr><td>

Recommended value

</td><td>

default

</td></tr><tr><td>

Default value

</td><td>

default

</td></tr><tr><td>

Fallback value

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
-   Security risk details: When the **com.glide.security.referrerpolicy** system property is set to `no-referrer-when-downgrade` or `unsafe-url`, the referrer header of a request to a site different to the origin includes the full URL for the referring page making the request. The full referrer URL shared with external sites may include sensitive information from or about your instance. This can lead to data leakage and privacy violations.

When the property is set to `no-referrer`, `origin`, or `strict-origin`, the referrer header is either not included, or includes only the origin portion of the referrer URL when requests are sent to the origin. This change may impede efforts to trace attack paths in the logs when a security incident occurs, as the exact origin of a request can’t be determined easily. Proper configuration of this property is essential to help prevent unauthorized disclosure of internal identifiers or confidential parameters while allowing for security incident investigations.


</td></tr><tr><td>

Functional impact

</td><td>

When the **com.glide.security.referrerpolicy** system property is set to `no-referrer`, `origin`, or `strict-origin`, the referrer header is either not be included, or includes only the origin portion of the referrer URL when requests are sent to the origin. This change can break functionality that requires this data.

 Some sites like YouTube require embedded link requests to include at least the origin in the referrer header \(for example, the "origin-when-cross-origin" policy\). The appropriate value of this property is dependent on the instance owner and use case. Those we recommend are described here. These policies are secure and don’t break base system functionality. More information of these and the other standardized policies can be found at [https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Referrer-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Referrer-Policy).

 -   `default`: Functionally equal to setting the value to `same-origin`
-   `same-origin`: Sends the origin, path, and query string for same-origin requests. Doesn't send the referrer header for cross-origin requests.
-   `origin-when-cross-origin`: When performing a same-origin request, sends the origin, path, and query string. Sends only the origin for cross-origin requests and requests to less secure destinations \(from HTTPS to HTTP\).
-   `strict-origin-when-cross-origin`: Sends the origin, path, and query string when performing a same-origin request. For cross-origin requests, sends the origin only when the protocol security level stays same \(from HTTPS to HTTPS\). Doesn't send the referrer header to less secure destinations \(from HTTPS to HTTP\).

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Referrer-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy)

</td></tr></tbody>
</table>**Parent Topic:**[Configuration](sc-configuration.md)

