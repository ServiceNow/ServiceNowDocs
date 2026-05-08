---
title: Plan product enhancements into different releases
description: Move product enhancements into different releases of the product or service to plan the scope of your release.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Digital Product Release, IT Service Management]
---

# Plan product enhancements into different releases

Move product enhancements into different releases of the product or service to plan the scope of your release.

## Before you begin

You can only plan releases that have the validates version option set to true.

Role required: sn\_dpr\_model.product\_manager

## About this task

Release planning is done using the Kanban board. The vertical lanes represent releases that are in the Draft or Pending state. The cards in each release lane represent product enhancements associated with the release.

When linking a plan version fromServiceNow® Agile Development 2.0, Jira, or GitLab, you can select the **Auto-create product versions from plan versions** option. Selecting this option automatically creates a release associated with one of the following, depending on the tool you select:

-   A Fix version created in Jira.
-   A Milestone created in GitLab.
-   A Release created in Agile Development 2.0.

When a release is created from a version from one of these planning tools, the product enhancements are planned for the appropriate release as well. This option verifies that the release planning in DPR reflects the planning state from the planning tool.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the products and services icon \(![Products and services icon.](../image/dpr-icon-products.png)\).

3.  Select a product or service from the list to open.

4.  Select **Release planning**.

    The Release planning page shows a Kanban board with lanes for the backlog and each product release. Only the releasesthat validate versions and are in Draft or Pending states are shown. You can identify the draft releases by the lane header color or the word \(Draft\) at the end of the release name. The release lanes are sorted by the order of the release creation date, from the most recent to the oldest.

    Enhancements are displayed as cards in the release lane they are associated with.

5.  View a release in the Pending state by selecting the sub menu icon \(![Sub menu icon.](../image/dpr-icon-menu.png)\) of a release lane and select the **View release** option.

6.  On the Kanban board, complete your release planning.

<table id="choicetable_y4q_fgr_lyb"><thead><tr><th align="left" id="d394549e195">

Action

</th><th align="left" id="d394549e198">

Steps

</th></tr></thead><tbody><tr><td id="d394549e204">

**Move an enhancement into a release**

</td><td>

Select an enhancement card and drag to move it from backlog to a release or between releases.

</td></tr><tr><td id="d394549e213">

**Add an enhancement**

</td><td>

1.  Select **Add enhancement**.
2.  On the Add enhancement dialog box, add details for the enhancement, and select **Confirm**.

For more information, see [Add an enhancement to a product or service](dpr-create-product-enhancement.md).

</td></tr><tr><td id="d394549e249">

**Add an enhancement from an epic**

</td><td>

1.  Select the more actions icon beside the **Add enhancement** button and then select **Add enhancement from epic**.

![Add enhancement from epic button.](../image/dpr-icon-enhance-epic-btn.png)

2.  On the Add enhancements from epics dialog box, select one or more epics, and then select **Add enhancements**.

For more information, see [Add a product enhancement from an epic](dpr-add-product-enhancement-from-epic.md).

</td></tr><tr><td id="d394549e294">

**Prioritize enhancements in a release**

</td><td>

Rearrange enhancement cards within a release in order of priority. The enhancement card positioned at the top of the release lane is given the highest ranking.

</td></tr><tr><td id="d394549e313">

**Create a release**

</td><td>

-   To create a release using a wizard, select **Create release**.

For more information, see [Create a release with a wizard](dpr-create-release-guided.md).

-   To create a release for a single product or service, select the more actions icon beside the **Create release** button and then select **Quick create**.

For more information, see [Create a release for a product or service](dpr-create-release.md).

</td></tr><tr><td id="d394549e367">

**Edit a draft release**

</td><td>

1.  Select the sub menu icon \(![Vertical lane action icon.](../image/dpr-icon-menu.png)\) of a release lane and select the **Edit release** option.
2.  On the Release details page, modify the details and complete the release creation process. For more information, see [Create a release with a wizard](dpr-create-release-guided.md).


</td></tr></tbody>
</table>
**Parent Topic:**[Using Digital Product Release](../concept/dpr-using-digital-product-release.md)

