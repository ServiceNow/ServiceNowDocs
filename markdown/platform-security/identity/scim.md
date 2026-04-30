---
title: System for Cross-domain Identity Management \(SCIM\)
description: The System for Cross-domain Identity Management \(SCIM\) API provides endpoints to create, read, update, and delete operations on users and groups using the SCIM protocol.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Identity]
---

# System for Cross-domain Identity Management \(SCIM\)

The System for Cross-domain Identity Management \(SCIM\) API provides endpoints to create, read, update, and delete operations on users and groups using the SCIM protocol.

<table id="table_qty_rnd_2yb" class="nav-card"><tbody><tr><td>

[SCIM Provider ![Explore](../../../common/image/icon-explore.png)](scim-provider.md)

 [The SCIM provider synchronizes the changes made to identities in the IdP, including creating, updating, or deleting records.](scim-provider.md)

</td><td>

[SCIM Client ![Reference](../../../common/image/icon-reference.png)](scim-client-app.md)

 [The SCIM Client is used for creating, updating, and deleting identity resources in a system that supports SCIM compliant REST requests.](scim-client-app.md)

</td></tr></tbody>
</table>The SCIM protocol is an application-level HTTP-based protocol based on the HTTP \([RFC7230](https://datatracker.ietf.org/doc/html/rfc7230)\) standard. Use this API for provisioning and managing identity data, such as users and groups. Use the API on the web and in cross-domain environments, such as enterprise-to-cloud service providers or inter-cloud scenarios.

To access this API, you must activate the SCIM v2 - ServiceNow® Cross-domain Identity Management \(com.snc.integration.scim2\) plugin.

To know more about the SCIM API, see [System for Cross-domain Identity Management \(SCIM\) API](https://www.servicenow.com/docs/access?context=scim-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

