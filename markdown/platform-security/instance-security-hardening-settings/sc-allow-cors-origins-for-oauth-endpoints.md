---
title: Allow CORS Origins for OAuth Endpoints
description: Use a system property to configure to specify which domains are allowed to make cross-origin requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-allow-cors-origins-for-oauth-endpoints.html
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Allow CORS Origins for OAuth Endpoints

Use a system property to configure to specify which domains are allowed to make cross-origin requests.

ServiceNow can function as an OAuth authorization server, a resource server, or both simultaneously. When browser-based applications must access ServiceNow's OAuth endpoints, such as the authorization server metadata, protected resource metadata, or token endpoint, the browser's same-origin policy blocks these cross-origin requests by default. Configure the Access-Control-Allow-Origin header for these endpoints to specify which domains are allowed to make cross-origin requests.

References:

-   [OAuth Authorization Server Metadata RFC](https://datatracker.ietf.org/doc/html/rfc8414)
-   [OAuth Protected Resource Metadata RFC](https://datatracker.ietf.org/doc/html/rfc9728)

When integrating third-party solutions with ServiceNow OAuth functionality, ensure that the **glide.oauth.cors.allowed.origin** system property exists in the System Properties \[sys\_properties\] table, and holds the external domain\(s\) required for Cross Origin Resource Sharing \(CORS\) functionality.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.oauth.cors.allowed.origin**

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

Varies based on use case. This property can one of these values:1.  An empty string
2.  A single hostname
3.  An asterisk \(\*\), which allows all origins to access the OAuth endpoints.

**Tip:** There's no dynamic list for allow-listing multiple hostnames. Use an asterisk\(\*\) to access the OAuth endpoints from multiple domains.

</td></tr><tr><td>

Default value

</td><td>

empty string

</td></tr><tr><td>

Fallback value

</td><td>

empty string

</td></tr><tr><td>

Category

</td><td>

[Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-configuration.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.5
-   CVSS score: Low
-   Security risk details: A third party applications inability to interact with the ServiceNow platform due to browsers' single origin policy may cause a denial of service.

</td></tr><tr><td>

Functional impact

</td><td>

This property can be used to connect MCP clients to the instance when the client exists entirely in the browser, and does not make token or discovery calls via a backend call to the ServiceNow platform.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-configuration.md)

