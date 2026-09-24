---
title: Enforce least privilege on scoped MCP OAuth tokens
description: The com.snc.platform.security.oauth.mcp.aig\_scope\_support property controls how OAuth access tokens are cached and reused for Model Context Protocol \(MCP\) flows in AI Gateway \(AIG\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-least-privilege-in-scoped-outbound-tokens.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [scoped outbound tokens, OAuth access tokens, Model Context Protocol, AI Gateway, token caching, least privilege]
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce least privilege on scoped MCP OAuth tokens

The **com.snc.platform.security.oauth.mcp.aig\_scope\_support** property controls how OAuth access tokens are cached and reused for Model Context Protocol \(MCP\) flows in AI Gateway \(AIG\).

The MCP OAuth flows cache and reuse outbound access tokens issued on behalf of connected AIG clients. This optimization prevents the requirement to mint a new token for each repeated call to a downstream resource.

When set to `true`, the cache key used to look up a reusable token is computed from the client's requested and baseline configured scopes. Requests carrying different scope combinations resolve to separate cached tokens instead of sharing one. When set to `false`, a single cached token is reused for every request from that client regardless of which scopes were involved when it was created.

To configure this property:

1.  Navigate to `/sys_properties_list.do` on the ServiceNow instance.
2.  Set the **com.snc.platform.security.oauth.mcp.aig\_scope\_support** property to `true`.

## More information

<table id="table_8ui_j45_3ik"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.snc.platform.security.oauth.mcp.aig\_scope\_support**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \( `/sys_properties_list.do`\)

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

false

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS rating: Low
-   Security risk details: It is insecure to reuse a single cached access token across every request from a client, independent of which permissions were involved when that token was created. This approach allows a token issued under one context to be handed out again for an unrelated request. When the original context carried a broader set of permissions, a later, narrower request can still be served the same token. This blurs the boundary between what different requests are authorized to do creating a token confusion risk. A lower-trust or compromised request path can leverage access that was meant to be reachable through a different, more privileged context.

</td></tr><tr><td>

Functional impact

</td><td>

Enabling this control changes outbound-token issuance for MCP OAuth client-credentials and authorization-code flows. Instead of one shared token per user/client, the platform provisions or reuses a distinct outbound token per effective scope combination. This approach increases the number of stored token mappings for clients that vary their requested scopes across calls. Regression test MCP client credentials token issuance, the MCP authorization code flows, and outbound token reuse and expiry behavior for AIG connections.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

