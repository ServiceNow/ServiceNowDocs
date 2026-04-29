---
title: Prevent OAuth Clients from Using Implicit Grant
description: Use a system property to avoid the use of the implicit grant type.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Prevent OAuth Clients from Using Implicit Grant

Use a system property to avoid the use of the implicit grant type.

The OAuth implicit grant was created to overcome a limitation between browsers and client-side applications \(for example, single page applications\) prior to the widespread adoption of Cross Origin Resource Sharing \(CORS\). Specifically, browsers' same-origin policy blocked the request that exchanged the OAuth authorization code with the OAuth access token. Since CORS support is universal, OAuth clients don’t need to use the implicit grant, and implicit grant type requests fail by default.

Client IDs listed in the **glide.oauth.clients.allowed.for.implicit.grant** property can continue using the implicit grant type. Ensure that the property doesn’t exist in the System Properties \[sys\_properties\] table, or exists but doesn’t contain a value.

**Important:** Changing an OAuth client to a different grant type may require code or configuration changes in the client application \(outside of the ServiceNow platform\).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.oauth.clients.allowed.for.implicit.grant**

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

&lt;blank&gt;

</td></tr><tr><td>

Default value

</td><td>

&lt;blank&gt;

</td></tr><tr><td>

Fallback value

</td><td>

&lt;blank&gt;

</td></tr><tr><td>

Category

</td><td>

[API and web service](sc-api-web-service.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.9
-   CVSS score: low
-   Security risk details:

The OAuth implicit grant type causes the authorization server to issue access tokens within the authorization response, making it vulnerable to access token leakage and access token replay. This means that an attacker can use the leaked or stolen access token at a resource endpoint.

In the implicit grant, the authorization server returns an access token directly in the URL fragment, potentially causing problems:

    1.  This URL fragment may be stored in the browser history.
    2.  If the page subsequently loads images, or follows links to other domains, parts of the URL may leak via the referrer header.
    3.  Web servers, load balancers, and proxies may log full URLs.
    4.  Any JavaScript running on the page \(including malicious, injected JS\) can read the `window.location.hash` and extract the token.
To avoid these issues, use the authorization code grant type rather than the implicit grant type when a human/interactive user is delegating authorization to the client.

References

    -   [RFC 9700, "Best Current Practice for OAuth 2.0 Security"](https://datatracker.ietf.org/doc/html/rfc9700#name-implicit-grant)
    -   [draft-ietf-oauth-v2-1-14, "The OAuth 2.1 Authorization Framework"](https://datatracker.ietf.org/doc/html/draft-ietf-oauth-v2-1-14#name-removal-of-the-oauth-20-imp)

</td></tr><tr><td>

Functional impact

</td><td>

The implicit grant type request fails out of the box. Any OAuth clients with the implicit grant type that aren’t added to the property fail by default.

 If you haven't defined any OAuth clients that use the implicit grant type, there is no impact.

 **Note:** Changing an OAuth client to a different grant type may require code or configuration changes in the client application \(outside of the ServiceNow platform\).

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[API and web service](sc-api-web-service.md)

