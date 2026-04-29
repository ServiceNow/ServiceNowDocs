---
title: Take action on an enterprise asset using the Mobile Agent application
description: Deploy, remove, or swap any assets or parts that are required for an enterprise asset by using the Mobile Agent application. You can also use the application to calibrate your enterprise assets.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Manage an Enterprise Asset Management task using the Mobile Agent application, Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Take action on an enterprise asset using the Mobile Agent application

Deploy, remove, or swap any assets or parts that are required for an enterprise asset by using the Mobile Agent application. You can also use the application to calibrate your enterprise assets.

## Before you begin

Role required: wm\_agent

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **My Tasks** tab.

    The home screen of the My Tasks application opens with the first few tasks in the list of tasks assigned to you displayed.

3.  If the task you want to work on isn't displayed, tap **See all**.

4.  Filter or sort the task view.

    -   To filter your tasks, tap the Filter icon \(![Filter icon](../image/filter-mobile-task-eam.png)\) and enter the values to use as a filter in the **Due Date**, **Asset**, **Location**, or **Priority** fields.
    -   To sort your tasks, tap the Filter icon \(![Filter icon](../image/filter-mobile-task-eam.png)\), tap **Sort by**, and select the fields by which to sort your tasks.
5.  Tap the work order task for which you want to take action.

6.  Complete all the work that is required for the work order task.

    -   If you want to deploy, swap, or remove any required assets or parts, use the following steps:
        1.  Tap the **Parts** tab of the work order task.

            By default, the Asset Usages list displays only the first few assets and parts that are associated with the work order task. If the asset or part that you want to take action on isn't displayed, tap **See all**.

        2.  On the Asset Usages list, choose the action that you want to take on the asset or part.

            **Note:** If you want to filter the displayed assets or parts, tap the Filter icon \(![Filter icon](../image/filter-mobile-task-eam.png)\) and enter the values to use as a filter in the **Quantity**, **State**, **Substate**, or **Display name** fields.

<table id="table_icr_plp_cbc"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deploy an asset or part

</td><td>

The asset or part must have a status of Not Used. You can also deploy assets or parts from your personal stockroom that have a state of In stock and a substate of either Available or Reserved.

1.  Select the asset.
2.  Tap **Deploy**.
3.  On the Deploy asset screen, tap the asset that you want to deploy.
4.  On the Deploy asset execute screen, in the **Quantity** field, select the quantity of parts that you want to deploy.
5.  Add the asset or part as a child of another asset or part by tapping **Add to asset** and then selecting the required asset from the asset list.
6.  Assign the asset or part to a specific user by tapping **Assign to user** and then selecting the user from the list of users.
7.  Tap **Deploy**.
-   **Result**
    -   The Asset Usages list reloads to display the deployed asset or part with a Status of **Used** and State of **In use**. The Status of a consumable asset changes to **Consumed**.
    -   If the work order task has an asset group and affected assets list, the deployed asset is added to the asset group and to the **Affected assets** section in the **Related** list.
    -   If the work order task has an affected assets list but no asset group selected, the deployed asset is added to the **Affected assets** list only.


</td></tr><tr><td>

Remove an asset or part

</td><td>

The asset or part must have a state of In use, In maintenance, or Consumed.1.  Select the asset or part.
2.  Tap **Remove**.
3.  On the Remove asset screen, tap the asset or part that you want to remove.

**Note:** The assets available in this field depend on whether the **Affected assets** list is populated.

    -   If the Affected assets list is populated, only assets in the list and their descendants with **Required** set to **false** are available.
    -   If the Affected assets list is empty — for example, when the work order and work order task are based on a location— assets associated with the work order task location and descendant locations are available. Descendant assets are included only if **Required** is set to **false**.
4.  Tap **Remove**.
-   **Result**
    -   The **Asset Usage** section reloads to display the removed asset or part, which now has the Status of**Removed** and State of **In stock**.
    -   If the work order task is based on an asset group, the removed asset is also removed from the asset group.


</td></tr><tr><td>

Swap an asset or part with a replacement part

</td><td>

1.  Tap **Swap**.
2.  On the Select asset to swap screen, tap the asset or part that you want to swap.

**Note:** The assets available in this field depend on whether the Affected assets list is populated.

    -   If the Assets Affected list is populated, only assets in the list and their descendants with **Hot swappable** set to **true** are available.
    -   If the affected assets list is empty — for example, when the work order and work order task are based on a location— assets associated with the work order task location and descendant locations are available. Descendant assets are included only if **Hot swappable** is set to **true**.
3.  On the Swap assets screen, in the **Swap in asset** field, select the replacement part that you want to swap in from the asset list.

**Note:** The replacement part must have a State of In stock and a substate of Available.

 -   **Result**
    -   The Asset Usages list reloads and displays the updated asset statuses:

        -   The Swap out asset has a status of Removed.
        -   The Swap in asset has a status of Used.
    -   The replacement asset is automatically added to the **Affected assets** section in the **Related** list.
    -   If the work order task is based on an asset group, the swapped-out asset is removed from the asset group, and the replacement asset is added to the asset group.


