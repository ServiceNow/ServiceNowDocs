---
title: Release dashboard for a multi-product release
description: The Release Overview dashboard for a multi-product release provides an overview of all the information about every product release, which the product team can use to assess the release readiness.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/dpr-release-dashboard-multi.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Release dashboards, Explore, Digital Product Release, IT Service Management]
---

# Release dashboard for a multi-product release

The Release Overview dashboard for a multi-product release provides an overview of all the information about every product release, which the product team can use to assess the release readiness.

\[Omitted image "dpr-release-dashboard-multi.png"\] Alt text: Release dashboard provides high-level information for all the product releases in a multi-product release.

## Required ServiceNow AI Platform roles

sn\_dpr\_model.product\_manager, sn\_dpr\_model.release\_admin, sn\_dpr\_model.release\_coordinator, or sn\_dpr\_model.release\_user, needed to see the dashboard.

## Access the Release Overview dashboard

To open the dashboard, navigate to **Workspaces** &gt; **Digital Product Release Workspace**. Select the releases icon \(\[Omitted image "dpr-icon-release.png"\] Alt text: Releases icon.\) and then select a multi-product release from the Releases list. Select **All products** in the **View by** to view the Release dashboard.

## Widgets

<table id="table_fk1_ksq_sdc"><thead><tr><th>

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

**Note:** This widget is applicable only for timeline-oriented releases.

</td></tr><tr><td>

Release target date

</td><td>

Readiness target date of the release.

</td></tr><tr><td>

Release Tasks

</td><td>

Number of tasks across all releases, grouped by their state.

</td></tr><tr><td>

Policies

</td><td>

Number of policies across all releases, grouped by products and stacked by their run status.

</td></tr><tr><td>

Approvals

</td><td>

Number of approval tasks across all releases, grouped by their state.

</td></tr><tr><td>

Enhancements

</td><td>

Number of enhancements across all releases.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Product Release dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-dashboard-release.md)

**Related topics**  


[Release Overview dashboard]()

[Release Quality dashboard]()

[Release Overview dashboard for a multi-product release]()

