---
title: Reviewing data integrations for Data Foundations
description: Review both existing and suggested Discovery patterns and Service Graph Connectors to improve your Data Foundations data coverage.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-02-25"
reading_time_minutes: 2
breadcrumb: [Analyze data integrations, Use Data Foundations advisor, CMDB success advisor, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Reviewing data integrations for Data Foundations

Review both existing and suggested Discovery patterns and Service Graph Connectors to improve your Data Foundations data coverage.

The **Data integrations** tab in CMDB success advisor for Data Foundations provides insight into current integration usage for Discovery patterns and Service Graph Connectors. To make sure your CMDB is being correctly populated with high-quality CI data for your principal classes, check the status of both integration types.

## Integration types

The **Data integrations** tab displays two key data sources that support Data Foundations:

-   **Discovery patterns**

    Discovery patterns identify IT infrastructure components through network-based discovery.

    To evaluate Discovery pattern effectiveness for Data Foundations, review the fields as described in the following table.

    |Field|Description|
    |-----|-----------|
    |Status|Indicates whether a Discovery pattern is currently active. Only active patterns contribute data to the CMDB.|
    |Attribute coverage|Displays how many Data Foundations relevant attributes within a principal class are being populated by each pattern.|
    |View pattern|Opens the Discovery pattern configuration, enabling you to inspect or refine the logic, identification rules, and targeted CI classes.|

    Low attribute coverage might occur if the Discovery pattern is limited in scope, not collecting detailed CI information, or if its identification rules are not aligned with the actual devices in your network. In such cases, required CI attributes may be missing from the resulting CI records.

-   **Service Graph Connectors**

    Service Graph Connectors import CI data from third-party platforms.

    To evaluate Service Graph Connectors effectiveness for Data Foundations, review the fields as described in the following table.

    |Field|Description|
    |-----|-----------|
    |Installed|Indicates whether the connector is deployed. A value of `Yes` confirms it is installed and available for use.|
    |Attribute coverage|Displays how many Data Foundations relevant attributes within a principal class are being populated by each connector.|
    |Active connections|Represents the number of connections actively importing data into the CMDB.|
    |Inactive connections|Displays connections that are configured but not currently importing data and may need troubleshooting.|

    If a Service Graph Connector shows low attribute coverage or no active connections, it may indicate that the specific version being evaluated has limited attribute coverage. This can happen if the connector is installed but not fully mapped to populate key attributes or if the data source is unavailable or misconfigured. As a result, critical CI data, such as ownership, location, or relationship information, may not be imported into the CMDB, affecting data quality for your principal classes.


