---
title: Release Overview dashboard
description: The Release Overview dashboard provides an overview of all the information about a release, which the product team can use to assess its readiness.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Release dashboards, Explore, Digital Product Release, IT Service Management]
---

# Release Overview dashboard

The Release Overview dashboard provides an overview of all the information about a release, which the product team can use to assess its readiness.

![Release Overview dashboard provides high-level information about a release and its progress.](../image/dpr-release-dashboard.png)

## Required ServiceNow AI Platform roles

sn\_dpr\_model.product\_manager, sn\_dpr\_model.release\_admin, sn\_dpr\_model.release\_coordinator, or sn\_dpr\_model.release\_user, needed to see the dashboard.

## Access the Release Overview dashboard

To open the dashboard, navigate to **Workspaces** &gt; **Digital Product Release Workspace**. Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\) and then select a release from the Releases list.

## Widgets

<table id="table_n4k_xm2_c1c"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Release start date

</td><td>

Start date of the release.If the release isn’t started, the planned start date is shown. After the release starts, the actual start date is shown.

</td></tr><tr><td>

Release end date

</td><td>

End date of the release.If the release isn’t closed, the planned end date is shown. After the release is closed, the actual end date is shown.

</td></tr><tr><td>

Release target date

</td><td>

Readiness target date of the release.

</td></tr><tr><td>

Risk score

</td><td>

Risk level of a release. This score is calculated based on the overdue tasks and policy failures.For more information, see [Risk score for a release](dpr-risk-score-release.md#).

</td></tr><tr><td>

Release tasks

</td><td>

Number of tasks in the release, grouped by their state.

</td></tr><tr><td>

Change requests

</td><td>

Total number of change requests in different phases of the release, grouped by their state.

</td></tr><tr><td>

Enhancements

</td><td>

Product enhancements in the release, grouped by their state.

</td></tr><tr><td>

Work items

</td><td>

Work items in the release, grouped by their type, and stacked by their state.

</td></tr><tr><td>

Related tasks

</td><td>

Related tasks linked to the release, grouped by their type, and stacked by their state.

</td></tr><tr><td>

Policies

</td><td>

List of all policies, grouped by the phases they’re mapped to.

</td></tr><tr><td>

Approvals

</td><td>

List of all approval tasks, grouped by their approval status.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Product Release dashboards](dpr-dashboard-release.md)

**Related topics**  


[Release Quality dashboard](dpr-release-quality-dashboard.md)

[Release dashboard for a multi-product release](dpr-release-dashboard-multi.md)

[Release Overview dashboard for a multi-product release](dpr-release-overview-dashboard-multi.md)

