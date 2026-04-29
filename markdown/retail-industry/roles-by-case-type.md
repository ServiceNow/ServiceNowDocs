---
title: Roles required by retail case type
description: Reference table listing the roles that store associates and managers must hold to create or manage cases of each retail case type.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-31"
reading_time_minutes: 1
breadcrumb: [Assign roles to Retail users, Configure, Retail]
---

# Roles required by retail case type

Reference table listing the roles that store associates and managers must hold to create or manage cases of each retail case type.

Each retail case type requires specific roles to grant requester or fulfiller access. Some roles are included in the default Store Associate and Store Manager role bundles; others must be assigned separately after the initial member setup.

**Note:** The **HQ Communications Case** and **In-Store Operations Case** types do not have associated record producers or service definitions out of the box. Cases of these types can only be created directly by users who hold the required fulfiller roles listed below.

|Case type|Requester role|Fulfiller role|Notes|
|---------|--------------|--------------|-----|
|Retail Customer Complaint|Included in default Store Associate bundle|Included in default Store Manager bundle|Available via record producer and service definition out of the box.|
|Store Inquiry|`sn_rtl_stre_servcs.contributor`|Included in default Store Manager bundle|The `sn_rtl_stre_servcs.contributor` role is NOT included in the default Store Associate role bundle and must be assigned separately.|
|In-Store Operations|Not applicable — no record producer or service definition out of the box|`sn_rtl_instore_ops.manager`|The `sn_rtl_instore_ops.manager` role is NOT included in default role bundles and must be assigned separately to users who need to create or manage In-Store Operations cases.|
|HQ Communications|Not applicable — no record producer or service definition out of the box|Included in default Store Manager bundle|Cases are created by HQ administrators directly or via task plan template generation, not by store users submitting through the portal.|

To assign a supplemental role to a store member after initial setup, see [Assign roles to Retail users](../task/rahi-retail-assign-roles-users.md).

