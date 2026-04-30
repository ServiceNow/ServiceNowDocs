---
title: Normalization and content dashboard
description: View normalization trend charts on the Normalization and content dashboard, which is integrated with Performance Analytics in Software Asset Workspace.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Software asset analytics view, Software Asset Workspace, Explore, Software Asset Management, IT Asset Management]
---

# Normalization and content dashboard

View normalization trend charts on the Normalization and content dashboard, which is integrated with Performance Analytics in Software Asset Workspace.

Normalization chart results are updated daily when the **SAM - Discovery Model Normalization** job is run.

You can filter the count of installations based on a publisher or product by using the Publisher or Product filter.

You can access the Normalization and content dashboard by navigating to **Workspaces** &gt; **Software Asset Workspace** &gt; **Software asset analytics** &gt; **Normalization and content**.

![Normalization and content dashboard view](../image/normalization-dashboard-workspace.png "Normalization and content dashboard")

<table id="table_pp1_2fh_rpb"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Percentage of normalized installs

</td><td>

Software Discovery Models \[cmdb\_sam\_sw\_discovery\_model\]

</td><td>

The percentage of fully normalized software installations out of the total software installations. You can view the percentage of installations by using the filter publisher or product.

</td></tr><tr><td>

Software installs normalization status

</td><td>

Software Discovery Models \[cmdb\_sam\_sw\_discovery\_model\]

</td><td>

Count of software installations based on the normalization status.

 Select a normalization status on the donut chart to view the list of discovery models along with the installation count for each discovery model. You can further select a discovery model to view the list of software installations.

 The report for this widget is populated only once the following daily scheduled jobs have run successfully:

-   **SAM - Normalize discovery models using content library rules**
-   **SAM - Daily Job**

</td></tr></tbody>
</table>## Central Data Service Download Status

The Central Data Service Download Status related list is updated daily when the **SAM - Central Data Service Download Status** job is run.

|Field|Description|
|-----|-----------|
|Name|Table name from which the content is pulled.|
|Current count|Number of records in the table.|
|Expected count|Expected number of records in the table.|
|Last updated on|Last date and time the data was pulled.|
|Next action|Next scheduled date and time to pull data from the table.|

