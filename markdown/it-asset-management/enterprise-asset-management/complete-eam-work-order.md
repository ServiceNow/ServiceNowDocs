---
title: Complete and close a work order for an enterprise asset
description: Close an assigned work order by completing all work that is required for the associated enterprise asset.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Managing work for your enterprise assets, Manage work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Complete and close a work order for an enterprise asset

Close an assigned work order by completing all work that is required for the associated enterprise asset.

## Before you begin

Role required: wm\_agent

## About this task

When working on an enterprise asset, you can choose to deploy, swap, or remove any required assets or parts. Similarly, you can deploy a discrete asset to a linear asset, swap a discrete asset associated with a linear asset, or remove a discrete asset associated with a linear asset. You can also choose to calibrate the enterprise asset. After you complete all work for the asset, you can close the associated work order.

**Note:** Starting with Enterprise Asset Management version 10.0, a work order can be associated with more than one asset or an asset group.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Work management**.

2.  On the **Work order tasks** tab, select the work order task for the work order that you want to complete and close.

3.  Select **Start Work**.

    The work order task reloads with an updated State of Work In Progress.

4.  Complete all work that is required for the work order task.

    -   If you want to deploy, swap, or remove any required assets or parts, follow these steps:
        1.  Select the **Asset Usages** tab.
        2.  Select the action that you’re taking on an asset or part that is required for the associated enterprise asset.

<table id="table_o5k_kl3_cbc"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Remove Asset**

</td><td>

Option to remove an asset or part. You can also remove a discrete asset associated with a linear asset.

**Note:** You can remove assets or parts that have a state of In use, In maintenance, and Consumed only.

 1.  In the **Remove asset** field, select the asset or part that you want to remove.

**Note:** In Enterprise Asset Management version 10.0 and later, the assets available in this field depend on whether the Affected assets list is populated.

    -   If the Affected assets list is populated, only assets in the list and their descendants with the **Required** field set to **false** are available.
    -   If the Affected assets list is empty — for example, when the work order and work order task are based on a location — assets associated with the work order task location and descendant locations are available. Descendant assets are included only if the **Required** field is set to **false**.
2.  Select **OK**.
 -   **Result**
    -   The asset or part that is removed appears on the **Asset Usages** tab. The removed asset or part is assigned to your personal stockroom. Execute all subsequent disposal tasks to complete the removal.
    -   The State and Substate of the asset change to In stock and Pending disposal.
    -   The Location field is empty.
    -   If the work order task is based on an asset group, the removed asset is also removed from the asset group.

**Note:** Starting with Enterprise Asset Management version 10.0, a work order can be associated with more than one asset or an asset group.

</td></tr><tr><td>

**Swap Asset**

</td><td>

Option to swap an asset or part. You can also swap a discrete asset associated with a linear asset with another discrete asset

 In the Deploy asset dialog box, perform the following steps:

1.  In the **Asset to swap out** field, select the asset or part that you want to swap out.

**Note:** In Enterprise Asset Management 10.0 and later, the assets available in this field depend on whether the Affected assets list is populated.

    -   If the Affected assets list is populated, only assets in the list and their descendants with the **Hot swappable** field set to **true** are available.
    -   If the Affected assets list is empty — for example, when the work order and work order task are based on a location — assets associated with the work order task location and descendant locations are available. Descendant assets are included only if the **Hot swappable** field is set to **true**.
2.  In the **Replacement Asset** field, select the replacement asset or part

**Note:** The replacement asset or part must meet the following criteria:

    -   The **State** field in the corresponding asset record is set to **In stock**.

If the asset or part is associated with a multi-component enterprise model that has hot-swappable model components, this field can also be set to **In use**.

    -   The asset or part is either displayed on the **Asset Usages** tab or located in your personal stockroom.
    -   The asset or part is associated with either the same enterprise model as the existing asset or part or a substitute enterprise model that is supported by the existing asset or part. For more information on substitute enterprise models, see [Add a substitute model for an enterprise model](add-enterprise-model-substitute.md).
3.  Select **OK**.
-   **Result**

After the swap is complete:

    -   Both the swapped-out asset or part and the replacement asset or part appear on the **Asset Usages** tab.
    -   In Enterprise Asset Management version 10.0 and later, the replacement asset is automatically added to the Affected assets list.
    -   If the work order task is based on an asset group, the swapped-out asset is removed from the asset group, and the replacement asset is added to it.

**Note:** Starting with Enterprise Asset Management version 10.0, work orders can be created for asset groups.

</td></tr><tr><td>

**Deploy Asset**

</td><td>

Option to deploy an asset or part. You can also deploy a discrete asset to a linear asset.

**Note:** You can deploy assets or parts that are displayed on the **Asset Usages** tab and have a status of Not Used. You can deploy assets or parts from your personal stockroom that have a state of In stock and a substate of either Available or Reserved.

 1.  In the **Asset to deploy** field, select the asset or part that you want to deploy.

**Note:** If you select a consumable asset or part, you must also specify the quantity that you want to deploy in the **Quantity** field.

