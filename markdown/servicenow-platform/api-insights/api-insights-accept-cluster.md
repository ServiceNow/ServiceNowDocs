---
title: Accept clustering recommendation in API Insights
description: Associate API components with an API record by accepting clustering recommendation in the API Insights workspace.
locale: en-US
release: zurich
product: API Insights
classification: api-insights
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Optimize clustering recommendations, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Accept clustering recommendation in API Insights

Associate API components with an API record by accepting clustering recommendation in the API Insights workspace.

## Before you begin

Role required: sn\_cmdb\_admin, ml\_report\_user, and platform\_ml\_read

## Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  On the **Overview** tab, select the count metric displayed in the API clustering recommendations section.

3.  On the **Proposed API clustering** tab, review the list of recommendations.

4.  From the **Cluster Concept** column, select a cluster concept link.

5.  On the Missing API page, review the list of API components that have not yet been associated with an API record.

6.  Select the check boxes next to the API components to associate with an API record.

    **Note:** You can select one or multiple components depending on your requirement.

7.  Select **Accept**.

8.  Select an API record.

    |Option|Description|
    |------|-----------|
    |**Existing API record**|Select this option if the API record already exists. Use the search field to find the API record by name.|
    |**Create API record**|Select this option to create an API record. Enter the required details such as the name, version, and base URL. The API will be created through the Identification and Reconciliation engine \(IRE\) using the provided details.|

9.  Select **Submit**.


## Result

The Missing API list is refreshed with the linked components removed from the list and associated with the specified API record.

