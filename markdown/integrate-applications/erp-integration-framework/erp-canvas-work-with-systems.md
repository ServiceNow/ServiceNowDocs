---
title: Working with ERP systems in Zero Copy Connector for ERP
description: A Zero Copy Connector for ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system. For example, sales orders or vendor invoices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-work-with-systems.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, system, erp system]
breadcrumb: [Configure, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Working with ERP systems in Zero Copy Connector for ERP

A Zero Copy Connector for ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system. For example, sales orders or vendor invoices.

## ERP systems organize connections to the ERP system

The Zero Copy Connector for ERP system plays a crucial role in data synchronization, sharing, and collaboration, enabling seamless integration and operation between the model and the connected ERP system.

Zero Copy Connector for ERP provides a standard set of models, such as SAP Material Stock and SAP Purchase Document. For a list, see [Standard extraction tables for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-standard-extraction-tables.md). For information about building new models, see [Create a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-add-new-data-model.md). Use Zero Copy Connector for ERP data products, sets of predefined models and process extensions, as examples to help you implement and deploy applications with less manual work. For more information, see [Zero Copy Connector for ERP content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-content-packs.md).

## Configuring ERP systems and checking connections

Zero Copy Connector for ERP ERP systems are configured by ServiceNow admins. Zero Copy Connector for ERP supports connecting to multiple systems.

Zero Copy Connector for ERP regularly scans all connected ERP systems for the latest heartbeat, which indicates whether a ping to the ERP system connection is successful.

