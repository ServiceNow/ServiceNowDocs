---
title: Release Overview dashboard
description: The Release Overview dashboard provides an overview of all the information about a release, which the product team can use to assess its readiness.
locale: en-US
release: xanadu
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2025-04-25"
reading_time_minutes: 3
breadcrumb: [Digital Product Release dashboards, Exploring Digital Product Release, Digital Product Release, IT Service Management]
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

Risk level of a release. This score is calculated based on the overdue tasks and policy failures. For more information, see the calculation of the risk score in the following section.

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
</table>## Calculation of risk score of a release

The risk score of a release combines overdue task scores and policy failure scores, weighted by their respective importance. The weight or priority to overdue tasks and policy failure determines their urgency or impact on a release. The overdue task score is categorized based on the percentage of overdue tasks. The policy failure score is determined by the percentage of failed policies.

Given `overdue_weight + policy_failure_weight = 1`, the risk score of a release is calculated according to the following formula:

`Risk score = Round((Overdue task score * overdue_weight + Policy failure score * policy_failure_weight) * (Number of days elapsed in release / Total number of days in release))`

Where each metric is calculated as follows:

-   **Overdue task score:**

    -   If &lt;10% of tasks are overdue, the overdue task score is 0.
    -   If 10-40% of tasks are overdue, the overdue task score is 1.
    -   If &gt;40% of tasks are overdue, the overdue task score is 2.
    If a task has no end date, the phase's end date is used as the task's due date.

-   **Policy failure score:**
    -   If &lt;10% of policies fail, the policy failure score is 0.
    -   If 10-40% of policies fail, the policy failure score is 1.
    -   If &gt;40% of policies fail, the policy failure score is 2.

Based on the calculated risk score, the release is categorized into one of the following risk levels:

-   Low, if the value is 0 or 1
-   Medium, if the value is 2
-   High, if the value is 3
-   Very high, if the value is 4

This categorization can help you determine the risks involved with the release, thus enabling you to take measures to reduce these risks in a timely manner.

**Parent Topic:**[Digital Product Release dashboards](dpr-dashboard-release.md)

**Related topics**  


[Release Quality dashboard](dpr-release-quality-dashboard.md)

[Release dashboard for a multi-product release](dpr-release-dashboard-multi.md)

[Release Overview dashboard for a multi-product release](dpr-release-overview-dashboard-multi.md)

