---
title: Confirm a planning scenario
description: Select and confirm a scenario to allocate budget and resources for executing the selected demands and projects in a fiscal year.
locale: en-US
release: australia
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Scenario Planning for PPM, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Confirm a planning scenario

Select and confirm a scenario to allocate budget and resources for executing the selected demands and projects in a fiscal year.

## Before you begin

Ensure that you have created up to four planning scenarios and selected projects and demands for execution. For more information, see [Create planning scenarios](create-scenarios.md) and [Select demands and projects for portfolio planning](select-prj-demands.md).

Role required: it\_portfolio\_manager

## Procedure

1.  Navigate to Portfolio Planning Workbench from either of two starting points.

<table id="choicetable_xfs_1fh_jlb"><thead><tr><th align="left" id="d156957e66">

Location

</th><th align="left" id="d156957e69">

Steps

</th></tr></thead><tbody><tr><td id="d156957e75">

**From application navigator**

</td><td>

1.  Navigate to **Project** &gt; **Portfolios** &gt; **Portfolio Planning Workbench**.
2.  From the **Portfolio** list, select the portfolio that you want to perform the planning for.


</td></tr><tr><td id="d156957e108">

**From the portfolio list**

</td><td>

1.  Navigate to **Project** &gt; **Portfolios** &gt; **All**.
2.  Open the portfolio that you want to perform the planning for.
3.  In the Portfolio form, click the **Portfolio Planning** related link.


</td></tr></tbody>
</table>2.  In the Project Planning Workbench, confirm a scenario as your current plan for the fiscal year using one of the following options:

    -   Select a scenario and click **Confirm**.
    -   Click **Compare Scenarios** and, in the Compare Scenarios page, click **Confirm Scenario**.
    -   If you are overriding an already confirmed plan , click **Override**.
3.  In the Confirm dialog box, set additional options to be performed on the selected demands and projects after the planning scenario is saved.

    **Note:** When a confirmed plan exists, the name of the dialog box is Override Selection rather than Confirm.

    -   If the [project property](../../project-management/reference/r_InstalledWithProjectManagement.md) **Create project\(s\) on confirming demands from portfolio workbench** is set to false, you can choose to approve all the selected demands after the save by selecting **Approve all selected demands \(if not approved already\)**.
    -   If the [project property](../../project-management/reference/r_InstalledWithProjectManagement.md) **Create project\(s\) on confirming demands from portfolio workbench** is set to true, you can choose to convert the selected demands to projects after the save by selecting **Convert all the selected demands to projects**.
    -   Confirm the resources for selected demands and projects by selecting **Confirm resources for selected demands or projects**.
    -   If the confirmed and allocated resource plans associated with the demands and projects that are newly unselected do not have any actual hours associated with them, then select **Unconfirm the resources for the unselected demands and projects \(only those resources where there is no actual hours/cost captured will be unconfirmed\)** to change the state of such resource plans to requested. If the confirmed and allocated resource plans have actuals associated with them, a notification is send to the project or demand managers specifying that they need to manually release such resources.
    -   Delete all the unconfirmed working scenarios after confirmation of the selected scenario by selecting **Delete all working scenarios**. This option is selected by default.
4.  Click **Save**.


## Result

Budget is allocated to selected demands and projects. The remaining demands and projects are removed from execution. However, resources already confirmed for the unselected demands and projects are not removed automatically.

**Parent Topic:**[Scenario Planning for PPM](../concept/portfolio-planning-overview.md)

