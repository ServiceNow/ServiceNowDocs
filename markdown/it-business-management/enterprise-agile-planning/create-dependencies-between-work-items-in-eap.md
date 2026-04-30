---
title: Create and manage dependencies between work items in EAP
description: Draw work item dependencies in real-time across teams and iterations and visually analyze them while you collaborate using the Planning board in Enterprise Agile Planning.
locale: en-US
release: xanadu
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work item dependencies in EAP, Perform PI planning, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create and manage dependencies between work items in EAP

Draw work item dependencies in real-time across teams and iterations and visually analyze them while you collaborate using the Planning board in Enterprise Agile Planning.

## Before you begin

Role required: sn\_apw\_advanced.eap\_user

## About this task

This task is explained using stories in an Agile Release Train \(ART\) as an example, which has Planning Interval \(PI\) as its calendar. The same guidance applies to creating, updating, and deleting dependencies for work items of an Agile Team, Solution Train, or Portfolio.

-   A story that has a dependency on it by another story is called a prerequisite story.
-   A story that is dependent on another story is called the dependent story.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  From the Agile structure section of the left navigation panel, choose your EAP team.

3.  Identify stories that have dependencies, and use the interactive functionality of the Planning board to draw dependency lines between them.

    1.  On the dependent story card, click the Add dependency line icon \(![Add dependency line icon.](../images/eap-dependency-add-icon.png)\).

        A dotted dependency line appears.

    2.  Select the prerequisite story card to finish drawing the dependency line.

    ![Draw dependency lines between stories on the Planning Board in EAP.](../images/eap-create-dependency.gif)

    The dependencies are added to the work items on the board.

4.  If the dependency line color is Yellow or Red, review it and reschedule stories as required.

5.  Delete a dependency, to account for any change in the requirements.

    1.  Navigate to the full details page of a work item card that has a dependency to it.

    2.  From the Prerequisite Stories or the Dependent Stories related lists, locate the dependency that you want to remove.

        **Note:** The names of these related lists are different for Epic and Solution Train.

    3.  From the Sys class name column, select **Story Dependencies**.

        ![Dependencies related lists for a work item.](../images/eap-delete-dependency-1.png)

    4.  From the dependency item header, select the More Actions icon \(![More Actions icon.](../images/eap-more-actions-icon.png)\) and select **Delete**.

    5.  Select **OK** to confirm deleting the dependency.


**Parent Topic:**[Work item dependencies in EAP](../concept/work-item-dependencies-in-eap.md)

