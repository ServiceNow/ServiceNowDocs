---
title: ServiceNow Otto for Zero Copy Connector ERP data discovery skill
description: Use the Otto ERP data discovery skill in ServiceNow Otto for Zero Copy Connector to query SAP standard database tables for data and records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/now-assist-erp-data-discovery-skill.html
release: australia
topic_type: concept
last_updated: "2026-07-22"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use generative AI, ServiceNow Otto for Zero Copy Connector, Workflow Data Fabric]
---

# ServiceNow Otto for Zero Copy Connector ERP data discovery skill

Use the Otto ERP data discovery skill in ServiceNow Otto for Zero Copy Connector to query SAP standard database tables for data and records.

## Now Assist ERP data discovery overview

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

The sn\_erp\_integration.erp\_ai\_user role is required to work with generative AI and agentic AI in ServiceNow Otto for ZCC.

The ERP data discovery skill lets you query SAP standard database tables for data and transactional records based upon natural language queries. This skill simplifies the process of getting information, potentially increasing efficiency.

Along with data, transactional records such as purchase orders, sales orders, sales documents, material information, billing documents, and delivery data are searched.

ERP data discovery is designed to support a wide range of business needs. It is ideal for use cases involving automation, business intelligence, auditing, and operational visibility. Use ERP data discovery for general data retrieval, such as listing all purchase orders or customer records. You can also monitor exceptions, such as blocked deliveries, incomplete orders, delivery holds, or rejected items. ERP data discovery gives you access to key status fields, like delivery blocks, rejection reasons, and overall order progress.

The sn\_erp\_integration.erp\_ai\_user role is required to work with generative AI and agentic AI in ServiceNow Otto for ZCC.

## Prerequisites for using ERP data discovery

Follow the instructions in [Configure ServiceNow Otto for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-now-assist-for-zero-copy-connectors.md) to install the plugin.

## Asking Now Assist for ERP data

Select the Otto icon \(\[Omitted image "bus-ai-otto.svg"\] Alt text:\) from anywhere in your instance to open the ServiceNow Otto panel.

Ask for information in plain language. For example, `Get all sales orders from SAP where sales organization is 1710`.

Otto responds with the table and filter condition it will use and asks for your confirmation. You select **Yes**.

Otto provides the information you requested.

Your conversation is saved until you start a new chat. If the conversation ends unexpectedly, start a new chat by selecting the New chat icon \(\[Omitted image "icon-zoom-in.png"\]\).

## Additional example prompts

Consider trying the following prompts to become familiar with the data and records information that is available.

-   Retrieve all purchase orders higher than a specific value or within a given date range.

-   List customer records or materials by sales organization or region.

-   Identify blocked deliveries, incomplete orders, or rejected items.

-   Monitor key process statuses like delivery blocks, rejection reasons, and order completion.


## Licensing requirements

The ERP data discovery skill requires a Workflow Data Fabric Pro license.

