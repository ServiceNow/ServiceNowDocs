---
title: Rank demands and projects
description: Rank demands and projects to prioritize demands and projects for their approval and execution within a portfolio.
locale: en-US
release: australia
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create planning scenarios, Scenario Planning for PPM, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Rank demands and projects

Rank demands and projects to prioritize demands and projects for their approval and execution within a portfolio.

## Before you begin

Role required: it\_portfolio\_manager

## About this task

By default, the Rank By Score list ranks demands and projects based on system-generated scores. Rank of a demand or project is specific to a fiscal year. A project can be ranked as third in FY17 but ranked sixth in FY18.

## Procedure

1.  Navigate to Portfolio Planning Workbench from either of two starting points.

<table id="choicetable_xfs_1fh_jlb"><thead><tr><th align="left" id="d186012e58">

Location

</th><th align="left" id="d186012e61">

Steps

</th></tr></thead><tbody><tr><td id="d186012e67">

**From application navigator**

</td><td>

1.  Navigate to **Project** &gt; **Portfolios** &gt; **Portfolio Planning Workbench**.
2.  From the **Portfolio** list, select the portfolio that you want to perform the planning for.


</td></tr><tr><td id="d186012e100">

**From the portfolio list**

</td><td>

1.  Navigate to **Project** &gt; **Portfolios** &gt; **All**.
2.  Open the portfolio that you want to perform the planning for.
3.  In the Portfolio form, click the **Portfolio Planning** related link.


</td></tr></tbody>
</table>2.  Adjust the rank automatically or manually.

<table id="choicetable_zyz_csk_nlb"><thead><tr><th align="left" id="d186012e145">

Action

</th><th align="left" id="d186012e148">

Steps

</th></tr></thead><tbody><tr><td id="d186012e154">

**Adjust the rank automatically**

</td><td>

1.  Go to the **Timeline View** tab of the **Plan** tab of the Portfolio Planning Workbench.
2.  Sort the projects and demands by the currency or number attribute such as ROI%, priority, and planned cost by which you want to rank the projects and demands.
3.  Click **Adjust Rank** to fill gaps in ranks if some projects are moved to the next fiscal year or canceled.

For example, if the ranks after moving or canceling some projects are 1, 2, and 5, this action adjusts the ranks as 1, 2, and 3.

4.  Click **Rank By Visual Sort** to rank projects and demands based on the attribute you chose.


</td></tr><tr><td id="d186012e192">

**Adjust the ranks manually**

</td><td>

1.  Go to the **Timeline View** tab of the **Plan** tab of the Portfolio Planning Workbench.
2.  Edit the **Rank** field.

When you change the rank of a project or demand, the ranks of other projects or demands adjust automatically. For example, if the rank for a project ranked as number 2 changes to number 4, the project ranked number 3 automatically assumes rank 2.

</td></tr></tbody>
</table>
## Example

The following table explains manual adjustment of ranks.

<table id="simpletable_ppl_4mv_jlb"><thead><tr><th>

Scenario for edit rank

</th><th>

Rank update

</th><th>

Rank before manual edit

</th><th>

Rank after manual edit

</th></tr></thead><tbody><tr><td>

If initial rank is 0 or blank and other ranks are present, then after edit, the successive ranks get incremented by 1.

</td><td>

-   Initial rank: 0
-   Edited rank: 2

</td><td>

-   **Task\_1: 0**
-   Task\_2: 1
-   Task\_3: 2
-   Task\_4: 3

</td><td>

-   Task\_2: 1
-   **Task\_1: 2**
-   Task\_3: 3
-   Task\_4: 4

</td></tr><tr><td>

If initial rank &gt; edited rank, then after edit, the successive ranks get incremented by 1.

</td><td>

-   Initial rank: 4
-   Edited rank: 1

</td><td>

-   Task\_1: 1
-   Task\_2: 2
-   Task\_3: 3
-   **Task\_4: 4**

</td><td>

-   **Task\_4: 1**
-   Task\_1: 2
-   Task\_2: 3
-   Task\_3: 4

</td></tr><tr><td>

If initial rank &lt; edited rank and there is no gap in rank sequence, then after edit, the previous ranks get decremented by 1.

</td><td>

-   Initial rank: 1
-   Edited rank: 3

</td><td>

-   **Task\_1: 1**
-   Task\_2: 2
-   Task\_3: 3
-   Task\_4: 4

</td><td>

-   Task\_2: 1
-   Task\_3: 2
-   **Task\_1: 3**
-   Task\_4: 4

</td></tr><tr><td>

If initial rank &lt; edited rank and there is a gap in rank sequence, then after edit, the successive ranks get incremented by 1.

</td><td>

-   Initial rank: 1
-   Edited rank: 4

</td><td>

-   **Task\_1: 1**
-   Task\_2: 2
-   Task\_3: 4
-   Task\_4: 5

</td><td>

-   Task\_2: 2
-   **Task\_1: 4**
-   Task\_3: 5
-   Task\_4: 6

</td></tr></tbody>
</table>**Parent Topic:**[Create planning scenarios](create-scenarios.md)

