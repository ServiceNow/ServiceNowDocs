---
title: Configure inbound authentication for the async callback
description: Set up the API-key authentication profile, access policy, role, and service account that secure the async callback endpoint.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplyon-configure-inbound-auth.html
release: zurich
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 1
breadcrumb: [Configuring the Supplyon integration, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure inbound authentication for the async callback

Set up the API-key authentication profile, access policy, role, and service account that secure the async callback endpoint.

## Before you begin

Role required: admin

## About this task

The async callback endpoint requires authentication. An API-key inbound authentication profile secures it, bound to the endpoint through a REST API Access Policy. A role gates access further — the calling account must hold that role. There is no shared-secret header.

The authentication chain is as follows:

1.  API key in the x-sn-apikey header: SupplyOn presents its API key in the `x-sn-apikey` header \(the default ServiceNow API-key header\). This credential identifies the caller.
2.  API-key authentication profile: An inbound authentication profile of type HTTP Authentication Profile Using API Key \(named SupplyOn, in scope `sn_supplyon_po`\) reads the key from `x-sn-apikey`. It then resolves the key to the user that the key belongs to.
3.  REST API Access Policy binds the profile to the endpoint: A REST API Access Policy targets the callback flow API \(api\_path `sn_supplyon_po/supplyon_outbound_po_async_callback`\) and maps it to the SupplyOn API-key profile. The flow security scheme requires authentication and enables external access.
4.  Endpoint ACL requires the integration-user role: An endpoint ACL requires the `sn_supplyon_po.integration_user` role, so the user that the API key resolves to must also carry this role to invoke the endpoint.
5.  Role is assigned to a dedicated service account: `sn_supplyon_po.integration_user` is assigned only to the dedicated SupplyOn integration service account, never to a human account.

The authentication profile, access policy, security scheme, ACL, and role ship with the application. The API key value is runtime data issued to the service account and must not be committed to source.

## Procedure

1.  Confirm the dedicated integration service account exists and holds the sn\_supplyon\_po.integration\_user role.

2.  In the API Keys module, create an API key attached to the service account, and record its value.

3.  Confirm that SupplyOn sends the key in the `x-sn-apikey` header.

4.  Provide the endpoint URL and issued key to SupplyOn for portal registration.


## What to do next

**Note:**

-   The integration\_user role also includes the procurement integrator role, which is required to create the inbound purchase order confirmation records.
-   The callback subflow runs as system for the staging writes, so the integration-user role is the authentication boundary between SupplyOn and ServiceNow and is kept deliberately narrow.

