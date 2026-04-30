---
title: Zero Copy Connector for ERP content pack process extensions
description: Use the process extensions in Zero Copy Connector for ERP content packs as examples that can be copied to add subflows with business logic to one or more models.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-04-16"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, content pack, process extension]
breadcrumb: [Zero Copy Connector for ERP content packs, Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Zero Copy Connector for ERP content pack process extensions

Use the process extensions in Zero Copy Connector for ERP content packs as examples that can be copied to add subflows with business logic to one or more models.

Process extensions are subflows that can use one or more models. Process extensions enable you to use a model without needing to understand the model details. The process extensions are another abstraction layer on top of the models inside the content pack to make the models easier to use.

Process extensions in a content pack are read-only examples. To use a process extension, make a copy and edit it within Workflow Studio. For the steps to copy a process extension and add cloned models, see [Using Zero Copy Connector for ERP process extensions](../task/erp-canvas-using-process-extensions.md).

![Workflow Studio subflows list showing content pack process extensions.](../image/erpc-process-extensions-list-ws.png)

## Process extension example

In this example, there is a model for reading a sales order. You want to determine the sales orders that are blocked, but you don't know the field in SAP that indicates if a sales order is blocked or not. Instead of researching to get the field name or asking the SAP experts in your organization, use the process extension named **ERP DP: Read Blocked Sales Orders** to do the work.

A process extension can filter or add data when reading, using the model to find exactly what you are looking for based on the process extension description. So, in our example, instead of reading all sales orders, the process extension finds only the blocked sales orders.

**Parent Topic:**[Zero Copy Connector for ERP content packs](erp-canvas-content-packs.md)

