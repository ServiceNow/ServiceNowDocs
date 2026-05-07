---
title: Exploring Zero Copy Connector for ERP models
description: Build ERP \(Enterprise Resource Planning\) models in Zero Copy Connector for ERP to create read, update, and create operations and organize mirrored ERP data.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model]
breadcrumb: [Explore, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Exploring Zero Copy Connector for ERP models

Build ERP \(Enterprise Resource Planning\) models in Zero Copy Connector for ERP to create read, update, and create operations and organize mirrored ERP data.

In Zero Copy Connector for ERP, a **model** is the foundational building block for accessing and working with ERP data. It represents the logical structure and organization of data coming from the ERP system of record. A model defines the tables, fields, read/update/create operations, and table join relationships that capture a specific business process or dataset. After a model is configured, it is set to a data source for building apps, flows, playbooks, workspaces, and more.

There are two types of models:

-   ERP models follow the data structures defined by the external ERP system itself, accommodating the unique formats of each connected system.
-   Platform models map ERP input and output fields to existing ServiceNow platform tables, standardizing ERP data into the Now Platform's data structure for tighter integration.

![Infographic showing the two types of models: ERP model and platform model.](../image/erp-explore-model-types-infographic.png)

Zero Copy Connector for ERP includes a standard set of models and supports creating custom models from scratch or by cloning existing ones. Each model is tied to one ERP system, and each model can have only one read operation, one update operation, and one create operation defined. Operations use one of several underlying methods depending on the type of operation and what the connected ERP system supports.

![Infographic showing the three types of model operations: read, update, and create.](../image/erp-explore-model-operations-infographic.png)

## Key benefits

Models create a consistent, reusable data layer. You can connect the same ERP table to multiple models, and build as many models as needed to represent different business areas.

Through input and output parameter mapping, you define exactly which ERP fields are used and exactly what is sent back to the ERP on reads, updates, and creates. This means sensitive fields can be excluded at the model level before data ever reaches remote or extraction tables.

Models support a range of underlying connection methods \(table reads, BAPIs, RFC, OData, IDoc, and REST APIs\), so you can match the method to what's available and appropriate for the ERP module and operation type you're working with.

After a model is built and its operations are configured, it can be used as a data source across Workflow Studio flows, ServiceNow Studio, Workspace Builder, UI Builder, Table Builder, and playbooks. This makes models a universal integration point rather than something custom built for a single use case.

## Use case

A developer is building a vendor management application and needs to retrieve vendor data from SAP, allow updates to vendor payment terms, and create vendor records.

Instead of building three separate integrations, the developer creates a single vendor model connected to the appropriate SAP system. In the model manager, they add three operations: a read operation using an RFC/BAPI entity to retrieve vendor details, an update operation using OData to write payment term changes back to SAP, and a create operation using a BAPI to create vendors.

The completed model is then used as the data source for a Workflow Studio flow that triggers whenever a new vendor request is submitted. The flow automatically reads existing vendor data, routes through an approval, and writes the approved changes directly back to the SAP system, all without anyone needing to log in to the SAP system.

**Parent Topic:**[Exploring Zero Copy Connector for ERP](exploring-erp-integration.md)

