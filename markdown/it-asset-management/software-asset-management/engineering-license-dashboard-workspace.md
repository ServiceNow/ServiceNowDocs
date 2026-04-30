---
title: Engineering License overview dashboard in workspace
description: Monitor and gain insights into your engineering applications license position and usage by viewing product usage reports in the Engineering license overview dashboard.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Software asset analytics view, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Engineering License overview dashboard in workspace

Monitor and gain insights into your engineering applications license position and usage by viewing product usage reports in the Engineering license overview dashboard.

The Engineering license overview dashboard displays reports on normalized products and publishers that belong to engineering applications such as AutoCAD, GIS.

To narrow your results based on products or publishers across all tabs, use the filter in the left-hand corner of the dashboard. You can further narrow your results based on the date, user, or license server.

**Note:** Only products and publishers that belong to engineering applications and are listed in the Engineering Application License \[samp\_eng\_app\_license\] table appear in the filter. If no product or publisher is selected, the cumulative data for all products and publishers that belong to engineering applications appear.

All the reports are updated daily or whenever a new reconciliation result is available.

You can access the Engineering license overview dashboard by navigating to **Software asset** &gt; **Software Asset Workspace** &gt; **Software asset analytics** &gt; **Engineering license overview**.

![Engineering Overview dashboard in workspace](../image/engineering-dboard-workspace.png "Engineering license overview dashboard")

<table id="table_xts_cjh_dpb"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total spend

</td><td>

Product Result

 \[samp\_product\_result\]

</td><td>

Total cost of all entitlements for all products.

</td></tr><tr><td>

Potential savings

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

Cost saved if removal candidates are reclaimed.

</td></tr><tr><td>

Top denied products

</td><td>

Engineering Application Denial \[samp\_eng\_app\_denial\]

</td><td>

Top products that are denied to users as these products have reached their peak concurrent usage.

</td></tr><tr><td>

Utilization and user ratio

</td><td>

Engineering Application Utilization and User Ratio \[samp\_eng\_utilization\_user\_ratio\]

</td><td>

Ratio of license utilization, for normalized products and publishers, to the number of users using those licenses.

-   Normalized publisher
-   Normalized product
-   License utilization: Percentage of peak consumption of the product against number of rights.
-   License to user ratio: Ratio of rights using this license to users using this product over the period of 90 days rights.

</td></tr><tr><td>

License usage over time

</td><td>

Engineering Application License \[samp\_eng\_app\_license\]

 Engineering Application Concurrent Usage \[samp\_eng\_app\_concurrent\_usage\]

 Engineering Application Denial \[samp\_eng\_app\_denial\]

</td><td>

The total number or quantity of all available licenses; not just the active products but all the products.

-   The blue line represents the total number of licenses allocated to a product or a publisher
-   The green line indicates the concurrent usage of the licenses.
-   The red line indicates denials or if and when the concurrent usage peaks.

</td></tr><tr><td>

User session summary

</td><td>

Engineering Application Usage Summary \[samp\_eng\_app\_usage\_summary\]

</td><td>

Duration of time spent by users \(idle vs active\) on products. Only the top 5 users with more idle duration appear on the report.

**Note:** Idle is the aggregate sum on Total idle duration column and Active is the aggregate sum on Total session duration column.

</td></tr><tr><td>

Top denied users

</td><td>

Engineering Application Denial \[samp\_eng\_app\_denial\]

</td><td>

Top users that are denied licenses to products.

</td></tr></tbody>
</table>