---
title: Engineering License overview dashboard in workspace
description: Monitor and gain insights into your engineering applications license position and usage by viewing product usage reports in the Engineering license overview dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/engineering-license-dashboard-workspace.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software asset analytics view, Software Asset Workspace, Explore, Software Asset Management, IT Asset Management, Asset Management]
---

# Engineering License overview dashboard in workspace

Monitor and gain insights into your engineering applications license position and usage by viewing product usage reports in the Engineering license overview dashboard.

The Engineering license overview dashboard displays reports on normalized products and publishers that belong to engineering applications such as AutoCAD, GIS.

To narrow your results based on products or publishers across all tabs, use the filter in the left-hand corner of the dashboard. You can further narrow your results based on the date, user, or license server.

**Note:** Only products and publishers that belong to engineering applications and are listed in the Engineering Application License \[samp\_eng\_app\_license\] table appear in the filter. If no product or publisher is selected, the cumulative data for all products and publishers that belong to engineering applications appear.

All the reports are updated daily or whenever a new reconciliation result is available.

Access the Engineering license overview dashboard by navigating to **Workspaces** &gt; **Software Asset Workspace** &gt; **Software asset analytics** &gt; **Engineering license overview**.

\[Omitted image "engineering-dboard-workspace.png"\] Alt text: Engineering Overview dashboard in workspace

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

Total cost of entitlements for products on a concurrent license metric group that includes token, float, or network-based licenses.

</td></tr><tr><td>

Potential savings

</td><td>

Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

Potential cost savings if license rights flagged as removal candidates are reclaimed.

</td></tr><tr><td>

Top denied products

</td><td>

Engineering Application Denial \[samp\_eng\_app\_denial\]

</td><td>

Products with the highest number of access denials. These denials occur when peak concurrent usage reaches the product's licensed user limit or peak usage.

</td></tr><tr><td>

Utilization and user ratio

</td><td>

Engineering Application Utilization and User Ratio \[samp\_eng\_utilization\_user\_ratio\]

</td><td>

Ratio of license utilization, for normalized products and publishers, to the number of users using those licenses. The **Utilization and user ratio** report contains the following metrics:

-   License utilization: Percentage of peak consumption for a product against the number of rights available. For example, a product has 100 rights. If the highest number of users accessing the product is 90, the license utilization is 90%. If over a 90-day period, 200 distinct users accessed it, then the license utilization is 200%.
-   License to user ratio: Ratio of rights using this license to users of this product over 90 days period. For example, a product has 100 license rights, but over a 90-day period, 200 distinct users accessed it. The license to user ratio is 100:200, or 50%.
-   Normalized publisher
-   Normalized product

</td></tr><tr><td>

License usage over time

</td><td>

Engineering Application License \[samp\_eng\_app\_license\]

 Engineering Application Concurrent Usage \[samp\_eng\_app\_concurrent\_usage\]

 Engineering Application Denial \[samp\_eng\_app\_denial\]

</td><td>

Trend of daily concurrent usage over time.

-   The blue line indicates the user limit set in the license server configuration, which may differ from the entitlement count in Software Asset Management.
-   The green line indicates the peak concurrent usage of licenses.
-   The red line, where applicable, indicates denials or if and when the concurrent usage reaches the peak.

</td></tr><tr><td>

User session summary

</td><td>

Engineering Application Usage Summary \[samp\_eng\_app\_usage\_summary\]

</td><td>

Duration of time that users spend \(idle vs active\) on products. Only the top 5 users with more idle duration appear on the report.

**Note:** Idle is the sum of the Total idle duration column. Active is the sum of the Total session duration column.

</td></tr><tr><td>

Top denied users

</td><td>

Engineering Application Denial \[samp\_eng\_app\_denial\]

</td><td>

Users with the highest number of access denials for products.

</td></tr></tbody>
</table>