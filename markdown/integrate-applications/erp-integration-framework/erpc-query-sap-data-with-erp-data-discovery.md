---
title: Query SAP data with the ERP data discovery skill
description: Ask ServiceNow Otto in plain language for data and transactional records from SAP standard database tables, such as purchase orders, sales orders, and delivery data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erpc-query-sap-data-with-erp-data-discovery.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 2
keywords: [erp, zero, copy, connector, sap, ai, otto, skill, data discovery, query, table, purchase order, sales order, delivery]
breadcrumb: [Data retrieval, Using, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Query SAP data with the ERP data discovery skill

Ask ServiceNow Otto in plain language for data and transactional records from SAP standard database tables, such as purchase orders, sales orders, and delivery data.

## Before you begin

Role required: sn\_erp\_integration.erp\_ai\_user

The ServiceNow Otto for Zero Copy Connector plugin is installed. For more information, see [Install the ServiceNow Otto for Zero Copy Connector plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-install-the-erp-ai-plugin.md).

The ERP data discovery and ERP data query skills require a Workflow Data Fabric Pro license.

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

The ERP data discovery skill searches SAP standard database tables for data and transactional records, including purchase orders, sales orders, material information, billing documents, and delivery data. Use it for data retrieval, such as listing purchase orders or customer records, and for monitoring exceptions, such as blocked deliveries, or incomplete orders. It also gives you access to key status fields, like delivery blocks, rejection reasons, and overall order progress.

## Procedure

1.  Select the Otto icon \(\[Omitted image "bus-ai-otto.svg"\] Alt text:\) from anywhere in your instance to open the ServiceNow Otto panel.

2.  Ask for the data that you want in plain language.

    For example, `Get all sales orders from SAP where sales organization is 1710`.

    You can also try requests like these:

    -   Retrieve all purchase orders higher than a specific value or within a given date range.
    -   List customer records or materials by sales organization or region.
    -   Identify blocked deliveries, incomplete orders, or rejected items.
    -   Monitor key process statuses like delivery blocks, rejection reasons, and order completion.
    ServiceNow Otto shows the table and filter condition that it will use and asks you to confirm.

3.  Select **Yes**.

    ServiceNow Otto provides the information you requested.


## Result

Your conversation is saved until you start a new chat. If the conversation ends unexpectedly, start a new chat by selecting the New chat icon \(\[Omitted image "icon-zoom-in.png"\]\).

## Query SAP data manually

If ServiceNow Otto is unavailable or the skill is deactivated, query a remote table instead. For more information, see [Query a remote table using Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-query-remote-table.md) and [Standard remote tables for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpi-standard-remote-tables.md).

**Parent Topic:**[Retrieving data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-retrieving-data.md)

**Related topics**  


[View and deactivate ERP skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-activate-and-manage-erp-skills.md)

[Set access controls for ERP skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-set-access-for-erp-skills.md)

