---
title: Perform a cluster analysis
description: Generate a cluster analysis on an activity, connection between activities, route, or an improvement opportunity.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cluster analysis, Analyzing and getting process insights, Using Process Mining, Process Mining, Platform Analytics]
---

# Perform a cluster analysis

Generate a cluster analysis on an activity, connection between activities, route, or an improvement opportunity.

**Before you begin**

-   [Configure a process for a clustering solution](process-configuration-clustering.md). To generate a cluster analysis, the project must have a process configured with a clustering solution on the relevant table.
-   Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin
-   An analysis can be performed on an activity, connection, improvement opportunity, or combined routes with a minimum of 100 and maximum of 300,000 records.

Run a cluster analysis in one of the following ways.

-   From the Summary and insights page:
    1.  From the Improvement Opportunities section, select a finding.
    2.  In the **Action** list, select **Requester intent \(cluster\)**.![Cluster analysis from Improvement Opportunities section](../image/cluster-analysis.png)

        **Note:** The status of the request is displayed in the same option as **In progress** until the task completes.

-   From an activity or connection on the process map:
    1.  Select an activity or connection from the process map that you want to perform a cluster analysis on.
    2.  From the metrics box, select **Investigate** &gt; **Requestor intent \(cluster\)**.

        You will get a notification that the task is running in the background. You can close the notification. When the task completes, you will be notified. You can see the details in the **Scheduled tasks** window.

        ![Cluster analysis from Analyst workbench](../image/cluster-analyst-wb.png)

    3.  From the Scheduled tasks panel or the metrics box that the cluster analysis was requested on, select **View result** after generation completes.

**Parent Topic:**[Cluster analysis](../concept/cluster-analysis.md)

**Related topics**  


[View a cluster analysis](view-cluster-analysis.md)

