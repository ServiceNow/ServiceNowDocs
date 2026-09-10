---
title: Exploring Zero Copy Connector for ERP content packs
description: Use Zero Copy Connector for ERP \(Enterprise Resource Planning\) content packs to view examples and create an ERP model faster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/exploring-erp-content-packs.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-08-05"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, content, pack, data, product, example]
breadcrumb: [Exploring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Exploring Zero Copy Connector for ERP content packs

Use Zero Copy Connector for ERP \(Enterprise Resource Planning\) content packs to view examples and create an ERP model faster.

Zero Copy Connector for ERP content packs are collections of ERP models and process extensions, available as separate downloads from the ServiceNow Store. They give developers a significant head start when building SAP integrations, especially developers and teams with little or no SAP domain knowledge.

Each content pack is organized around a specific business process area. Currently available content packs include:

-   Enterprise Data Foundation: Data models covering materials, vendors, customers, cost centers, chart of accounts, and foundational SAP reference data that spans modules.
-   Quote to Cash: Sales order management models covering create, read, and update operations for sales orders, outbound deliveries, credit memos, customer invoices, and customer credit limits.
-   Source to Settle: Procurement models covering purchase orders, purchase requisitions, and purchasing info records.
-   Hire to Retire: Employee life cycle models covering candidates, employee profiles, job applications, job requisitions, and positions.

## Key benefits

The biggest benefit is speed. Building models from scratch requires mapping SAP tables, BAPIs \(business application programming interfaces\), input/output fields, and operations by hand. Content packs give developers a ready-made starting point. Read, update, and create operations come pre-configured with typical input/output parameter mappings already in place.

SAP data structures are complex. Content packs make SAP integrations accessible to developers who don't have deep SAP expertise. The work of identifying the right tables, BAPIs, and field mappings has already been done.

## Use case

A developer must build an application that manages sales order delivery and billing blocks in SAP. However, the developer isn't an SAP expert and doesn't know which fields control blocking behavior.

Rather than spending days researching, they install the Quote to Cash content pack. They find the CP: Sales Orders model already has Read, Update, and Create operations configured, with input and output parameters mapped to relevant SAP fields. They also find a process extension called Manage Delivery and Billing Block that contains two subflows: one that reads all sales orders with delivery or billing blocks, and one that updates the blocking status for a given order.

The developer clones the model into their own application scope, copies the process extension into Workflow Studio, and wires it to their application. The developer can do this work without needing to know the underlying SAP field names. What might have taken weeks of research is reduced to configuration work.

