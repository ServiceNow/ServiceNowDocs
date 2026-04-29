---
title: Localization Workspace Home and translation job status
description: Start a translation request and monitor the current status of your translation requests from the Localization Workspace Home screen.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exploring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Localization Workspace Home and translation job status

Start a translation request and monitor the current status of your translation requests from the Localization Workspace Home screen.

## Overview of Localization Workspace Home

The Home screen of Localization Workspace is where you can launch a new translation request using the **Request translation** button.

Also you can track and manage the progress of translation requests in the Home screen's **My Requests** list.

-   Get an overview of a request, including due date and status, at a glance.
-   Open the Translation Request Details window from the request's Number.
-   Archive a closed request, delete a draft request, or cancel an in-progress request from the **Action** column.

## Guided Tours available from Help Center on Home

From version 3.0.0, two guided tours are available. One guided tour assists with configuring a language provider, and is accessible to users with the Localization administrator role \(localization\_admin\). The other guided tour assists with configuring language groups, and is accessible to the Localization admin \(localization\_admin\) and Localization requester \(localization\_requestor\) roles. Find the guided tours by selecting the Help Center icon ![](../../../common/image/Banner_HelpIcon.png) on the Home screen.

## Projects

![The Home screen of Localization Workspace including the My Requests list displaying one saved translation request and one submitted request. A tab for a localization project is highlighted.](../image/lw-status-synchronization-home-overview.png)

Localization Workspace extends and builds upon projects in [Localization Framework](../../localization-framework/concept/localization-framework-landing.md). When you create a translation request, the system creates a project in Localization Framework for you. You can open a tab for the translation request's project by selecting the **LF Project** number from the Requests list.

![A localization project tab which has been opened from the Home screen. The project details can be reviewed and optionally updated.](../image/lw-status-synchronization-project.png)

In the Localization Project tab you can drill down into project components such as Localization Tasks. You can fulfill a localization task using the **Translate** button in a Localization Task tab, when the project state is In Progress.

Any update you make here in Localization Workspace is saved to the underlying Localization Framework tables. Completed and archived projects can't be updated. For more information, see [Fulfill a localization task](../../localization-framework/task/fulfill-localization-task.md) in the Localization Framework documentation.

## Translation request states

The **State** column of **My Requests** is where you can find the status of your translation requests. States in Localization Workspace correspond to Localization Framework projects as follows.

<table id="table_yrw_dtn_bgc"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The translation request is saved but not submitted. The **Save** button is available in each step of the translation request wizard. Draft requests can be re-opened and updated from My Requests by selecting the value in the Number column.

 **Action** column: The available action is **Delete draft**. From version 3.0.0.

 **Note:** Draft requests are not subject to the scheduled job Remove discarded Translation Requests.

Corresponding Localization Framework status: Draft.

</td></tr><tr><td>

Submitted

</td><td>

The translation request has been moved to Localization Framework, where the project and its tasks are being created. Corresponding Localization Framework status: \(N/A\).

</td></tr><tr><td>

In progress

</td><td>

The translation project and its tasks have been successfully created in Localization Framework and sent to the selected translation provider. **Action** column: The available action is **Cancel request**. From version 3.0.0.

 Corresponding Localization Framework status: In Progress.

</td></tr><tr><td>

Complete

</td><td>

The translation project is complete and all tasks within the project are complete and closed. **Action** column: The available action is **Archive request**. From version 3.0.0.

 Corresponding Localization Framework status: Closed Complete.

</td></tr><tr><td>

Closed: Project Incomplete

</td><td>

The translation project is incomplete when at least one of the tasks within the project has been marked as closed but isn’t complete.From version 3.0.0, when you select Cancel for a translation request, its status displays as Closed: Project Incomplete. **Action** column: The available action is **Archive request**. From version 3.0.0.

 Corresponding Localization Framework status: Closed Incomplete.

</td></tr></tbody>
</table>## Archiving translation requests

From version 3.0.0 you can optionally archive your translation requests by selecting **Archive request** in the **Action** column. This is a table view of translation requests, so it isn't a status.

![On the My Requests list, the link Switch to archived requests is highlighted. Also highlighted is Archive request in the Action column.](../image/lw-switch-archived-requests-a.png)

Select the **Switch to archived requests** link to view the list of archived requests. You can return to My Requests by selecting the link **Switch to my requests**.

-   Only requests in a state of Complete or Closed: Incomplete can be archived.
-   Archived requests are maintained indefinitely. They are not subject to the scheduled job Remove discarded Translation Requests.
-   **Action** column: After archiving, selecting **Unarchive request** moves the row back to My Requests.
-   Archived requests are read-only, so they can't be reopened or edited.

## Translation request details

You can open a modal window displaying details about your translation request by selecting the value in the **Number** column. From version 3.0.0, the details window displays the request's translation method. Possible values are [TMS](../../localization-framework/concept/tms-configuration.md), MT \(machine translation\), or Mixed.

Also in the details window you can modify the Due date for requests that are handled by a TMS. Select the Due date field to open a calendar picker. Due dates can be postponed to a later date, but can't be moved to an earlier date.

**Note:** Notify your third-party providers directly regarding any changes to due dates.

After modifying the date, select Update to save the new date, or Cancel to abandon the modification.

![In the Translation Request Details modal window, the Translation Method field is highlighted. The method in this example is TMS.](../image/lw-tr-request-method-a.png)

## The display of Cost in the My Requests list

When displayed in the Requests list, the Cost uses a rate rounded up to the decimal place that is set in your Display Value Currency field. However, the base calculation of the informational cost estimate uses the actual rate that you have configured in Localization Workspace. The base calculation does not use the currency's display value. For more information, see [Identify the FX Currency field and its display parameters](../../currency/task/fx-currency-display-parameters.md).

**Related topics**  


[States of Localization Framework projects and tasks](../../localization-framework/reference/localization-task-states.md)

[Requesting translations in Localization Workspace](requesting-translations-localization-workspace.md)

