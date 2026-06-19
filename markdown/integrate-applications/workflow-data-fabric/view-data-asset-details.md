---
title: View data asset details
description: View comprehensive information about data assets on the asset detail page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/view-data-asset-details.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Finding and accessing data assets, Data Catalog, Workflow Data Fabric]
---

# View data asset details

View comprehensive information about data assets on the asset detail page.

## Before you begin

Role required: WDF Consumer \(wdf\_consumer\)

## About this task

Asset detail pages organize information into tabs for easy navigation. The Overview tab provides summary information, while additional tabs offer detailed views of specific aspects like columns, relationships, and lineage. \[Omitted image "dc-data-asset-details.png"\] Alt text: View details of a data asset

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Data catalog icon in the left sidebar.

3.  Select the data asset you want to view.

4.  On the Overview tab view the general details about the asset, such as, the name, source, columns included \(if it is a table\), the preview of [relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/explore-data-asset-relationships-dc.md) and [lineage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/explore-data-assets-lineage-dc.md).

    For table and column assets, the Overview tab also shows a Quality section with the overall data quality status, the number of rules, the number of passed rules, and when quality was last evaluated. Select **View all** to open the Quality tab.

5.  On the Columns tab, view column information for tabular assets, such as tables.

    Select a column name to browse to the details page of the column.

6.  On the Related assets tab, view the list of connected catalog assets.

7.  On the Quality tab, review data quality information for the asset.

    The Quality tab is available for table and column assets. The summary shows the overall data quality status, the total number of rules, and the number of passed rules. Quality badges awarded to the resource are also displayed here.

    The Rules table lists each rule with its source, asset type, asset name, category, status, and last run time. External data quality tools \(such as Anomalo, Soda, or Monte Carlo\) submit rule results via the Data Quality API. Use filters and search to locate a specific rule.

8.  On the Activity tab, review the activities performed on the data asset.

    The system stores the name of the user who made the change, the change details, and the timestamp. Use filters, search, and sort to locate the change you want to track.


-   **[Explore data asset relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/explore-data-asset-relationships-dc.md)**  
See the data assets, business terms, and governance objects connected to a data asset. Open the relationships view in Graph Explorer to expand, hide, and rearrange the graph.
-   **[Explore data assets lineage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/explore-data-assets-lineage-dc.md)**  
Trace the upstream sources and downstream consumers of a data asset. Open the lineage view in Graph Explorer to examine specific relationships, focus on a path, and review related asset details.

**Parent Topic:**[Finding and accessing data assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/find-access-data-assets-dc.md)

