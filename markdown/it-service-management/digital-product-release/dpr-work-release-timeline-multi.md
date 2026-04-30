---
title: Work on a timeline-oriented release for multiple products
description: Monitor and work on a release that follows the timeline-oriented release process for multiple products.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 5
breadcrumb: [Timeline-oriented releases, Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Work on a timeline-oriented release for multiple products

Monitor and work on a release that follows the timeline-oriented release process for multiple products.

## Before you begin

Role required: sn\_dpr\_model.product\_manager or sn\_dpr\_model.release\_admin

## About this task

When working on a release for multiple products, you can choose to work with the main release \(for the primary product or service\) or a specific release \(for an Included product\). The main release controls and executes all activities for each product release under it.

-   Perform primary activities, like starting the release and managing phases and tasks in the main release.
-   Define the release scope and manage change requests in each product release.
-   Run policies for the current phase either from the main release level or an individual product release. The policy statuses from the individual product releases are aggregated into the policy status of the main release. For more information about how the aggregated status is derived, see [Policy status aggregation in a multi-product release](../reference/dpr-policy-status-aggregation.md).

You can monitor the progress of an individual product release, or you can track the overall progress at the main release level.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).

3.  Select a release from the list to open.

4.  Select the **Details** tab and add or update the schedule in the **Schedule** list to account for holidays during the release period.

    The list shows schedule entries that are of the type Excluded from the Schedule \[cmn\_schedule\] table.

    **Note:** The selected schedule must be within the release duration \(release target date\).

    The phase start and end dates are updated and the release duration is recalculated by considering the non-working days in the schedule. For more information on how schedules impact the dates of phases and release target, see [Holiday schedules in a release](../concept/dpr-release-holiday-schedule.md).

5.  If the release isn't in progress, select **Start release**.

6.  Select **Dashboard** to monitor the overall status of the release, see the details and all products that have their individual releases.

    -   Select the **Release dashboard** tab to view important dates of the release, release tasks, policies, related tasks, and approvals by their state for all releases together.

        For more information, see [Release dashboard for a multi-product release](../concept/dpr-release-dashboard-multi.md).

    -   Select the **Details** tab to make any necessary changes to the release details, such as the release name, owner, status, or description. For more information, see [Review and update release details](dpr-work-release-details.md).
    -   Select the **Products** tab to view a list of all products, including their release versions and statuses.
7.  In the **Products** tab, add or remove a product from the release as the scope and requirements of the release evolve.

    For more information, see [Add a product to a multi-product release](dpr-add-product-release.md) and [Remove a product from a multi-product release](dpr-remove-product-release.md).

8.  Select a product or service to work on its release from the **View by** drop-down list.

    Based on the selected option, you can see different sections as follows:

<table id="table_rnl_swl_b2c"><thead><tr><th>

View by option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All products or services

</td><td>

You can see the following sections:-   **Release execution**: Work on the main release, which involves starting the release, [retargeting the release](dpr-work-release-readiness-target.md), and [executing the release](dpr-work-release.md#) to manage phases, tasks, key dates, policies, and approvals. All of these actions apply to all releases.
-   **Change requests**: View a list of all change requests across releases for all products or service.


</td></tr><tr><td>

Included product

</td><td>

You can see the following sections for the selected product's release:-   **Overview**: View the progress and quality of the release on the respective dashboards. For more information, see [Release Overview dashboard for a multi-product release](../concept/dpr-release-overview-dashboard-multi.md) and [Release Quality dashboard](../concept/dpr-release-quality-dashboard.md).
-   **Release execution**: View the details of phases of the release or run policies mapped to its phases for compliance checks. For more information, see [Execute the release](dpr-work-release.md#).

**Note:** In the **Details** tab, the **Policy status** field displays a combined compliance status for all releases.

-   **Release scope**: View and [update the scope of the release](dpr-work-release-scope.md), including product enhancements, planning items, and related tasks such as incidents and problems associated with the release.
-   **Configuration items**: View and [manage configuration items](dpr-work-release-config-items.md) related to the release.
-   **Change requests**: View and [manage change requests](dpr-work-release-change-request.md) related to the release.
-   **Release notes**: Create, publish, and share release notes for the release. You can add release notes manually or generate using AI. For more information, see [Generate AI-powered release notes for a release](dpr-generate-release-notes.md).
On the Release form header, select the number under the **Artifacts** label to manage artifacts in the release. The **Artifacts** label is available in the **Overview**, **Release scope**, **Configuration items**, and **Change requests** sections. For more information, see [Manage artifacts in a release](dpr-work-release-artifact.md).

</td></tr></tbody>
</table>9.  Close a release after verifying its completeness.

    For more information, see [Close a release](dpr-complete-release.md).


