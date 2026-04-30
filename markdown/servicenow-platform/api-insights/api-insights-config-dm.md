---
title: Configure data model recommendations for API clustering in API Insights
description: Set recommendations for clustering API components to align the organization's data with the desired data model.
locale: en-US
release: xanadu
product: API Insights
classification: api-insights
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CMDB administrator tasks, Configure, API Insights, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure data model recommendations for API clustering in API Insights

Set recommendations for clustering API components to align the organization's data with the desired data model.

## Before you begin

Role required: sn\_cmdb\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  Select the **Settings** tab.

3.  In the Data model recommendations section, configure system-generated recommendations for clustering related API components based on your organization’s data model.

    |Field|Description|
    |-----|-----------|
    |Proposed API clustering|Option to enable the system-generated API clustering recommendations. When selected, the system will propose clustering connections between related API components within the same API.|
    |Cluster quality|Desired quality level for the API clustering recommendations. The cluster quality can range from `0` to `100`, where a higher value represents a stronger connection between related components.|

4.  Select **Save**.


