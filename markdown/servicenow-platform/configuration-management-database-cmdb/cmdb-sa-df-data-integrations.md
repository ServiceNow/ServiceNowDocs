---
title: Analyzing data integrations for improving Data Foundations
description: Improve Data Foundations coverage by analyzing existing and suggested data integrations, including Discovery patterns and Service Graph Connectors.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-02-25"
reading_time_minutes: 2
breadcrumb: [Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Analyzing data integrations for improving Data Foundations

Improve Data Foundations coverage by analyzing existing and suggested data integrations, including Discovery patterns and Service Graph Connectors.

Use the **Data integrations** tab in the CMDB success advisor for Data Foundations to assess the effectiveness of your current data integration sources in the Configuration Management Database \(CMDB\) and identify opportunities to improve coverage across your principal classes. The **Data integrations** tab provides a breakdown of active Discovery patterns and installed Service Graph Connectors, including how many key configuration item \(CI\) attributes each integration source is populating.

For a quick reference to improve Data Foundations coverage, see [Data integration checklist for Data Foundations in CMDB success advisor](cmdb-sa-df-integ-checklist.md).

## Access data integrations

Navigate to the CMDB success advisor landing page, and on the Data Foundations card, select **View insights**. Select the **Data integrations** tab to access integration-related details. For more information, see [Access CMDB success advisor](../task/cmdb-sa-access.md).

**Note:** The CMDB success advisor for Data Foundations dashboard is available only after the setup process is complete. For more information, see [Set up CMDB success advisor for Data Foundations](cmdb-sa-df-config-settings.md).

## Required roles

|Role|Description|
|----|-----------|
|sn\_cmdb\_admin|Required to access the CMDB success advisor.|
|cmdb\_inst\_admin|Required to manage Service Graph Connector connections in SGC Central.|

## Use cases

For examples of how different people in your organization would use this feature, see these use cases.

<table id="table_lnc_zz1_2gc"><thead><tr><th>

User

</th><th>

Feature use

</th></tr></thead><tbody><tr><td>

CMDB administrator

</td><td>

-   Identify an inactive Discovery pattern that can populate attribute data for your principal classes
-   Identify Service Graph Connectors that cover your principal classes with the highest attribute coverage
-   Detect integration sources that are installed but have no active connections
-   Evaluate which integrations populate ownership, relationship, and infrastructure attributes for CMDB data accuracy
-   Prioritize which integrations to improve to maximize data quality across principal classes

</td></tr></tbody>
</table>## Data integration features

|Feature|Description|
|-------|-----------|
|Integration overview|Displays the count of all Discovery patterns and Service Graph Connectors contributing CI data to your principal classes in the CMDB.|
|Status indicators|Check whether Discovery patterns are active and Service Graph Connectors are installed with active connections. For more information, see [Reviewing data integrations for Data Foundations](cmdb-sa-df-integration-details.md).|
|Attribute coverage insights|Select the **Attribute coverage** link next to the integration to review which CI attributes it populates for your principal classes. For more information, see [Evaluate Data Foundations data integration coverage](../task/cmdb-sa-df-evaluate-data-integration.md).|
|Access integration details|Configure integrations to improve attribute coverage. For more information, see [Evaluate Data Foundations data integration coverage](../task/cmdb-sa-df-evaluate-data-integration.md).|

