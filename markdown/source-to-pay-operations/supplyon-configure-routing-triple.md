---
title: Configure the routing triple and payload properties
description: Set the organization code, plant code, and payload constant system properties that identify the buyer tenant in SupplyOn.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplyon-configure-routing-triple.html
release: australia
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 1
breadcrumb: [Configuring the Supplyon integration, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure the routing triple and payload properties

Set the organization code, plant code, and payload constant system properties that identify the buyer tenant in SupplyOn.

## Before you begin

Role required: admin

## About this task

The routing triple identifies the buyer tenant in SupplyOn. Resolve each element as follows.

|Element|Value|Source|
|-------|-----|------|
|OrgCode|The org\_code\_override property if set, otherwise plus the app creator company code.|System property or app creator company code.|
|PlantCode|The sn\_supplyon\_po.plant\_code property if set, otherwise the same plus company code base.|System property.|
|SupplierNumber|`sn_fin_supplier.number` \(the ServiceNow SUP... number\).|Resolved from the outbound header supplier\_id. Not `erp_company_code`.|

The following system properties carry payload constants and routing values: **edi\_sender** \(default `SERVICENOW`\), **erp\_system\_id**, **order\_type** \(`NB`, for standard orders\), **header\_note**, **plant\_code**, and **org\_code\_override**.

## Procedure

1.  If the SupplyOn organization differs from the default, set **sn\_supplyon\_po.org\_code\_override**.

2.  Set **sn\_supplyon\_po.plant\_code** for your plant.

3.  Adjust the payload constants—**edi\_sender**, **order\_type**, **header\_note**, and **erp\_system\_id**—as needed.


