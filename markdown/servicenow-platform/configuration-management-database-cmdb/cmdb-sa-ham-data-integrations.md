---
title: Analyzing data integrations for improving HAM data coverage
description: Improve HAM data coverage by analyzing existing and suggested data integrations, including Discovery patterns and Service Graph Connectors.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use HAM advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Analyzing data integrations for improving HAM data coverage

Improve HAM data coverage by analyzing existing and suggested data integrations, including Discovery patterns and Service Graph Connectors.

Use the **Data integrations** tab in the CMDB success advisor for HAM to assess the effectiveness of your current data integration sources in the Configuration Management Database \(CMDB\) and identify opportunities to improve HAM data coverage. The **Data integrations** tab provides a breakdown of active Discovery patterns and installed Service Graph Connectors, including how many key configuration item \(CI\) attributes each integration source is populating.

For a quick reference to improve HAM data coverage, see [Data integration checklist for HAM in CMDB success advisor](cmdb-sa-ham-integ-checklist.md).

## Access data integrations

Navigate to the CMDB success advisor, and on the HAM card, select **View insights**. Select the **Data integrations** tab. To access the dashboard, see [Access CMDB success advisor](../task/cmdb-sa-access.md).

**Note:** The CMDB success advisor for HAM dashboard is available only after the setup process is complete. For more information, see [Set up CMDB success advisor for HAM](cmdb-sa-ham-config-settings.md).

## Required roles

|Role|Description|
|----|-----------|
|sn\_cmdb\_admin|Required to access the CMDB success advisor.|
|cmdb\_inst\_admin|Required to manage Service Graph Connector connections in SGC Central.|
|pd\_admin|Required to manage Discovery patterns with create and write access.|
|pd\_user|Required to view Discovery patterns with read-only access.|
|pd\_mid|Required to view Discovery and Service Mapping Patterns with read-only access.|

## Use cases

For examples of how different people in your organization would use this feature, see these use cases.

<table id="table_lnc_zz1_2gc"><thead><tr><th>

User

</th><th>

Feature use

</th></tr></thead><tbody><tr><td>

CMDB administrator

</td><td>

-   Identify an inactive Discovery pattern that can populate attribute data for hardware assets.
-   Identify a Service Graph Connector relevant to hardware assets that is installed but without any active connections.
-   Prioritize which hardware-related integrations to improve to maximize CMDB data quality for improving the completeness, accuracy, and reconciliation of hardware asset records.

</td></tr></tbody>
</table>## Data integration features

|Feature|Description|
|-------|-----------|
|Integration overview|Displays the count of all Discovery patterns and Service Graph Connectors contributing hardware asset data to the CMDB.|
|Status indicators|Check whether Discovery patterns are active and Service Graph Connectors are installed with active connections. For more information, see [Reviewing data integrations for HAM](cmdb-sa-ham-integration-details.md).|
|Attribute coverage insights|Select the **Attribute coverage** link next to the integration to review which hardware asset attributes are populated by a Discovery pattern or Service Graph Connector. For more information, see [Evaluate HAM data integration coverage](../task/cmdb-sa-ham-evaluate-data-integration.md).|
|Access integration details|Configure integrations to improve attribute coverage. For more information, see [Evaluate HAM data integration coverage](../task/cmdb-sa-ham-evaluate-data-integration.md).|

