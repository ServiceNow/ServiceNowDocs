---
title: Identify SAP objects for a model with the ERP data query skill
description: ServiceNow Otto identifies the SAP tables, BAPIs, and OData endpoints that you need to query the data you describe, so you can create ERP models and model operations faster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-identify-sap-objects-with-erp-data-query.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 3
keywords: [erp, zero, copy, connector, sap, ai, otto, skill, data query, table, bapi, odata, endpoint, model]
breadcrumb: [ERP models, Using, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Identify SAP objects for a model with the ERP data query skill

ServiceNow Otto identifies the SAP tables, BAPIs, and OData endpoints that you need to query the data you describe, so you can create ERP models and model operations faster.

## Before you begin

Role required: sn\_erp\_integration.erp\_ai\_user

The ServiceNow Otto for Zero Copy Connector plugin is installed. For more information, see [Install the ServiceNow Otto for Zero Copy Connector plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-install-the-erp-ai-plugin.md).

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Use the ERP data query skill to find the correct SAP data source without looking it up manually. For example, ask for the OData endpoint that returns the data you need, and then use it in a model operation.

## Procedure

1.  Select the Otto icon \(\[Omitted image "bus-ai-otto.svg"\] Alt text:\) from anywhere in your instance to open the ServiceNow Otto panel.

2.  Describe the data that you want in plain language.

    For example, `Fetch routing operations for material 12345 in work center WC-10`.

    ServiceNow Otto shows the table and filter condition that it will use and asks you to confirm.

3.  Select **Yes**.

    ServiceNow Otto provides the information you requested.


## Result

You have the SAP object to use in a model operation.

Your conversation is saved until you start a new chat. If the conversation ends unexpectedly, start a new chat by selecting the New chat icon \(\[Omitted image "icon-zoom-in.png"\]\).

## Find SAP objects manually

If ServiceNow Otto is unavailable or the skill is deactivated, find tables or look up the BAPI, OData, or RFC source yourself. For more information, see [View and edit ERP remote table details with Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpi-find-tables.md), [Add a BAPI entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/add-a-bapi-entity-to-a-model-operation.md), [Add an OData entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/add-an-odata-entity-to-a-model-operation.md), and [Add an RFC entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/add-a-rfc-entity-to-a-model-operation.md).

## What to do next

Add the SAP object to a model. For more information, see [Create a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-add-new-data-model.md) and [Adding an entity to a Zero Copy Connector for ERP model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/add-an-entity-to-model.md).

**Parent Topic:**[Building and managing models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/work-with-erp-data-models.md)

**Related topics**  


[View and deactivate ERP skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-activate-and-manage-erp-skills.md)

[Set access controls for ERP skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-set-access-for-erp-skills.md)

