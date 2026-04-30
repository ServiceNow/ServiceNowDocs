---
title: Add a dashboard
description: As the first step in designing your dashboards, add an empty dashboard to the KPI Composer Dashboard Visualization tab.Each KPI Composer dashboard mock-up can reference project personas or 'Group by' categories, or an existing Performance Analytics dashboard.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Designing dashboards, Design your Performance Analytics solution with KPI Composer, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Add a dashboard

As the first step in designing your dashboards, add an empty dashboard to the KPI Composer Dashboard Visualization tab.

## Before you begin

You have an existing KPI Composer project with a complete draft of the KPI tree in the Analytics tab.

Role required: sn\_kpi\_composer.user \(own project\), sn\_kpi\_composer.admin \(any project\), admin. No role required for responsible user or user with edit access from project sharing.

## Procedure

1.  Navigate to **All** &gt; **KPI Composer** and open the project.

2.  Navigate to the Dashboard Visualization tab.

3.  Click **+ Add Dashboard**.

4.  Give the Dashboard a meaningful name, probably corresponding to a Business Goal or a higher-level Critical Success Factor in the KPI tree.

5.  Click the Edit Item icon \(![](../image/kpi-comp-edit-item-icon.png)\) in the Dashboard artifact to edit dashboard properties.

6.  Repeat this process for all Business Goals or Critical Success Factors for which you want to create dashboards.


## Add a Customer Experience dashboard to the Design tab

In the following short animation, you see the user create a dashboard named Customer Experience, after a Critical Success Factor. The user adds the Agent and CIO personas, who are expected to view the dashboard. The user groups all the widgets on the dashboard by Assignment Group, intending to create a breakdown dashboard.![A dashboard being added in KPI Composer](../image/kpi-comp-add-dashboard.gif)

**Parent Topic:**[Designing dashboards](../concept/create-a-dashboard-mock-up.md)

**Previous topic:**[Designing dashboards](../concept/create-a-dashboard-mock-up.md)

**Next topic:**[Add tabs and rows to a dashboard](add-tabs-kpi-dashboard.md)

## KPI Composer dashboard details

Each KPI Composer dashboard mock-up can reference project personas or 'Group by' categories, or an existing Performance Analytics dashboard.

<table id="table_kpi-dash-props"><thead><tr><th>

Detail

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

PA Dashboard![](../image/kpi-comp-pa-link-icon.png)

</td><td>

Link to an existing Performance Analytics dashboard. This can be an older dashboard that corresponds to your use case, or a new dashboard that you create based on this KPI Composer design. By linking dashboards as you create them, you can keep track of the state of your project.

</td><td>

In this image, you see the existing Performance Analytics dashboards being filtered by the word "Incident".

 ![Linking an existing PA Dashboard to the dashboard mock-up](../image/kpi-comp-pa-dash-link.png)

</td></tr><tr><td>

Persona![](../image/kpi-comp-persona-icon.png)

</td><td>

The personas you expect to view the final dashboard. Choose from the personas currently linked to the project. For information about adding personas to the project, see [Add personas to a project](add-personas-project.md).After you link personas to a dashboard mock-up, only the artifacts from the Analytics tab that are associated with those personas are available.

</td><td>

In this image, the Agent, CIO, and Incident Manager personas are linked to the project. The Agent and CIO personas are linked to the dashboard. The Incident Manager is not.![Personas available to a dashboard in a project](../image/kpi-comp-dashboard-personas.png)

</td></tr><tr><td>

Group by![](../image/kpi-comp-bkdown-icon.png)

</td><td>

Group all the widgets you place on a dashboard by one or more breakdown definition. \(The resulting design is for a Performance Analytics breakdown dashboard.\) Choose from the breakdown definitions currently selected for the project. For information about adding breakdown definitions to the project, see [Group data by breakdown definitions](add-breakdowns-project.md#).

</td><td>

In this image, the Assignment Group, Impact, and Priority breakdown definitions are available to dashboards in the project. The data in the dashboard is grouped by Impact only.

 ![Adding or removing 'Group by' categories to a dashboard](../image/kpi-comp-dashboard-bkdwns.png)

</td></tr></tbody>
</table>**Related topics**  


[Using breakdowns on dashboards](../concept/c_SpecialDashboards.md)

