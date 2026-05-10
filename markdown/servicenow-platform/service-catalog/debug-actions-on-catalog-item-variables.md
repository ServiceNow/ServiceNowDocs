---
title: Debug actions on catalog item variables
description: Analyze the client-side actions affecting the state and values of all variables. You can also get insights into the performance of each script working on the variables.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Debugging Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Debug actions on catalog item variables

Analyze the client-side actions affecting the state and values of all variables. You can also get insights into the performance of each script working on the variables.

## Before you begin

Role required: admin, catalog\_admin, catalog\_manager, or catalog\_editor.

**Note:** You can perform this task with the catalog\_manager or catalog\_editor role only if you are assigned as the manager or editor of the catalog.

## About this task

The variable action logger displays the chronology of actions that happen on all variables of a catalog item before it is submitted. These actions can happen due to catalog client scripts, catalog UI policies, or catalog data lookups. This client-side logger does not store any data in the database. Also, the information displayed is applicable only while you work on the catalog form.Features available for debugging Service Catalog issues including UI macro customization debugging; variable action logger; variable watcher; item diagnostic report

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Enable Variable Action Logger**.

    The UI Page Customization Diagnostics logger is enabled.

    **Note:** Perform this step before you run the logger.

2.  Navigate to **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

3.  In the Catalog Items list, select an item that you want to log ****.

4.  On the Catalog Item form, click **Try it**.

5.  On the catalog page for the item, right-click the header and select **Show Variable Action Logger**.

    **Note:** The variable logs are grouped by catalog UI policies, catalog client scripts, and data lookups.

    The following information is displayed in the Variable Action Logger window:

    -   Order in which scripts and actions are executed. When a new action is triggered from an existing action, the order of the new action is tracked at a sublevel under the order of the existing action. For example, the order of a new action triggered from step 1.2 is 1.2.1.
    -   Source of the action taken on a variable and the variable name.
    -   Details of the action taken on the variable.
    ![Screenshot for the Variable Action Logger window](../image/VariableActionLogger.png "Variable Action Logger window")

6.  Review the results of the variable action logger.

<table id="choicetable_f5q_mwb_5bb"><tbody><tr><td id="d266074e185">

**Search**

</td><td>

To search for a variable or script, use the **Search** field.

</td></tr><tr><td id="d266074e197">

**Collapse All**

</td><td>

To collapse variable logs within a group, click **Collapse All**.

</td></tr><tr><td id="d266074e209">

**Expand All**

</td><td>

To expand variable logs within a group, click **Expand All**.

</td></tr><tr><td id="d266074e221">

**Filter**

</td><td>

To filter variable logs, click the Filter icon \(![Filter icon](../image/Filter.png)\) and select the required options.

</td></tr><tr><td id="d266074e236">

**Clear Logs**

</td><td>

To clear variable logs, click the Actions icon \(![Icon to clear variable logs](../image/Actions.png)\) and select **Clear Logs**.

</td></tr><tr><td id="d266074e255">

**Export to CSV**

</td><td>

To export the variable logs to a .csv file, click the Actions icon \( ![Actions icon](../image/Actions.png)\) and select **Export to CSV**.

</td></tr><tr><td id="d266074e273">

**Print Logs**

</td><td>

To print variable logs, click the Actions icon \(![Actions icon](../image/Actions.png)\) and select **Print Logs**.

</td></tr></tbody>
</table>
**Parent Topic:**[Debugging Service Catalog](../concept/debugging-service-catalog.md)

