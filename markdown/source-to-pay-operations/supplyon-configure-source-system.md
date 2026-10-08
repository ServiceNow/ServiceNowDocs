---
title: Configure the SupplyOn source system
description: Confirm the ERP source and integration source records that route purchase orders to SupplyOn.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplyon-configure-source-system.html
release: zurich
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [Configuring the Supplyon integration, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure the SupplyOn source system

Confirm the ERP source and integration source records that route purchase orders to SupplyOn.

## Before you begin

Role required: admin

## About this task

The SupplyOn source is modeled as an ERP source. It shares the same purchase order, legal entity, ERP source, integration source, and connection pattern as the SAP, Oracle, Ariba, and Coupa integrations. It does not use the cXML punchout model. The application includes two configuration records as application data.

|Table|Record|Key fields|
|-----|------|----------|
|sn\_fin\_erp\_source|SupplyOn|`source = "SupplyOn"`, `active = true`|
|sn\_fcms\_intg\_source|SupplyOn|`name = "SupplyOn"`, fin\_erp points at the ERP source, `inactive = false`, connection points at the supplyOnOrders alias|

## Procedure

1.  Confirm the ERP Source \[sn\_fin\_erp\_source\] record \(source SupplyOn, active\) exists.

2.  Confirm the Integration Source \[sn\_fcms\_intg\_source\] record exists, with **fin\_erp** pointing at the ERP source, **inactive** cleared, and **connection** pointing at the **supplyOnOrders** alias.

3.  Verify that each legal entity that routes to SupplyOn has its **erp\_source** set to the SupplyOn ERP source.

4.  Confirm the child Integration Service \[sn\_fcms\_intg\_service\] row that registers the confirmation subflow against the integration source record.


