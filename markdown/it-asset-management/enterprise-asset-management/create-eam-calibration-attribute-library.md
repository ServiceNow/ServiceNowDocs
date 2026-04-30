---
title: Create a calibration attribute library
description: Create a library of common calibration attributes that are not associated with any enterprise models or enterprise assets. Use these attributes to define the details and requirements of your commonly used calibrations.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create and manage enterprise assets, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a calibration attribute library

Create a library of common calibration attributes that are not associated with any enterprise models or enterprise assets. Use these attributes to define the details and requirements of your commonly used calibrations.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## About this task

You can create common calibration attributes that are not associated with any enterprise models or enterprise assets. These calibration attributes can be cloned to any of your available enterprise models. You can also create calibration attributes for a specific enterprise model or enterprise asset. For details on how to create a calibration attribute for a specific enterprise model, see [Add calibration attributes to an enterprise model](add-calibration-attributes-enterprise-model.md). For details on how to create a calibration attribute for a specific enterprise asset, see [Add calibration attributes to an enterprise asset](add-calibration-attributes-enterprise-asset.md).

## Procedure

1.  From the Enterprise Asset Workspace, open the Admin center view.

2.  From the left navigation menu of the Admin center view, navigate to **Calibration** &gt; **Attribute library**.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_ln5_w4y_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Attribute details

</td></tr><tr><td>

Name

</td><td>

Name of the calibration attribute.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the calibration attribute.

</td></tr><tr><td>

Criticality

</td><td>

Criticality level that indicates how important the calibration attribute is.

</td></tr><tr><td>

Service frequency

</td><td>

Frequency at which you must perform the calibration.

</td></tr><tr><td>

Category

</td><td>

Type of calibration.**Note:** The Enterprise Asset Management application includes default calibration categories such as Electrical, Flow, Humidity, and Pressure. You can create additional calibration categories for any calibrations that do not fall under the default categories. For detailed instructions, see [Create a calibration category for your enterprise asset calibrations](create-eam-calibration-categories.md).

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the calibration attribute is active.

</td></tr><tr><td>

Order

</td><td>

Order in which the calibration attribute applies to an enterprise model after it is cloned to the model. If the enterprise model contains more than one calibration attribute, the attribute with the lowest numerical value applies to the model first.

</td></tr><tr><td colspan="2">

Calibration properties

</td></tr><tr><td>

Value type

</td><td>

Method by which you want to measure accuracy. Select one of the following options:-   **Accuracy % full scale**: Accuracy is based on a fixed percentage of the enterprise asset's full measurement range. The corresponding tolerance limits remain the same regardless of which point you measure accuracy at. For example, if a measurement range is 100 units and the accuracy percentage is set to ±1%, the tolerance limits are ±1 unit at every point within the measurement range.
-   **Accuracy % point**: Accuracy is based on a fixed percentage of the specific point that you are measuring accuracy at. The corresponding tolerance limits increase or decrease proportionally based on the point that you measure accuracy at. For example, if your accuracy percentage is set to ±1% and you measure accuracy at a point that has a value of 50 units, the tolerance limits for this specific point are ±0.5 units. If you then measure accuracy at another point that has a value of 60 units, the tolerance limits increase to ±0.6 units.


</td></tr><tr><td>

Scale**Note:** This field appears only if you set the **Value type** field to **Accuracy % full scale**.

</td><td>

Full measurement range that you can measure accuracy within.

</td></tr><tr><td>

Unit

</td><td>

Unit of measurement that you are using to measure accuracy.

</td></tr><tr><td>

Accuracy \(%\)

</td><td>

Percentage of accuracy that your enterprise assets must fall within.

</td></tr><tr><td>

Resolution

</td><td>

Smallest distinguishable change in value that you can detect and measure. The higher the resolution is, the more specific the change in value is.

</td></tr><tr><td colspan="2">

Quality standard

</td></tr><tr><td>

Quality standard

</td><td>

Set of requirements and guidelines that you must follow while performing the calibrations.**Note:** You can create quality standards manually in the Admin center view of the Enterprise Asset Workspace. See [Create a quality standard for your enterprise asset calibrations](create-eam-calibration-quality-standard.md) for detailed instructions.

</td></tr><tr><td colspan="2">

Instrument

</td></tr><tr><td>

Instrument model

</td><td>

Model of the instrument that you must use to perform the calibrations.

</td></tr><tr><td>

Instruction

</td><td>

General instructions or instrument settings that you must follow when performing the calibrations.

</td></tr></tbody>
</table>5.  Select **Save**.

    The form closes and you are automatically redirected to the new calibration attribute record.

6.  Specify the points at which you can measure accuracy.

    **Important:** You must specify one or more points within each enterprise asset's measurement range. If you do not specify at least one point, the calibration attribute cannot be set to Active.

    1.  On the calibration attribute record, select **Add calibration points**.

        The Calibration points dialog box opens.

    2.  In the dialog box, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Point name|Name of the point.|
        |Expected value|Point value that you want to measure accuracy against.|
        |Order|Order in which you want to use the point to measure accuracy. If your calibration attribute contains more than one point, the point with the lowest numerical value is used first.|

    3.  To add an additional point to the calibration attribute, select the Add Content icon ![](../../hardware-asset-management/image/add_content_icon.png) and then fill in the fields.

        Repeat this step for each point that you want to add.

    4.  Select **OK**.

    The dialog box closes and the points appear on the **Calibration points** tab of the calibration attribute record.


## What to do next

Clone the calibration attribute to all applicable enterprise models. See [Clone calibration attributes to an enterprise model](clone-calibration-attributes-enterprise-model.md) for detailed instructions.

**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

