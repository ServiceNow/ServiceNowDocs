---
title: Advisor card states in Service Graph Workspace
description: Each of the three ServiceNow CMDB success advisor cards in Service Graph Workspace shows different content depending on setup and entitlement status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-workspace-card-states.html
release: brazil
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-11-03"
reading_time_minutes: 2
keywords: [CMDB workspace product highlight cards, card button labels, AI-generated summary caption, advisor card entitlement]
breadcrumb: [CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Advisor card states in Service Graph Workspace

Each of the three ServiceNow® CMDB success advisor cards in Service Graph Workspace shows different content depending on setup and entitlement status.

In the Governance view of Service Graph Workspace, the CMDB success advisor section shows a separate card for three products. The products are Data Foundations \(DF\), Hardware Asset Management \(HAM\), and Software Asset Management \(SAM\). Each card has one button. The button label and action depend on the setup status of the product and on whether an AI-generated summary is available.

-   If the advisor scope for the product isn't configured yet, the button is labeled **Set principal classes** \(DF\), **Select model categories** \(HAM\), or **Select software products** \(SAM\). Select it to open the CMDB success advisor landing page and start the setup for that product.
-   If the advisor scope is configured and no AI-generated summary is available, the button is labeled **View insights**. Select it to open the advisor dashboard for that product.
-   If the advisor scope is configured and an AI-generated summary is available, the button is labeled **View remediations**. Select it to open the advisor dashboard for that product.

A card may also show an **Auto-setup** tag. For more information, see [Automatic dashboard setup for Data Foundations in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-auto-setup.md).

## Card content by state

The content and timestamp shown on a product card depend on setup status, entitlement, and whether an AI-generated summary is available for that product.

|State|What the card shows|Timestamp|
|-----|-------------------|---------|
|Advisor scope configured, AI-generated summary available|An AI-generated caption that summarizes the most significant data quality issue for the product.|Shown. Displays the date and time of the last data collection.|
|Advisor scope configured, AI-generated summary not available|A static caption indicating that an AI-generated summary isn't available yet.|Not shown.|
|Advisor scope not configured, product entitled|A static caption prompting you to set up the advisor for that product.|Not shown.|
|Advisor scope not configured, product not entitled|The card doesn't appear in the CMDB success advisor section.|Not applicable.|

**Note:** The AI-generated summary is available for Data Foundations and HAM only.

