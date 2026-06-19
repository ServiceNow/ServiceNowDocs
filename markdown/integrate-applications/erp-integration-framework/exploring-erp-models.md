---
title: Exploring Zero Copy Connector for ERP models
description: Build ERP \(Enterprise Resource Planning\) models in Zero Copy Connector for ERP to create read, update, and create operations and organize mirrored ERP data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/exploring-erp-models.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model]
breadcrumb: [Explore, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Exploring Zero Copy Connector for ERP models

Build ERP \(Enterprise Resource Planning\) models in Zero Copy Connector for ERP to create read, update, and create operations and organize mirrored ERP data.

In Zero Copy Connector for ERP, a **model** is the foundational building block for accessing and working with ERP data. It represents the logical structure and organization of data coming from the ERP system of record. A model defines the tables, fields, read/update/create operations, and table join relationships that capture a specific business process or dataset. After you configure a model, you can use it as a data source for building apps, flows, playbooks, workspaces, and more.

There are two types of models:

-   ERP models follow the data structures defined by the external ERP system itself, accommodating the unique formats of each connected system.
-   Platform models map ERP input and output fields to existing ServiceNow platform tables, standardizing ERP data into the Now Platform's data structure for tighter integration.

\[Omitted image "erp-explore-model-types-infographic.png"\] Alt text: Infographic showing the two types of models: ERP model and platform model.

Zero Copy Connector for ERP includes a standard set of models and supports creating custom models from scratch or by cloning existing ones. Each model connects to one ERP system, and each model can have only one read operation, one update operation, and one create operation defined. Operations use one of several underlying methods depending on the type of operation and what the connected ERP system supports.

## Key benefits

Models create a consistent, reusable data layer. You can connect the same ERP table to multiple models, and build as many models as needed to represent different business areas.

Through input and output parameter mapping, you define exactly which ERP fields are used and exactly what the model sends back to the ERP on reads, updates, and creates. This means sensitive fields never reach remote or extraction tables, because you exclude them at the model level before any data flows.

Models support a range of underlying connection methods \(table reads, BAPIs, RFC, OData, IDoc, and REST APIs\), so you can match the method to what's available and appropriate for the ERP module and operation type you are working with.

After a model is ready and its operations are configured, use it as a data source across Workflow Studio flows, ServiceNow Studio, Workspace Builder, UI Builder, Table Builder, and playbooks. This makes models a universal integration point rather than something custom built for a single use case.

## Use case

A developer is building a vendor management application and needs to retrieve vendor data from SAP, allow updates to vendor payment terms, and create vendor records.

Instead of building three separate integrations, the developer creates a single vendor model connected to the appropriate SAP system. In the model manager, they add three operations: a read operation using an RFC/BAPI entity to retrieve vendor details, an update operation using OData to write payment term changes back to SAP, and a create operation using a BAPI to create vendors.

The completed model is then used as the data source for a Workflow Studio flow that triggers whenever a new vendor request is submitted.The flow automatically reads existing vendor data, routes through an approval, and writes the approved changes directly back to the SAP system, so that no one needs to log in to the SAP system directly.

**Parent Topic:**[Exploring Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/exploring-erp-integration.md)

