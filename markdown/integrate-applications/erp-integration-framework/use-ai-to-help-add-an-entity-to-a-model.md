---
title: Use generative AI to help add an entity to a model
description: Enter a use case for an entity and obtain suggestions from generative AI about the relevant table, BAPI, Odata, or RFC to use.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, entity, entities, ai, generative, now assist]
breadcrumb: [Add an entity to a model, Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Use generative AI to help add an entity to a model

Enter a use case for an entity and obtain suggestions from generative AI about the relevant table, BAPI, Odata, or RFC to use.

## Before you begin

This feature is available starting with the Zurich Patch 4 release.

Role required: sn\_erp\_integration.erp\_admin and sn\_erp\_integration.erp\_ai\_user

## About this task

When adding an entity to a model operation, use the **Ask AI** button to receive suggestions for relevant data entities, including tables, BAPIs, OData services, and RFCs. Generative AI can simplify the process of getting information, potentially increasing efficiency.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page and select the model to which you want to add an operation entity.

3.  Select **Manage model**.

4.  Select an operation.

5.  Select **Ask AI**.

6.  In the search, enter text to describe the entity you want.

    For example, enter `Get the list of Purchase Orders created in the last 3 years for the vendors that are blocked`.

    Read the **AI suggestions** for the relevant data sources \(for example, table, BAPI, OData, RFC\) available. Select the plus icon \(![](../image/erp-plus-icon.png)\) next to any option for more information.

    ![Entity suggestions listed based on text entered to describe the needed entity.](../image/erp-entity-ask-ai1.png)

    A separate list shows any already installed models that contain the suggested entities. For example, after entering `Show list of all change documents that are in progress`, several installed models were listed. Select the plus icon \(![](../image/erp-plus-icon.png)\) next to any model for more information.

    ![Entity suggestions with separate highlighted list of installed models.](../image/erp-entity-ask-ai2.png)

    If there are any relevant data products, they are listed with a link to the ServiceNow Store page for more information about purchasing and installing.

    If no relevant data entities are identified, a **No results found** message is displayed. Try describing what you need in different ways to see if you receive different results.

    At any time, select a **Previous AI response** to see the suggestions again.

    ![Entity suggestions with previous AI responses list highlighted.](../image/erp-entity-ask-ai3.png)


**Parent Topic:**[Add an entity to a model](../concept/add-an-entity-to-model.md)

