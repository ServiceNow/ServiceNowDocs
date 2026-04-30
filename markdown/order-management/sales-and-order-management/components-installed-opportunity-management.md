---
title: Components installed with Opportunity Management
description: Several types of components are installed with activation of the Opportunity Management plugin, including user roles.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Lead and opportunity management, Reference, Sales Customer Relationship Management]
---

# Components installed with Opportunity Management

Several types of components are installed with activation of the Opportunity Management plugin, including user roles.

## Roles installed

<table id="table_nkn_5py_3hc"><thead><tr><th>

Role name

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_opty\_mgmt\_core.opportunity\_viewer

</td><td>

A granular role created to give read access to Opportunity and Opportunity Line Item.

</td><td>

-   sn\_csm\_pricing.pricelist\_viewer
-   sn\_prd\_pm.product\_catalog\_viewer
-   sn\_customerservice.customer\_data\_viewer
-   sn\_opty\_mgmt\_core.opportunity\_setup\_viewer

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_responsibility\_read\_granular

</td><td>

Provides granular read access to opportunity and its related entities through the responsibility framework.

</td><td>

None

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_admin

</td><td>

A granular role created to give CRUD access to Opportunity tables.

</td><td>

-   sn\_opty\_mgmt\_core.opportunity\_setup\_writer
-   sn\_opty\_mgmt\_core.opportunity\_writer

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_responsibility\_write\_granular

</td><td>

Provides granular access to opportunity and related entities through the responsibility framework.

</td><td>

sn\_opty\_mgmt\_core.opportunity\_responsibility\_read\_granular

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_setup\_viewer

</td><td>

Provides read-only access to the Sales cycle and Opportunity stage tables.

</td><td>

None

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_writer

</td><td>

A granular role created to give write access to Opportunity and Opportunity Line Item.

</td><td>

-   sn\_opty\_mgmt\_core.opportunity\_viewer
-   sn\_quote\_mgmt\_core.quote\_writer

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_contributor

</td><td>

Provides limited permissions to FSM/CSM agents to generate opportunities and view their progress across the sales life cycle.

</td><td>

-   sn\_prd\_pm.product\_catalog\_viewer
-   sn\_opty\_mgmt\_core.opportunity\_setup\_viewer
-   sn\_csm\_pricing.pricelist\_viewer
-   sn\_customerservice.customer\_data\_viewer

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_setup\_writer

</td><td>

Provides access to read, create, and write the Sales cycle and Opportunity stage tables.

</td><td>

sn\_opty\_mgmt\_core.opportunity\_setup\_viewer

</td></tr></tbody>
</table>**Parent Topic:**[Lead and opportunity management reference](../concept/reference-lead-opportunity-mgt.md)

