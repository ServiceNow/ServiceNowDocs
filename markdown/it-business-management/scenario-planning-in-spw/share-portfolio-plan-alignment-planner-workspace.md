---
title: Share a portfolio plan with stakeholders
description: Share your portfolio plan with stakeholders and other planning managers so that they have visibility into the plan's progress and start collaborating.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage portfolio plans, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Share a portfolio plan with stakeholders

Share your portfolio plan with stakeholders and other planning managers so that they have visibility into the plan's progress and start collaborating.

## Before you begin

-   [Create a portfolio plan](create-portfolio-plans-in-alignment-planner-workspace.md).
-   Users or groups that you want to share the portfolio plan with must have the sn\_align\_core.ap\_read\_only or sn\_align\_core.apw\_user role to get the read or edit access to the portfolio plan respectively.

Role required: sn\_align\_core.apw\_user or business\_stakeholder

## About this task

Select individual users or groups to share the portfolio with.

When you share a portfolio plan with an individual user or a group, they can access the following data of the portfolio plan:

-   Planning page
    -   Prioritization, Roadmap, Kanban, Hierarchy tabs by default
    -   Capacity tab if the user has the sn\_align\_ws.spw\_capacity\_user or sn\_align\_ws.spw\_capacity\_read role
    -   Financials tab if the user has sn\_align\_ws.spw\_financial\_user role
-   Goals page if the user has the sn\_apw\_advanced.spw\_goal\_user role
-   Scoring page if the user has the sn\_align\_core.apw\_user role

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select one.

3.  From the portfolio plan header in the Planning page, select the **Share portfolio plan** icon \(![Share portfolio plan with users and groups](../images/icon-share-pp.png)\).

4.  On the Share portfolio plan form, select users to share the portfolio plan with and set their access appropriately.

    1.  In the **Members or Groups** field, enter the names of individual users or groups.

    2.  From the **Access** field, select the access level as **Viewer** or **Editor** for the selected names.

        -   An editor can view and change the portfolio plan's settings and data.
        -   A viewer can comment and add attachments to the portfolio plan, but cannot modify the portfolio plan's settings or data.

            **Note:** Even if a user has the sn\_align\_core.apw\_user role, they cannot edit planning item data from the portfolio plan grid view or side panel when granted view-only access. However, users with the sn\_align\_core.apw\_user role can edit planning items and related tables from the record page.

5.  Select **Send invite**.


## Result

The selected individual and group users are notified of the portfolio plan sharing through an email.

## What to do next

[Collaborate on a portfolio plan](collaborate-stakeholders-portfolio-plan-alignment-planner-workspace.md).

Change the access level or remove access for a user or a group.

1.  On the Share portfolio plan form, select **Manage access**.
2.  From the user or group card, select the Action Menu icon \(![Action menu icon.](../images/action-menu-icon.png)\).
3.  Select the right access level or select **Remove**.

**Parent Topic:**[Managing portfolio plans in Strategic Planning Workspace](../concept/managing-portfolio-plans-in-alignment-planner-workspace.md)

**Related topics**  


[Modify a portfolio plan](modify-the-details-of-a-portfolio-plan-alignment-planner-workspace.md)

[Show or hide the features for a portfolio plan](show-or-hide-the-features-for-your-portfolio-plan-spw.md)

