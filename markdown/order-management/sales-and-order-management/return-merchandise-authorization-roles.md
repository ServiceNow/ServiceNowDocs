---
title: Return Merchandise Authorization roles
description: Information about Return Merchandise Authorization \(RMA\) roles.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Return Merchandise Authorization Case Management, Order operations, Reference, Sales Customer Relationship Management]
---

# Return Merchandise Authorization roles

Information about Return Merchandise Authorization \(RMA\) roles.

|Roles|Description|Contains roles|
|-----|-----------|--------------|
|sn\_csm\_rma\_case.csm\_rma\_case\_creator|This role provides granular access to create RMA cases and RMA case Lines.|sn\_csm\_rma\_case.writer|
|sn\_csm\_rma\_case.csm\_rma\_case\_viewer|This role provides granular access to read RMA cases and RMA case Lines.|None|
|sn\_csm\_rma\_case.csm\_rma\_case\_writer|This role provides granular access to edit or update RMA cases and RMA case Lines.|sn\_csm\_rma\_case.viewer|
|sn\_csm\_rma\_case.csm\_rma\_case\_navigation\_menu|Provides access to RMA Case navigation menus.|None|
|sn\_csm\_rma\_case.csm\_rma\_case\_report\_viewer|Provides Report Viewer access to RMA Case and RMA Case Line.|None|

<table id="table_vmb_bfx_cht"><thead><tr><th>

Roles

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_csm\_rma\_case.agent

</td><td>

Inherit the base case and case task agent roles. User can perform all the CRUD actions.

</td><td>

-   sn\_case\_line.characteristic\_report\_viewer
-   sn\_csm\_rma\_case.csm\_rma\_case\_navigation\_menu
-   sn\_csm\_rma\_case.csm\_rma\_case\_creator
-   sn\_case\_line.characteristic\_delete
-   sn\_customerservice.case\_task\_agent
-   sn\_customerservice\_agent

</td></tr></tbody>
</table>**Parent Topic:**[Return Merchandise Authorization Case Management](return-merchandise-authorization-case-management-reference.md)