2.  \(Optional\) In the **Assign to user** field, select the user to whom you want to assign the asset or part.
3.  \(Optional\) In the **Add to asset** field, select the parent asset or part to which you want to add the asset or part.
4.  Select **OK**.
 -   **Result**
    -   The deployed asset with a status of Used appears in the **Asset Usages** tab.
    -   If the work order task has an asset group and Affected assets list, the deployed asset is added to the asset group and to the **Affected assets** list.

**Note:** Starting with Enterprise Asset Management version 10.0, work orders can be created for asset groups.

    -   If the work order task has an affected assets list but no asset group selected, the deployed asset is added to the **Affected assets** list only.

**Note:** The Affected assets tab is available with Enterprise Asset Management version 10.0 and later.

 To deploy a discrete asset to a linear asset, in the **Deploy asset** dialog box, select a discrete asset from your stockroom, and then choose one of the following options:

-   **Add to discrete asset**: Select the discrete asset to which you want to add the selected asset as a child asset.
-   **Add to existing location**: Select an existing location
-   **Add to new location**: Use the location picker to mark the new location on the geo map.


</td></tr></tbody>
</table>        3.  Repeat step b for every asset or part that you want to deploy, swap, or remove.
    -   If you want to calibrate the associated enterprise asset, use the following steps:
        1.  Navigate to the calibration playbook.
            -   In Enterprise Asset Management version 10.0 and later, perform these steps:
                1.  Select the **Calibrations** tab.

                    The Calibrations tab displays a calibration event for each asset in the Affected assets tab that has a calibration attribute defined. The number of calibration events depends on the work order association:

                    -   If the work order is associated with an asset, one calibration event is created, provided the asset has a calibration attribute defined and no other assets are added to the Affected assets list.
                    -   If the work order is associated with an asset group, one calibration event is created for each asset from the asset group that is added to the Affected assets list and has a calibration attribute defined.
                2.  Select the calibration event for the asset that you want to calibrate.

                    The Service event details page opens.

                3.  Select the **Calibration** tab.
            -   In Enterprise Asset Management versions prior to 10.0, select the **Calibration** tab.
            -   **Result**

                The Calibration event playbook opens.

                **Note:** Each lane in the side panel of the playbook represents an activity that you must complete as part of the calibration event workflow.

        2.  In the work area of the Details lane, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Name of the calibration event.|
            |Temperature|Temperature of the environment in which you’re performing the calibration.|
            |Temperature unit|Unit of temperature that you’re using to measure the environmental temperature.|
            |Humidity \(%\)|Relative humidity level of the environment in which you’re performing the calibration.|

        3.  Select **Mark as complete**.

            The Details lane is marked as Complete and you automatically progress to the Calibration Lines lane.

        4.  In the work area of the Calibration lines lane, select the calibration line that you want to complete or skip.

            Each calibration line corresponds with a calibration attribute on the associated enterprise asset. If any calibration attribute contains multiple points at which you can measure accuracy, the Enterprise Asset Management application creates a separate calibration line for each point. You can choose to complete or skip each calibration line as needed. For more details on calibration attributes, see [Add calibration attributes to an enterprise asset](add-calibration-attributes-enterprise-asset.md) or [Add calibration attributes to an enterprise model](add-calibration-attributes-enterprise-model.md).

        5.  On the calibration line record, use one of the following options to complete or skip the calibration line:

            -   To complete the calibration line, fill in the fields and then select **Submit**.

<table id="table_mp2_h23_cbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Details

</td></tr><tr><td>

Instrument

</td><td>

Instrument that you’re using to perform the calibration. If you specified an instrument model in the **Instrument model** field of the corresponding calibration attribute, the options in this field are filtered based on the specified instrument model.

</td></tr><tr><td>

Calibration date

</td><td>

Date and time at which you’re performing the calibration. This field populates automatically based on the date and time at which the Details lane was marked as complete. You can overwrite this field if needed.

</td></tr><tr><td colspan="2">

Readings

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
</table>            -   To skip the calibration line, select **Skip**.
            The calibration line record closes and you automatically return to the playbook.

        6.  Repeat steps d and e for each calibration line in the Calibration lines lane.

            **Note:** If any of your calibration lines have a Result of Failed, you can remediate the entire calibration event by initiating a new work order and corresponding work order tasks. See [Remediate an unsuccessful enterprise asset calibration](remediate-unsuccessful-enterprise-asset-calibration.md) for detailed instructions.

        7.  Select **Mark as complete**.

            The lane is marked as Complete.

        8.  If there are multiple calibration events, repeat steps a through g for each calibration event in the Calibrations tab.

            **Note:** Multiple calibration events are supported in Enterprise Asset Management version 10.0 and later.

5.  After you complete all required work, select **Close Complete** on the work order task.

    The state of both the work order task and associated work order changes from Work In Progress to Closed Complete.


**Parent Topic:**[Managing work for your enterprise assets](../concept/managing-work-enterprise-assets.md)

