---
title: Query range access for TNI tables
description: TNI tables use query range access control lists \(ACLs\) to enforce field-level read access for authenticated users who already have read permission on the table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/query-range-access-for-tni-tables.html
release: brazil
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Configure, Telecommunications Network Inventory]
---

# Query range access for TNI tables

TNI tables use query range access control lists \(ACLs\) to enforce field-level read access for authenticated users who already have read permission on the table.

When a user has read access to a TNI table, query range ACLs automatically grant them access to the associated query range fields. No additional roles are required.

## Query range ACL pattern

TNI uses a two-part ACL pattern to control query range access. A Deny Unless ACL blocks unauthenticated requests, and an Allow If ACL grants access to any authenticated user who already has read permission on the table. This pattern is applied at both the table level and the record level for each TNI table.

|ACL type|Security attribute|Effect|
|--------|------------------|------|
|Deny Unless|UserIsAuthenticated|Blocks unauthenticated users from using query range fields.|
|Allow If|UserIsAuthenticatedAndHasRightsToRead|Grants query range access to any authenticated user who already has read access to the table.|

## Roles that receive query range access

Query range access is derived from existing read roles. No new roles are required.

-   Users with the `sn_ni_core.inventory_agent`, `sn_ni_core.inventory_integrator`, or `sn_ni_core.inventory_template_manager` role automatically receive query range access to TNI tables.
-   For Number Management tables, users with the `sn_inv_num_mgmt.inventory_number_manager` role receive the same access.

**Parent Topic:**[Configuring Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/telecommunications-network-inventory/configuring-telecom-network-inventory.md)

