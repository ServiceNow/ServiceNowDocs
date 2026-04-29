---
title: Create a library element
description: Convert an artifact and its children in a KPI tree into a KPI Composer cross-project library element.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Cross-project library elements, Design your indicator solution, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a library element

Convert an artifact and its children in a KPI tree into a KPI Composer cross-project library element.

## Before you begin

You need an existing project with a KPI tree with at least one artifact.

Role required: sn\_kpi\_composer.user \(own project\), sn\_kpi\_composer.admin \(any project\), admin. No role required for responsible user or user with edit access from project sharing.

## About this task

**Note:** You can nest library elements. In other words, you can create a library element from an artifact that includes another library element among its descendants. The elements of the original library element are included in the new, higher-level one. The original library element still exists and can be included in a KPI tree on its own.

## Procedure

1.  Open the Analysis tab of a KPI Composer project.

2.  Select an artifact in the tree.

    Select an artifact that you want to be able to reuse in other projects. If you want to reuse a group of artifacts, select the root artifact. All descendant artifacts of the root artifact will be included in the library element.

    In this example, you want to reuse the "Improve Customer Service Quality" critical success factor. You want to use it with its two child measurements "% of incidents resolved on time" and "% of major incident first call resolution."

    ![Artifacts in a KPI tree that you want to reuse in multiple projects.](../image/kpi-comp-block-reuse.png)

3.  In the properties window of the artifact, select **Add this element to the library**.

    In this example, you have opened the properties of the "Improve Customer Service Quality" artifact and are about to click **Add this element to the library**.

    ![Properties window for an artifact showing the Add this element to the library link.](../image/kpi-comp-add-element-library.png)


## Result

The selected artifact and its descendants are converted to a library element. A bookmark icon is added to each of their tiles to identify them as belonging to a library element. You can no longer edit them in the original project.

## "Improve Customer Service Quality" library element

This example shows the library element that results from the procedure steps. The root artifact is "Improve Customer Service Quality." The library element consists of it and the two measurements "% of incidents resolved on time" and "% of major incident first call resolution".

![The library element from the example steps in the procedure.](../image/kpi-comp-library-element.png)

## What to do next

A library element starts out as Personal in scope. Only the user who created it can add it to a KPI tree. If you have the admin or sn\_kpi\_composer\_admin role, you can change the scope of a library element to Global. All users can add Global library elements to their KPI trees.

You cannot edit a library element from inside a project.

**Parent Topic:**[Cross-project library elements](../concept/cross-project-artifact-libraries.md)

