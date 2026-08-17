---
title: ServiceNow Otto for Zero Copy Connector ERP data query skill
description: Use the Otto ERP data query skill in ServiceNow Otto for Zero Copy Connector to identify SAP objects such as tables, BAPI, and OData endpoints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/now-assist-erp-data-query.html
release: australia
topic_type: concept
last_updated: "2026-07-22"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use generative AI, ServiceNow Otto for Zero Copy Connector, Workflow Data Fabric]
---

# ServiceNow Otto for Zero Copy Connector ERP data query skill

Use the Otto ERP data query skill in ServiceNow Otto for Zero Copy Connector to identify SAP objects such as tables, BAPI, and OData endpoints.

## ERP data query overview

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

The ERP data query skill helps you identify SAP objects that can then be used to query the required data. For example, use ERP data query to obtain an OData endpoint.

This skill can help you create new ERP models and model operations more quickly by automating the identification of correct SAP data sources. The skill also reduces the need for deep technical knowledge and manually looking up information.

The sn\_erp\_integration.erp\_ai\_user role is required to work with generative AI and agentic AI in ServiceNow Otto for Zero Copy Connector.

## Prerequisites for using ERP data query

Follow the instructions in [Configure ServiceNow Otto for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-now-assist-for-zero-copy-connectors.md) to install the plugin.

## Asking Now Assist to identify SAP objects

Select the Otto icon \(\[Omitted image "bus-ai-otto.svg"\] Alt text:\) from anywhere in your instance to open the ServiceNow Otto panel.

Ask for information in plain language. For example, `Fetch routing operations for material 12345 in work center WC-10`.

Otto responds with the table and filter condition it will use and asks for your confirmation. You select **Yes**.

Otto provides the information you requested.

## Licensing requirements

The ERP data query skill requires a Workflow Data Fabric Pro license.

