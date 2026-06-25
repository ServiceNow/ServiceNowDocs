---
title: Release Overview dashboard for a multi-product release
description: The Release overview dashboard provides an overview of all the information about an individual product's release in a multi-product release, which the product team can use to assess its readiness.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/dpr-release-overview-dashboard-multi.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Release dashboards, Explore, Digital Product Release, IT Service Management]
---

# Release Overview dashboard for a multi-product release

The Release overview dashboard provides an overview of all the information about an individual product's release in a multi-product release, which the product team can use to assess its readiness.

\[Omitted image "dpr-release-overview-multi.png"\] Alt text: Release Overview dashboard provides high-level information about a single product or service release and its progress.

## Required ServiceNow AI Platform roles

sn\_dpr\_model.product\_manager, sn\_dpr\_model.release\_admin, sn\_dpr\_model.release\_coordinator, or sn\_dpr\_model.release\_user, needed to see the dashboard.

## Access the Release Overview dashboard

To open the dashboard, navigate to **Workspaces** &gt; **Digital Product Release Workspace**. Select the releases icon \(\[Omitted image "dpr-icon-release.png"\] Alt text: Releases icon.\) and then select a release from the Releases list.

## Widgets

<table id="table_n4k_xm2_c1c"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk score

</td><td>

Risk level of a release. This score is calculated based on the overdue tasks and policy failures.For more information, see [Risk score for a release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-risk-score-release.md).

</td></tr><tr><td>

Release tasks

</td><td>

Number of tasks in the release, grouped by their state.

</td></tr><tr><td>

Change requests

</td><td>

Number of change requests in the release, grouped by their state.

</td></tr><tr><td>

Policies

</td><td>

Number of policies for the selected product release, grouped by their run status.

</td></tr><tr><td>

Approvals

</td><td>

Number of approval tasks for the selected product release, grouped by their state.

</td></tr><tr><td>

Enhancements

</td><td>

Number of product enhancements in the release, grouped by their state.

</td></tr><tr><td>

Work items

</td><td>

Number of work items in the release, grouped by their type, and stacked by their state.

</td></tr><tr><td>

Related tasks

</td><td>

Number of related tasks \(incidents, problems\) linked to the release, grouped by their type, and stacked by their state.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Product Release dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-dashboard-release.md)

**Related topics**  


[Release Overview dashboard]()

[Release Quality dashboard]()

[Release dashboard for a multi-product release]()

