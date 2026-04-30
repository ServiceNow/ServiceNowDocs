---
title: Now Assist ERP data discovery skill
description: Use the Now Assist ERP data discovery skill in Now Assist for Zero Copy Connector to query SAP standard database tables for data and records.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI, zero copy connector, erp]
breadcrumb: [Now Assist for Zero Copy Connector skills, Now Assist for Zero Copy Connector, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Now Assist ERP data discovery skill

Use the Now Assist ERP data discovery skill in Now Assist for Zero Copy Connector to query SAP standard database tables for data and records.

## Now Assist ERP data discovery overview

This feature is available starting with the Zurich Patch 4 release.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

The sn\_erp\_integration.erp\_ai\_user role is required to work with generative AI and agentic AI in Now Assist for Zero Copy Connector.

The ERP data discovery skill lets you query SAP standard database tables for data and transactional records based upon natural language queries. This skill simplifies the process of getting information, potentially increasing efficiency.

Along with data, transactional records such as purchase orders, sales orders, sales documents, material information, billing documents, and delivery data are searched.

ERP data discovery is designed to support a wide range of business needs. It is ideal for use cases involving automation, business intelligence, auditing, and operational visibility. Use ERP data discovery for general data retrieval, such as listing all purchase orders or customer records. You can also monitor exceptions, such as blocked deliveries, incomplete orders, delivery holds, or rejected items. ERP data discovery gives you access to key status fields, like delivery blocks, rejection reasons, and overall order progress.

The sn\_erp\_integration.erp\_ai\_user role is required to work with generative AI and agentic AI in Now Assist for Zero Copy Connector.

## Prerequisites for using ERP data discovery

Follow the instructions in [Configure Now Assist for Zero Copy Connector](../task/configure-now-assist-for-zero-copy-connectors.md) to install the plugin.

## Asking Now Assist for ERP data

Select the Now Assist icon \(![](../image/now-assist-sparkle-icon-dark.png)\) from anywhere in your instance to open the Now Assist panel.

Ask for information in plain language. For example, `Get all sales orders from SAP where sales organization is 1710`.

![Now Assist panel with entered question highlighted.](../image/erp-data-discovery-skill1.png)

Now Assist responds with the table and filter condition it will use and asks for your confirmation. You select **Yes**.

![Now Assist panel with information about the table and a confirmation option.](../image/erp-data-discovery-skill2.png)

Now Assist provides the information you requested.

![Now assist panel with information retrieved listed.](../image/erp-data-discovery-skill3.png)

Your conversation is saved until you start a new chat. If the conversation ends unexpectedly, start a new chat by selecting the New chat icon \(![New chat icon.](../../../common/image/icon-zoom-in.png)\).

## Additional example prompts

Consider trying the following prompts to become familiar with the data and records information that is available.

-   Retrieve all purchase orders above a specific value or within a given date range.

-   List customer records or materials by sales organization or region.

-   Identify blocked deliveries, incomplete orders, or rejected items.

-   Monitor key process statuses like delivery blocks, rejection reasons, and order completion.


## Licensing requirements

The ERP data discovery skill requires a Workflow Data Fabric Pro license.

