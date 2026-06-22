---
title: Now Assist for Zero Copy Connector ERP data query skill
description: Use the Now Assist ERP data query skill in Now Assist for Zero Copy Connector to identify SAP objects such as tables, BAPI, and OData endpoints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/now-assist-erp-data-query.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use generative AI, Now Assist for Zero Copy Connector, Workflow Data Fabric]
---

# Now Assist for Zero Copy Connector ERP data query skill

Use the Now Assist ERP data query skill in Now Assist for Zero Copy Connector to identify SAP objects such as tables, BAPI, and OData endpoints.

## ERP data query overview

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

The ERP data query skill helps you identify SAP objects that can then be used to query the required data. For example, use ERP data query to obtain an OData endpoint.

This skill can help you create new ERP models and model operations more quickly by automating the identification of correct SAP data sources, eliminating the need for manual look up and deep technical knowledge.

The sn\_erp\_integration.erp\_ai\_user role is required to work with generative AI and agentic AI in Now Assist for Zero Copy Connector.

## Prerequisites for using ERP data query

Follow the instructions in [Configure Now Assist for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-now-assist-for-zero-copy-connectors.md) to install the plugin.

## Asking Now Assist to identify SAP objects

Select the Now Assist icon \(\[Omitted image "now-assist-sparkle-icon-dark.png"\] Alt text:\) from anywhere in your instance to open the Now Assist panel.

Ask for information in plain language. For example, `Fetch routing operations for material 12345 in work center WC-10`.

\[Omitted image "erp-data-query-skill1.png"\] Alt text: Now Assist panel with entered question highlighted.

Now Assist responds with the table and filter condition it will use and asks for your confirmation. You select **Yes**.

\[Omitted image "erp-data-query-skill2.png"\] Alt text: Now Assist panel with information about the table and a confirmation option.

Now Assist provides the information you requested.

\[Omitted image "erp-data-query-skill3.png"\] Alt text: Now assist panel with information retrieved listed.

## Licensing requirements

The ERP data query skill requires a Workflow Data Fabric Pro license.

