---
title: Tag Governance dashboard – Overview tab
description: The Overview tab tracks the health and compliance of CIs based on tag audits. Interactive widgets provide information that enables you to view and analyze tag compliance status and the most-used and least-used tags.
locale: en-US
release: xanadu
product: Tag Governance
classification: tag-governance
topic_type: concept
last_updated: "2024-08-06"
reading_time_minutes: 2
breadcrumb: [Exploring Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Tag Governance dashboard – Overview tab

The **Overview** tab tracks the health and compliance of CIs based on tag audits. Interactive widgets provide information that enables you to view and analyze tag compliance status and the most-used and least-used tags.

## Accessing the dashboard

Log in as a Tag Governance administrator \(sn\_itom\_tag.tag\_governance\_admin\) to configure reports and Tag Governance Viewer \(sn\_itom\_tag.tag\_reports\_viewer\) view the reports. To access the dashboard, navigate to **Tag Governance** &gt; **Dashboard**.

![Overview tab](../image/tag-health-dashboard.png "Overview tab")

## Applying filters

The Health tab displays the cumulative status of the tag health of all CIs that the tag audits ran on. Each category indicates the percentage and the count of CIs with a matching status.

By default, data is grouped by status. You can also group the results by using the filters in the **Group By** list.

Use the following interactive filters to refine reports:

-   **Cloud Service Account**
-   **Logical Datacenter**
-   **CMDB Class**

    **Note:** The **CMDB Class** filter only applies to the **Tag Health** report. Using this filter does not impact or refine the results of the **Most Popular Tags** and the **Least Used Tags** reports.


For example, you can use a combination of the **Cloud Service Accounts**, **CMDB Class**, and **Logical Datacenter** filters. You can then view the tag audit results for the virtual machine instances that are mapped to a specific cloud service account and are located in a specific logical datacenter.

## Reports

Tag audits run on all discovered resources in the CMDB CI \[`cmdb_ci`\] table. The tab displays health and compliance results for discovered CIs.

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Widget

</th><th>

Description

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health

</td><td>

Pie chart

</td><td>

Percentage and count of all CIs in the following categories:-   Non Compliant: CIs that meet none of the tag policy requirements.
-   Partial Compliant: CIs that meet some tag policy requirements.
-   Fully Compliant: CIs that meet all tag policy requirements.

Select any related slice or category to view a more detailed report.

</td></tr><tr><td>

Most Popular Tags

</td><td>

Bar chart

</td><td>

The ten most commonly used tags across all discovered CIs that tag audits evaluate. -   Point to a bar to view the corresponding percentage of the total and count of the tag's occurrence.
-   Select a bar to view the list of CIs with that tag.

</td></tr><tr><td>

Least Used Tags

</td><td>

Bar chart

</td><td>

The ten least used tags across all discovered CIs that tag audits evaluate. -   Point to a bar to view the corresponding percentage of the total and count of the tag's occurrence.
-   Select a bar to view the list of CIs with that tag.

</td></tr></tbody>
</table>