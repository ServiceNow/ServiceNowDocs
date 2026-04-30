---
title: View Tag Governance metrics
description: View metrics like tag policy coverage, compliance status, and usage trends on the Tag Governance Insights dashboard.
locale: en-US
release: zurich
product: Tag Governance
classification: tag-governance
topic_type: concept
last_updated: "2026-02-13"
reading_time_minutes: 3
keywords: [Tag Governance Insights dashboard, Tag policy coverage, Overall compliance status, CI compliance by infrastructures, Compliance trends, Most used tags, Least used tags]
breadcrumb: [Exploring Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# View Tag Governance metrics

View metrics like tag policy coverage, compliance status, and usage trends on the Tag Governance Insights dashboard.

## Before you begin

Verify the following:

-   To be able to configure reports, log in as a Tag Governance admin \(sn\_itom\_tag.tag\_governance\_admin\).
-   To be able to view reports, log in as a report viewer \(sn\_itom\_tag.tag\_reports\_viewer\).
-   Tag policies must be configured and audits must be run to populate data. For more information, see [Configure a tag policy for Tag Governance](../task/configure-tag-governance-policy.md).

## Access the dashboard

To access the dashboard, navigate to **Tag Governance** &gt; **Dashboard**.

## Dashboard details

The Tag Governance Insights dashboard displays metrics that help you make data-driven decisions, like identify tag compliance gaps, introduce tag policy adoption initiatives, assess tag compliance status, and more. For example, you can view the least used tags and decide whether they require remediation or deprecation. You can also drill down into each widget to view a list of relevant configuration items \(CIs\) and edit, save, or export them.

**Note:** The dashboard displays results from tag audit runs on discovered CIs from the CMBD CI \[cmdb\_ci\] table.

<table id="table_djj_ywn_g3c"><thead><tr><th>

Widget

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tag policy coverage

</td><td>

Pie chart

</td><td>

Displays the total count of discovered CIs and CIs that are governed and ungoverned by a tag policy.Hover over a pie segment to view the total count and percentage of CIs for that category. Select it to view the detailed tag quality state list.

</td></tr><tr><td>

Overall compliance status across CIs

</td><td>

Pie chart

</td><td>

Displays the overall compliance status of all discovered CIs. The possible statuses are:-   Non Compliant: CIs that don't meet any tag policy requirements.
-   Partially Compliant: CIs that meet some tag policy requirements.
-   Fully Compliant: CIs that meet all tag policy requirements.

Hover over a pie segment to view the total count and percentage of CIs for that category. Select it to view the tag policy health list.

You can filter by cloud accounts, datacenters, and policy type for specific results. For example, you can combine filters to view the tag compliance status for virtual machine instances mapped to a specific cloud account in a relevant datacenter.

**Note:** The dashboard fetches cloud account and datacenter records directly from the Tag Compliance Aggregate Counts \[sn\_itom\_tag\_widget\_aggregate\_counts\] table, displaying only cloud accounts and datacenters that have associated compliance CIs.

</td></tr><tr><td>

CI compliance by infrastructures

</td><td>

Stacked bar chart

</td><td>

Displays the compliance distribution across datacenters and cloud accounts. Each bar represents an infrastructure location with each bar segment representing their CI compliance status.Hover over a bar segment to view the total count and percentage of CIs for that category. Select it to view the tag policy run list.

**Note:** The chart displays the data of top ten datacenters or cloud accounts by CI count. If there are more than ten infrastructure locations, the remaining data is combined into one bar.

</td></tr><tr><td>

Compliance trends over the past 90 days

</td><td>

Line trend report

</td><td>

Displays the compliance performance trends over the previous 90 days for CIs according to their compliance status.Hover over a point on the line trend to view the total count and percentage of CIs for that category. Select it to view the tag policy run list.

</td></tr><tr><td>

Most used tags in the past 90 days

</td><td>

Pareto chart

</td><td>

Displays the most used tags across all CIs over the previous 90 days.Hover over a bar to view the total count and percentage of CIs for that category. Select it to view the tag report key counts list.

**Note:** The chart displays the data of top ten tags by CI count. If there are more than ten tags, the remaining data is combined into one bar.

</td></tr><tr><td>

Least used tags

</td><td>

Horizontal bar chart

</td><td>

Displays the least used tags across all CIs.Hover over a bar to view the total count and percentage of CIs using the tag. Select it to view the tag report key counts list.

**Note:** The chart displays the data of the ten least used tags by CI count. If there are more than ten tags, the remaining data is combined into one bar.

</td></tr></tbody>
</table>For more information about tag audit results and non-compliant CIs, see [Preview and remediate tag audit failures](../task/perform-remediations-tag-governance.md).

