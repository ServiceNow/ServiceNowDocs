---
title: Create an application service for unmapped servers
description: Maximize the use of your organization's resources by mapping application service candidates that include unmapped servers. Use the Service Mapping workspace's unmapped servers widget to create an application service and ensure that your servers are used efficiently.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Service Mapping, Application Service, unmapped server, Service Mapping workspace]
breadcrumb: [Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Create an application service for unmapped servers

Maximize the use of your organization's resources by mapping application service candidates that include unmapped servers. Use the Service Mapping workspace's unmapped servers widget to create an application service and ensure that your servers are used efficiently.

## Before you begin

-   Ensure that Predictive Intelligence is enabled.
-   Verify Machine Learning readiness.
-   Confirm that the data is trained.

For more information, see [Application service readiness dashboard in configurable workspace](../reference/readiness-dashboard-ml.md).

**Important:**

Service Mapping Plus v.1.10.0 or higher:

To update your data and view application candidates for unmapped servers, see [Troubleshooting steps for Mapping unmapped servers with Application service candidates \[KB1585065\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585065) in the Now Support Knowledge Base.

Role required: service\_mapping\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Mapping**.

2.  Select the unmapped server that you want to use to create an application service.

<table id="choicetable_vyc_pgt_zfc"><thead><tr><th align="left" id="d535230e133">

Version of Service Mapping Plus

</th><th align="left" id="d535230e139">

Actions

</th></tr></thead><tbody><tr><td id="d535230e145">

**Versions released before version 1.16.3**

</td><td>

1.  In the **Unmapped servers** tile, select the **Unmapped servers with Candidate ID** graph.
2.  Review the list of suggested candidates.
3.  Organize the candidate list to prioritize your work.

    |Organization method|Action|
    |-------------------|------|
    |Order|Select a column name to sort the results in ascending or descending order.|
    |Group|Select the menu \(![Menu icon](../../service-operations-workspace-itom/image/menu-icon.png)\) icon to group results by the selected column.|

4.  Select the preferred candidate.
5.  Select **Map application service**.


</td></tr><tr><td id="d535230e227">

**Starting with version 1.16.3**

</td><td>

1.  In the **Unmapped servers** tile, select the **Unmapped servers with relevant candidate** graph.

**Note:** All application service candidates have been filtered to exclude irrelevant tools, so only the most relevant candidates are presented.

2.  Review the list of servers with their associated candidates.
3.  Organize the candidate list to prioritize your work.

    |Organization method|Action|
    |-------------------|------|
    |Order|Select a column name to sort the results in ascending or descending order.|
    |Group|Select the menu \(![Menu icon](../../service-operations-workspace-itom/image/menu-icon.png)\) icon to group results by the selected column.|

4.  Select the preferred server or candidate.
5.  Select **Map application service**.


</td></tr></tbody>
</table>
## Result

The selected application service candidate is converted to an application service, and the selected unmapped servers are mapped.

**Parent Topic:**[Using Service Mapping](../concept/using-service-mapping.md)

