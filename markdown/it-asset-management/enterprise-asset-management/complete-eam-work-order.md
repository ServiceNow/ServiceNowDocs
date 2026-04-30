---
title: Complete and close a work order for an enterprise asset
description: Close an assigned work order by completing all work that is required for the associated enterprise asset.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Managing work for your enterprise assets, Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Complete and close a work order for an enterprise asset

Close an assigned work order by completing all work that is required for the associated enterprise asset.

## Before you begin

Role required: wm\_agent

## About this task

When working on an enterprise asset, you can choose to deploy, swap, or remove any required assets or parts. Similarly, you can deploy a discreet asset to a linear asset, swap a discreet asset associated to a linear asset, or remove a discreet asset associated to a linear asset. You can also choose to calibrate the enterprise asset. After you complete all work for the asset, you can close the associated work order.

## Procedure

1.  From the Enterprise Asset Workspace, open the Work management view.

2.  On the **Work order tasks** tab, select the work order task for the work order that you want to complete and close.

    The work order task opens.

3.  Select **Start Work**.

    The work order task reloads with an updated State of Work In Progress.

4.  Complete all work that is required for the work order task.

    -   If you want to deploy, swap, or remove any required assets or parts, use the following steps:
        1.  Select the **Asset Usages** tab.
        2.  Select the action that you are taking on an asset or part that is required for the associated enterprise asset.

<table id="table_o5k_kl3_cbc"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Remove Asset**

</td><td>

Option to remove an asset or part. You can also remove a discreet asset associated to a linear asset.

**Note:** You can remove assets or parts that have a state of In use, In maintenance, and Consumed only.

 If you select this option, the Remove asset dialog box opens. In the dialog box, select the asset or part that you want to remove and then select **OK**. When the dialog box closes, the **Asset Usages** tab reloads to display the removed asset or part, which is now assigned to your personal stockroom. Execute all subsequent disposal tasks to complete the removal.

</td></tr><tr><td>

**Swap Asset**

</td><td>

Option to swap an asset or part. You can also swap a discreet asset associated to a linear asset with another discrete asset

 If you select this option, the Swap asset dialog box opens. In the dialog box, select both the asset or part that you want to swap and the replacement asset or part that you want to swap it with. Select **OK**. When the dialog box closes, the **Asset Usages** tab reloads to display both assets or parts.

**Note:** You can swap an existing asset or part with a replacement asset or part that meets the following criteria:

-   The **State** field in the corresponding asset record is set to **In stock**.

If the asset or part is associated with a multi-component enterprise model that has hot-swappable model components, this field can also be set to **In use**.

-   The asset or part is either displayed on the **Asset Usages** tab or located in your personal stockroom.
-   The asset or part is associated with either the same enterprise model as the existing asset or part or a substitute enterprise model that is supported by the existing asset or part. For more information on substitute enterprise models, see [Add a substitute model for an enterprise model](add-enterprise-model-substitute.md).


</td></tr><tr><td>

**Deploy Asset**

</td><td>

Option to deploy an asset or part. You can also deploy a discreet asset to a linear asset.

**Note:** You can deploy assets or parts that are displayed on the **Asset Usages** tab and have a status of Not Used. You can also deploy assets or parts from your personal stockroom that have a state of In stock and a substate of either Available or Reserved.

 If you select this option, the Deploy asset dialog box opens. In the dialog box, select the asset or part that you want to deploy. If you select a consumable asset or part, you must also specify the quantity that you want to deploy. You can optionally assign the asset or part to a specific user or add the asset or part as a child of another asset or part. After you fill in all required fields, select **OK**. When the dialog box closes, the **Asset Usages** tab reloads to display the deployed asset or part.

 In the Deploy asset dialog box, if you want to deploy a discrete asset to a linear asset, you need to first select a discrete asset from your stockroom, and then choose one of the following options for where to deploy that asset.

-   Add to discreet asset: to add the selected asset as a child asset of the discrete asset. Select the discreet asset you want to add it to.
-   Add to existing location: Select an existing location.
-   Add to new location: Use the location picker to mark the new location on the geo map.


</td></tr></tbody>
</table>        3.  Repeat step b for every asset or part that you want to deploy, swap, or remove.
    -   If you want to calibrate the associated enterprise asset, use the following steps:
        1.  Select the **Calibration** tab.

            The Calibration event playbook opens.

            **Note:** Each lane in the side panel of the playbook represents an activity that you must complete as part of the calibration event workflow.

        2.  In the work area of the Details lane, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Name of the calibration event.|
            |Temperature|Temperature of the environment in which you are performing the calibration.|
            |Temperature unit|Unit of temperature that you are using to measure the environmental temperature.|
            |Humidity \(%\)|Relative humidity level of the environment in which you are performing the calibration.|

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

Instrument that you are using to perform the calibration. If you specified an instrument model in the **Instrument model** field of the corresponding calibration attribute, the options in this field are filtered based on the specified instrument model.

</td></tr><tr><td>

Calibration date

</td><td>

Date and time at which you are performing the calibration. This field populates automatically based on the date and time at which the Details lane was marked as complete. You can overwrite this field if needed.

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

5.  After you complete all required work, select **Close Complete** on the work order task.

    The state of both the work order task and associated work order changes from Work In Progress to Closed Complete.


**Parent Topic:**[Managing work for your enterprise assets](../concept/managing-work-enterprise-assets.md)

