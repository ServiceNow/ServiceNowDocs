---
title: Associate guidances for different failure codes
description: Associate guidances to paths with different failure code conditions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Associate guidances for different failure codes

Associate guidances to paths with different failure code conditions.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

![Failure code nodes](../image/ex-associate-guidances-failure-codes.png)

## Procedure

1.  Associate a guidance to the 200 path.

    1.  Select **Add node** in the 200 path.

    2.  In the pop-up window, select **Propose a guidance as an outcome** to configure a guidance node.

        A guidance is an outcome of a decision tree.

    3.  In the **Node name** field, enter `Reassign this case`.

    4.  In the **Guidance** field, select the Reassign case guidance.

    5.  In the **Set more field inputs to show to users** section, map inputs by selecting the Link input icon \(![Link input icon](../image/icon-link-input.png)\) next to the field and selecting a guidance input from the list.

    6.  Select **Save and close**.

2.  Associate a guidance to the 300 path.

    1.  Select **Add node** in the 300 path.

    2.  In the pop-up window, select **Propose a guidance as an outcome** to configure a guidance node.

        A guidance is an outcome of a decision tree.

    3.  In the **Node name** field, enter `Create a work order`.

    4.  In the **Guidance** field, select the Create work order guidance.

    5.  In the **Set more field inputs to show to users** section, map inputs by selecting the Link input icon \(![Link input icon](../image/icon-link-input.png)\) next to the field and selecting a guidance input from the list.

    6.  Select **Save and close**.

3.  Associate a guidance to the 500 path.

    1.  Select **Add node** in the 500 path.

    2.  In the pop-up window, select **Propose a guidance as an outcome** to configure a guidance node.

        A guidance is an outcome of a decision tree.

    3.  In the **Node name** field, enter `Assign an IT technician`.

    4.  In the **Guidance** field, select the Assign IT technician guidance.

    5.  In the **Set more field inputs to show to users** section, map inputs by selecting the Link input icon \(![Link input icon](../image/icon-link-input.png)\) next to the field and selecting a guidance input from the list.

    6.  Select **Save and close**.


## Result

![Failure code nodes displaying a process flowchart that involves asking for failure codes and branching into three distinct paths based on the code provided.](../image/ex-failure-code-guidances-result.png)

