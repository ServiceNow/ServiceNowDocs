---
title: View the status of API data connections in API Insights
description: View the status of your API data connections using Service Graph Connectors, including success rates, processing status, and ongoing executions.
locale: en-US
release: xanadu
product: API Insights
classification: api-insights
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage API data connections, API Insights, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View the status of API data connections in API Insights

View the status of your API data connections using Service Graph Connectors, including success rates, processing status, and ongoing executions.

## Before you begin

Role required: sn\_cmdb\_admin and cmdb\_inst\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  In the Connections overview section of the Overview tab, access the various cards to gain insights on the performance of Service Graph Connectors.

    |Card|Description|
    |----|-----------|
    |Connections status|Percentage of connections tested successfully based on connection status, with the count of success, error, and unknown statuses.|
    |Processing status|Percentage of connections for which all data import runs in the last import execution were successful, with the count of success and error statuses.|
    |Ongoing executions|Number of connections where data import execution is currently in progress.|

3.  From the **Connection** column, select a connection.

4.  On the connection record page, select a tab to view more information about the selected connection.

    |Tab|Description|
    |---|-----------|
    |Details|Connection information, such as the connection name and credentials associated with the connection.|
    |Connection properties|Properties configured for the connection.|
    |Data sources|Data sources associated with the connection, specifying what data is being retrieved or synchronized.|
    |Import schedules|Scheduled imports for the connection, including parent schedule, data source, timing and frequency of data retrieval.|
    |Errors|Error related to the connection.|


