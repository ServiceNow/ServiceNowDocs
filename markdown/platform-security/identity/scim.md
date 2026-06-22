---
title: System for Cross-domain Identity Management \(SCIM\)
description: The System for Cross-domain Identity Management \(SCIM\) API provides endpoints to create, read, update, and delete operations on users and groups using the SCIM protocol.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/identity/scim.html
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Identity]
---

# System for Cross-domain Identity Management \(SCIM\)

The System for Cross-domain Identity Management \(SCIM\) API provides endpoints to create, read, update, and delete operations on users and groups using the SCIM protocol.

<table id="table_qty_rnd_2yb" class="nav-card"><tbody><tr><td>

[SCIM Provider \[Omitted image "bus-explore.svg"\] Alt text: Explore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/identity/scim-provider.md)

 [The SCIM provider synchronizes the changes made to identities in the IdP, including creating, updating, or deleting records.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/identity/scim-provider.md)

</td><td>

[SCIM Client \[Omitted image "bus-learn.svg"\] Alt text: Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/identity/scim-client-app.md)

 [The SCIM Client is used for creating, updating, and deleting identity resources in a system that supports SCIM compliant REST requests.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/identity/scim-client-app.md)

</td></tr></tbody>
</table>The SCIM protocol is an application-level HTTP-based protocol based on the HTTP \([RFC7230](https://datatracker.ietf.org/doc/html/rfc7230)\) standard. Use this API for provisioning and managing identity data, such as users and groups. Use the API on the web and in cross-domain environments, such as enterprise-to-cloud service providers or inter-cloud scenarios.

To access this API, you must activate the SCIM v2 - ServiceNow® Cross-domain Identity Management \(com.snc.integration.scim2\) plugin. To know more about the SCIM API, see [System for Cross-domain Identity Management \(SCIM\) API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/scim-api.md).

