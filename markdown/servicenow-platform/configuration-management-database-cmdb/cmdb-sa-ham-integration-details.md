---
title: Reviewing data integrations for HAM
description: Review both existing and suggested Discovery patterns and Service Graph Connectors to improve your HAM data coverage.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-08-07"
reading_time_minutes: 2
breadcrumb: [Analyze data integrations, Use HAM advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Reviewing data integrations for HAM

Review both existing and suggested Discovery patterns and Service Graph Connectors to improve your HAM data coverage.

The **Data integrations** tab in CMDB success advisor for HAM provides insight into current integration usage for Discovery patterns and Service Graph Connectors. To make sure your CMDB is being correctly populated with high-quality HAM data, check the status of both integration types.

## Integration types

The **Data integrations** tab displays two key data sources that support HAM:

-   **Discovery patterns**

    Discovery patterns identify IT infrastructure components through network-based discovery.

    To evaluate Discovery pattern effectiveness for HAM, review the fields as described in the following table.

    |Field|Description|
    |-----|-----------|
    |Status|Indicates whether a Discovery pattern is currently active. Only active patterns contribute data to the CMDB.|
    |Attribute coverage|Displays how many HAM relevant attributes within a model category are being populated by each pattern.|
    |View pattern|Opens the Discovery pattern configuration, enabling you to inspect or refine the logic, identification rules, and targeted CI classes.|

    Low attribute coverage might occur if the Discovery pattern is limited in scope, not collecting detailed CI information, or if its identification rules are not aligned with the actual devices in your network. In such cases, required hardware attributes may be missing from the resulting CI records.

-   **Service Graph Connectors**

    Service Graph Connectors import asset and CI data from third-party platforms.

    To evaluate Service Graph Connectors effectiveness, review the fields as described in the following table.

    |Field|Description|
    |-----|-----------|
    |Installed|Indicates whether the connector is deployed. A value of `Yes` confirms it is installed and available for use.|
    |Attribute coverage|Displays how many HAM relevant attributes within a model category are being populated by each connector.|
    |Active connections|Represents the number of connections actively importing data into the CMDB.|
    |Inactive connections|Displays connections that are configured but not currently importing data and may need troubleshooting.|

    If a Service Graph Connector shows low attribute coverage or no active connections, it may indicate that the specific version being evaluated has limited attribute coverage. This can happen if the connector is installed but not fully mapped to populate key attributes or if the data source is unavailable or misconfigured. As a result, critical hardware data, such as serial numbers, models, or manufacturers, may not be imported into the CMDB, affecting the completeness and reliability of asset records.


