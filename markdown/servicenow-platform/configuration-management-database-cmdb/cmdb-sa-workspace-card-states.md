---
title: Product highlight card states in CMDB Workspace
description: Each of the three ServiceNow CMDB success advisor cards in CMDB Workspace shows different content depending on setup and entitlement status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-workspace-card-states.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [CMDB workspace product highlight cards, Remediate action, AI-generated summary caption, advisor card entitlement]
breadcrumb: [CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Product highlight card states in CMDB Workspace

Each of the three ServiceNow® CMDB success advisor cards in CMDB Workspace shows different content depending on setup and entitlement status.

In the Home view of CMDB Workspace, the Product highlights section shows a separate card for three products. The products are Data Foundations \(DF\), Hardware Asset Management \(HAM\), and Software Asset Management \(SAM\). Each card includes a **Remediate** action.

-   If the advisor scope for the product is already configured, **Remediate** opens the advisor dashboard for that product.
-   If the advisor scope for the product isn't configured yet, **Remediate** opens the CMDB success advisor landing page and starts the setup for that product.

A card may also show an **Auto-setup** tag. For more information, see [Automatic dashboard setup for Data Foundations in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-auto-setup.md).

## Card content by state

The content and timestamp shown on a product card depend on setup status, entitlement, and whether an AI-generated summary is available for that product.

|State|What the card shows|Timestamp|
|-----|-------------------|---------|
|Advisor scope configured, AI-generated summary available|An AI-generated caption that summarizes the most significant data quality issue for the product.|Shown. Displays the date and time of the last data collection.|
|Advisor scope configured, AI-generated summary not available|A static caption indicating that an AI-generated summary isn't available yet.|Not shown.|
|Advisor scope not configured, product entitled|A static caption prompting you to set up the advisor for that product.|Not shown.|
|Advisor scope not configured, product not entitled|The card doesn't appear in the Product highlights section.|Not applicable.|

**Note:** The AI-generated summary is available for Data Foundations and HAM only. The SAM card always shows the static caption for an unavailable summary, even after the SAM advisor scope is configured.

