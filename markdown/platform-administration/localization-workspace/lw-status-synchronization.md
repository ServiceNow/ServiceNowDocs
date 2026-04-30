---
title: Localization Workspace Home and translation job status
description: Start a translation request and monitor the current status of your translation requests from the Localization Workspace Home screen.
locale: en-US
release: zurich
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2025-12-12"
reading_time_minutes: 2
breadcrumb: [Exploring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer]
---

# Localization Workspace Home and translation job status

Start a translation request and monitor the current status of your translation requests from the Localization Workspace Home screen.

## Overview of Localization Workspace Home

The Home screen of Localization Workspace is where you can launch a new translation request. Also, in the Home screen's **My Requests** list, you can track the progress of translation requests in the system.

-   A translation request that has been saved but not submitted has the State of **Draft**.
-   A translation request that has been submitted to the translation service provider has a State of **In progress** \(after its project has been packaged\).

![The Home screen of Localization Workspace including the My Requests list displaying one saved translation request and one submitted request. A tab for a localization project is highlighted.](../image/lw-status-synchronization-home-overview.png)

**Note:** When displayed in the Requests list, the Cost is based on a rate rounded up to the decimal place that is set in your Display Value Currency field. However, the calculation of the informational cost estimate uses the actual rate that you have configured in Localization Workspace. The calculation does not use the currency's display value. For more information, see [Identify the FX Currency field and its display parameters](../../currency/task/fx-currency-display-parameters.md).

Localization Workspace extends and builds upon projects in Localization Framework. From the My Requests list you can review details of the translation request's project by selecting the **LF Project** number.

![A localization project tab which has been opened from the Home screen. The project details can be reviewed and optionally updated.](../image/lw-status-synchronization-project.png)

For information about creating a translation request, see [Requesting translations in Localization Workspace](requesting-translations-localization-workspace.md).

## Translation request states

The state of translation requests in Localization Workspace corresponds to Localization Framework projects as follows.

<table id="table_yrw_dtn_bgc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The translation request is saved but not submitted. Corresponding Localization Framework status: Draft.

</td></tr><tr><td>

Submitted

</td><td>

The translation request has been moved to Localization Framework, where the project and its tasks are being created. Corresponding Localization Framework status: \(N/A\).

</td></tr><tr><td>

In progress

</td><td>

The translation project and its tasks have been successfully created in Localization Framework and sent to the selected translation provider.Corresponding Localization Framework status: In Progress.

</td></tr><tr><td>

Complete

</td><td>

The translation project is complete and all tasks within the project are complete and closed.Corresponding Localization Framework status: Closed Complete.

</td></tr><tr><td>

Closed: Project Incomplete

</td><td>

The translation project is incomplete when at least one of the tasks within the project has been marked as closed but isn’t complete.Corresponding Localization Framework status: Closed Incomplete.

</td></tr></tbody>
</table>The status of your translation request is displayed in the My Requests list in the **State** column.

**Related topics**  


[States of Localization Framework projects and tasks](../../localization-framework/reference/localization-task-states.md)

[Requesting translations in Localization Workspace](requesting-translations-localization-workspace.md)

