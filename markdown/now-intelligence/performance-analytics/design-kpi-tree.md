---
title: Analysis and the KPI tree
description: In the Analysis tab of KPI Composer, design your KPI tree. Specify your business goals, their associated critical success factors, and the measurement related to those factors. Chart the logical relationship between these factors and the personas who are responsible for them.Add artifacts to the KPI tree by using the drag-and-drop tiles at the bottom of the project canvas.Each artifact in a KPI tree can reference knowledge base articles, personas, or breakdown definitions.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Design your Performance Analytics solution with KPI Composer, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Analysis and the KPI tree

In the Analysis tab of KPI Composer, design your KPI tree. Specify your business goals, their associated critical success factors, and the measurement related to those factors. Chart the logical relationship between these factors and the personas who are responsible for them.

A KPI tree contains the following hierarchically related artifacts:

-   **Business goals**

    Typically, you put a business goal at the top of your KPI tree. This goal represents what you want to achieve with the dashboards coming forth from this project. A business goal can be something like "Cost Efficiency" or "Quality Assurance."

-   **Critical Success Factors**

    Put these factors under your business goals to identify what your organization needs to do to achieve the business goal. Critical success factors can be placed under a business goal or under other critical success factors.

-   **Measurements**

    Decide how to measure the performance of a critical success factor. Measurements are the most 'indicator-like' artifact in the KPI tree. They contain the functional description of how to make the measurement. Additionally, you can store who is responsible for the measurement and who to contact in case this measurement is used in different projects.


The KPI tree has a header and a footer with the following drag-and-drop icons:

-   Artifacts, on the left of the footer
-   Breakdown definitions, on the right of the header \(See [Group data by breakdown definitions](../task/add-breakdowns-project.md#)\)
-   Personas, on the left of the header \(See [Add personas to a project](../task/add-personas-project.md)\)

## Filtering

The following filter options are available on the Analysis tab:

-   Filter by persona. Select a Persona icon in the header to highlight the artifacts that are linked to the persona. You can select multiple personas. In this case, any artifact that is linked to at least one of the selected personas is highlighted.
-   Filter by breakdown definition. Select a Breakdown definition icon in the header to highlight the artifacts that are linked to the breakdown. You can select multiple breakdowns. In this case, any artifact that is linked to at least one of the selected breakdowns is highlighted.
-   Filter on text. Enter text in the filter field, then leave the field. All artifacts that contain the text are highlighted.

All filter functions can be used with each other.

## Expanding and collapsing tree nodes

When working with large KPI trees, you can close those parts of the tree that you are not currently working with. To collapse part of a tree, click the minus - icon on an artifact that has child artifacts. Collapsed nodes appear as a shadow under the top-level node. To expand collapsed nodes, click the plus + icon.

![Collapse node icon with two levels of subnodes](../image/kpi-composer-collapse-nodes.png) ![](../image/kpi-composer-collapsed-nodes.png)

When a filter or a search matches a collapsed, hidden artifact, the tree does not expand. Instead, the "shadow" turns white although the top-level element remains grey.

![Collapsed nodes that do and do not match a filter](../image/kpi-composer-filter-collapsed-node.png)

**Parent Topic:**[Design your Performance Analytics solution with KPI Composer](designing-pa-solution.md)

## Add artifacts to a KPI tree

Add artifacts to the KPI tree by using the drag-and-drop tiles at the bottom of the project canvas.

### Before you begin

Think about your business goal and critical success factors before you begin to work on a project.

Role required: sn\_kpi\_composer.user \(own project\), sn\_kpi\_composer.admin \(any project\), admin. No role required for responsible user or user with edit access from project sharing.

### Procedure

1.  Navigate to **KPI Composer** and open or create a project, then navigate to the Analysis tab.

2.  Locate the KPI tree artifacts at the bottom of the screen.

    ![Draggable icons for each KPI Composer tree artifact](../image/kpi-comp-tree-elements.png)

3.  Drag a Business Goal icon to the top of your project.

    To keep your planning simple, usually you have one business goal for each project, but you can have business goals as children of other business goals.

4.  Set the Business Goal properties as described in "Artifact properties."

    You can edit these properties later by clicking the Edit icon \(![](../image/kpi-comp-edit-item-icon.png)\) on the artifact tile.

5.  Repeat this process with Critical Success Factors and Measurements.

    Drop an artifact on top of another artifact to have the new artifact displayed as a child of the existing artifact. Critical Success Factors can be children of Business Goals or other Critical Success Factors. A Measurement can be a child of any artifact.

6.  As an alternative to creating and configuring all your artifacts, you can add an existing Library Element.

    1.  Select the bookmark icon to open the **Library Elements** list.

    2.  Drag an appropriate library element into your KPI tree.

        ![Library Elements list.](../image/kpi-comp-library-elements.png)

    For more information, see [Cross-project library elements](cross-project-artifact-libraries.md).


### What to do next

If you change your mind about the relationships in a tree, you can select and drag an existing artifact to a different artifact. You can also change the ordering of artifacts. Drag a child artifact onto its parent to move it into the top position among its siblings.

## Artifact properties

Each artifact in a KPI tree can reference knowledge base articles, personas, or breakdown definitions.

<table id="table_p4n_z4d_mjb"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique, meaningful name

</td><td>

High-quality cost-effective business resolution \(for a business goal artifact\)Total incident resolution cost \(for a measurement artifact\)

</td></tr><tr><td>

Description

</td><td>

A detailed description of the artifact to help others understand its purpose and to avoid redundancy

</td><td>

Total monetary cost from when an incident is raised until it is resolved, including estimated salary and opportunity costs

</td></tr><tr><td>

Target

</td><td>

The future performance improvement you want from Performance Analytics. If you do not yet have a quantitative target score for an indicator, describe the target qualitatively.

</td><td>

A 10% reduction every month until a final value of 40 is reached.

</td></tr><tr><td>

**Add this element to the library** link

</td><td>

Adds this artifact and any child artifacts in the KPI tree to a multi-project, reusable library element.

</td><td>

For more information, see [Cross-project library elements](cross-project-artifact-libraries.md).

</td></tr><tr><td>

Info![](../image/kpi-comp-info-icon.png)

</td><td>

Specify any of the following details:-   Knowledge articles that contain further explanation about the artifact. You can link any number of knowledge articles.
-   Artifact owners
-   Contact persons

</td><td>

This short animation shows a knowledge article being added to an artifact.![Adding a KB article to an artifact](../image/kpi-comp-add-kb.gif)

</td></tr><tr><td>

Persona![](../image/kpi-comp-persona-icon.png)

</td><td>

The personas currently linked to the project. In the artifact properties, you can only add and remove personas to the artifact. For information about adding personas to the project, see [Add personas to a project](../task/add-personas-project.md).

</td><td>

In this image, the Agent and CIO personas are linked to the project. The CIO persona is linked to the artifact and the Agent persona is not.![Personas available to an artifact in a project](../image/kpi-comp-element-personas.png)

</td></tr><tr><td>

Group by![](../image/kpi-comp-bkdown-icon.png)

</td><td>

Group the data associated with an artifact by one or more of the breakdown definitions selected for the project. For information about adding breakdown definitions to the project, see [Group data by breakdown definitions](../task/add-breakdowns-project.md#).

</td><td>

In this image, the Assignment Group, Impact, and Priority breakdown definitions are available for the artifact. The data in the artifact is grouped by only Assignment Group.![Grouping the data of an artifact by 'Group by' terms](../image/kpi-comp-add-bkdowns.png)

</td></tr></tbody>
</table>