</td></tr></tbody>
</table>    -   If you want to calibrate the associated enterprise asset, use the following steps:
        1.  Tap **View calibrations** on the work order task.

            **Note:** The **View calibrations** button is only visible when the work order task is in the Work in progress state. If the work order task is associated with an asset group that has no calibration attributes defined for the assets, the **View calibrations** button is not visible.

            The **Calibration events** screen opens with two tabs: **Open** and **Completed**.

            -   The **Open** tab displays all calibration events that are not yet completed.
            -   The **Completed** tab displays all completed calibration events.
        2.  Tap the calibration event that you want to complete.

            The Calibration event playbook opens.

            **Note:** Each lane in the playbook represents an activity that you must complete as part of the calibration event workflow.

        3.  Expand the Calibration event playbook.
        4.  Expand the **Details** lane and then tap **Calibration event details**.
        5.  On the Calibration event details screen, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Name of the calibration event.|
            |Environmental conditions|
            |Temperature|Temperature of the environment in which you are performing the calibration.|
            |Temperature unit|Unit of temperature that you are using to measure the environmental temperature.|
            |Humidity \(%\)|Relative humidity level of the environment in which you are performing the calibration.|

        6.  Tap **Mark as complete**.

            The Details lane is marked as Complete and you automatically progress to the Calibration Lines lane.

        7.  On the Calibration lines screen, select the calibration line that you want to complete or skip.

            Each calibration line corresponds with a calibration attribute on the associated enterprise asset. If any calibration attribute contains multiple points at which you can measure accuracy, the Enterprise Asset Management application creates a separate calibration line for each point. You can choose to complete or skip each calibration line as needed. For more details on calibration attributes, see [Add calibration attributes to an enterprise asset](add-calibration-attributes-enterprise-asset.md) or [Add calibration attributes to an enterprise model](add-calibration-attributes-enterprise-model.md).

        8.  On the Calibration line record, use one of the following options to complete or skip the calibration line:
            -   To complete the calibration line, tap **Edit**. On the Edit calibration line screen, fill in the fields and then tap **Submit**.

<table id="table_mp2_h23_cbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Instrument

</td><td>

Instrument that you are using to perform the calibration. If you specified an instrument model in the **Instrument model** field of the corresponding calibration attribute, the options in this field are filtered based on the specified instrument model.

</td></tr><tr><td>

Expected value

</td><td>

Value that you are measuring tolerance conformance against. This field populates automatically based on the expected value that you specified in the calibration attribute.**Note:** This field appears only if you set the Value type of the calibration attribute to either Accuracy % full scale, Accuracy % point, or True/false.

</td></tr><tr><td>

As found value

</td><td>

Value that you measure prior to the calibration.

</td></tr><tr><td>

As left value

</td><td>

Value that you measure after the calibration.

</td></tr><tr><td>

Comment

</td><td>

Additional comments about the calibration.

</td></tr></tbody>
</table>            -   To skip the calibration line, tap **Skip**.
        9.  Return to the Calibration lines screen.
        10. Repeat steps f to h for each of your calibration lines.

            **Note:** If any of your calibration lines have a Result of Failed, you can remediate the entire calibration event by initiating a new work order and corresponding work order tasks. See [Remediate an unsuccessful enterprise asset calibration](remediate-unsuccessful-enterprise-asset-calibration.md) for detailed instructions.

        11. Tap **Mark as complete**.

            The Calibration lines lane is marked as Complete.

        12. Repeat steps b through k for each calibration event in the **Open** tab.

## What to do next

Close the work order associated with the enterprise asset. For details, see [Close a work order for an enterprise asset using the Mobile Agent application](close-workorder-mobile-app-eam.md).

**Parent Topic:**[Manage an Enterprise Asset Management task using the Mobile Agent application](work-order-mobile-agent-eam.md)

**Related topics**  


[View your tasks using the Mobile Agent application](track-tasks-using-mobile-agent-app.md)

[Assign a group task to yourself using the Mobile Agent application](pick-task-from-assignment-group.md)

[Start working on tasks using the Mobile Agent application](start-work-mobile-agent-eam.md)

[Record time worked on a task using the Mobile Agent application](../concept/record-time-mobile-agent-app.md)

[Initiate a request to source parts for work order tasks using the Mobile Agent application](source-parts-mobile-agent.md)

[Close a Pick Up Asset task using the Mobile Agent application](pickup-asset-task-mobile-agent.md)

[Close a work order for an enterprise asset using the Mobile Agent application](close-workorder-mobile-app-eam.md)

[Create a checklist for work order tasks using the Mobile Agent application](manage-work-orders-using-checklist.md)

[View knowledge articles related to work order tasks in the Mobile Agent application](view-knowledge-articles-mobile-agent.md)

[Create work notes about the work order tasks using the Mobile Agent application](create-worknote-mobile-agent.md)

[Set enterprise assets to the shutdown state using the Mobile Agent application](shutdown-assets-eam-mobile.md)

[Start up enterprise assets after maintenance activities using the Mobile Agent application](startup-assets-eam-mobile.md)

[Move enterprise assets to maintenance state using the Mobile Agent application](move-assets-maintenance-mobile.md)

