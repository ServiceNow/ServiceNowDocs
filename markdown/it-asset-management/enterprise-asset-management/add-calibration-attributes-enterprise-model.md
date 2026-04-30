---
title: Add calibration attributes to an enterprise model
description: Add calibration attributes to an enterprise model to specify and manage the calibrations that are required for the associated enterprise assets throughout their life cycles.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Create and manage enterprise models, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Add calibration attributes to an enterprise model

Add calibration attributes to an enterprise model to specify and manage the calibrations that are required for the associated enterprise assets throughout their life cycles.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## About this task

You can add calibration attributes at the enterprise model level or at the individual enterprise asset level. Alternatively, you can create common calibration attributes that are not associated with any enterprise models or enterprise assets. For details on how to add calibration attributes to an individual enterprise asset, see [Add calibration attributes to an enterprise asset](add-calibration-attributes-enterprise-asset.md). For details on how to create common calibration attributes, see [Create a calibration attribute library](create-eam-calibration-attribute-library.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Enterprise model management view.

3.  Select either the **All enterprise** tab or the tab for a specific model category, such as **Construction**.

4.  From the list of available enterprise models, select the enterprise model that you want to add calibration attributes to.

5.  On the **Calibration attributes** tab of the enterprise model record, select **New**.

6.  On the form, fill in the fields.

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

Order in which the calibration attribute applies to the enterprise model. If your enterprise model contains more than one calibration attribute, the attribute with the lowest numerical value applies to the model first.**Important:** You must use a unique numerical value for each calibration attribute.

</td></tr><tr><td colspan="2">

Calibration properties

</td></tr><tr><td>

Value type

</td><td>

Method by which you want to measure tolerance conformance. Select one of the following options:-   **Accuracy % full scale**: Fixed percentage of accuracy that your calibration measurements must fall within at any point within the enterprise asset's full measurement range. The corresponding tolerance limits remain the same at every point within the measurement range. For example, if a measurement range is 100 units and the accuracy percentage is set to ±1%, the tolerance limits are ±1 unit at every point within the measurement range.
-   **Accuracy % point**: Fixed percentage of accuracy that your calibration measurements must fall within at a specific point within the enterprise asset's full measurement range. The corresponding tolerance limits increase or decrease proportionally based on the value of the point that you are comparing your calibration measurement against. For example, if your accuracy percentage is set to ±1% and you want to compare your calibration measurement against a point that has a value of 50 units, the tolerance limits for this specific point are ±0.5 units. If you want to compare your calibration measurement against a point that has a value of 60 units, the tolerance limits increase to ±0.6 units.
-   **Range**: Measurement range that your calibration measurements must fall within. The corresponding tolerance limits are based on the lowest and highest acceptable point values within the range.
-   **Less than**: Value within the enterprise asset's full measurement range that your calibration measurements must fall below. The corresponding tolerance limit is based on the highest acceptable point value within the range.
-   **Greater than**: Value within the enterprise asset's full measurement range that your calibration measurements must lie above. The corresponding tolerance limit is based on the lowest acceptable point value within the range.
-   **True/false**: Option to assess any qualitative elements of the calibration.


</td></tr><tr><td>

Scale

</td><td>

Full measurement range that you're measuring tolerance conformance against.**Note:** This field appears only if you set the **Value type** field to **Accuracy % full scale**.

</td></tr><tr><td>

Unit

</td><td>

Unit of measurement that you're using to measure tolerance conformance.**Note:** This field appears only if you set the **Value type** field to one of the following options:

-   **Accuracy % full scale**
-   **Accuracy % point**
-   **Range**
-   **Less than**
-   **Greater than**


</td></tr><tr><td>

Accuracy \(%\)

</td><td>

Percentage of accuracy that your calibration measurements must fall within.**Note:** This field appears only if you set the **Value type** field to either **Accuracy % full scale** or **Accuracy % point**.

</td></tr><tr><td>

Resolution

</td><td>

Smallest distinguishable change in value that you can detect and measure. The higher the resolution is, the more specific the change in value is.**Note:** This field appears only if you set the **Value type** field to one of the following options:

-   **Accuracy % full scale**
-   **Accuracy % point**


</td></tr><tr><td colspan="2">

Quality standard

</td></tr><tr><td>

Quality standard

</td><td>

Set of requirements and guidelines that you must follow when performing the calibrations.**Note:** You can create quality standards manually in the Admin center view of the Enterprise Asset Workspace. See [Create a quality standard for your enterprise asset calibrations](create-eam-calibration-quality-standard.md) for detailed instructions.

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
</table>7.  Select **Save**.

    The form closes and you are automatically redirected to the new calibration attribute record.

8.  Specify the points at which you can measure tolerance conformance.

    **Important:** You must specify one or more points within each enterprise asset's measurement range. If you do not specify at least one point, the calibration attribute cannot be set to Active.

    1.  On the calibration attribute record, select **Add calibration points**.

        The Calibration points dialog box opens.

    2.  In the dialog box, fill in the fields.

<table id="table_ewt_whf_bbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Point name

</td><td>

Name of the point.

</td></tr><tr><td>

Expected value

</td><td>

Value that you want to measure tolerance conformance against. If you set the **Value type** field to either **Accuracy % full scale** or **Accuracy % point** in the Create New Calibration Attribute form, enter the value of the point that you want to measure against. If you set the **Value type** field to **True/false**, select a Boolean value of either **true** or **false**.**Note:** This field appears only if you set the **Value type** field to one of the following options in the Create New Calibration Attribute form.

-   **Accuracy % full scale**
-   **Accuracy % point**
-   **True/false**


</td></tr><tr><td>

Order

</td><td>

Order in which you want to use the point to measure tolerance conformance. If your calibration attribute contains more than one point, the point with the lowest numerical value is calibrated first.**Important:** You must use a unique numerical value for each point.

</td></tr><tr><td>

Lower tolerance

</td><td>

Lowest acceptable value that the calibration measurement can reach to stay in conformance.**Note:** This field appears only if you set the **Value type** field to one of the following options in the Create New Calibration Attribute form:

-   **Accuracy % full scale**
-   **Accuracy % point**
-   **Range**
-   **Greater than**
If you set the **Value type** field to either **Accuracy % full scale** or **Accuracy % point**, this field is read-only.

</td></tr><tr><td>

Upper tolerance

</td><td>

Highest acceptable value that the calibration measurement can reach to stay in conformance.**Note:** This field appears only if you set the **Value type** field to one of the following options in the Create New Calibration Attribute form:

-   **Accuracy % full scale**
-   **Accuracy % point**
-   **Range**
-   **Less than**
If you set the **Value type** field to either **Accuracy % full scale** or **Accuracy % point**, this field is read-only.

</td></tr></tbody>
</table>    3.  To add an additional point to the calibration attribute, select the Add Content icon \(![Add Content icon.](../../hardware-asset-management/image/add_content_icon.png)\) and then fill in the fields.

        Repeat this step for each point that you want to add.

    4.  Select **OK**.

    The dialog box closes and the points appear on the **Calibration points** tab of the calibration attribute record.


## What to do next

Create work orders to track the calibrations that are made to the associated enterprise assets. These work orders must use a work order template with tasks that have a Work type of Calibration. For more information on work orders, see [Managing work orders for your enterprise assets](../concept/create-manage-wo-enterprise-assets.md).

**Parent Topic:**[Create and manage enterprise models](../concept/create-manage-enterprise-models.md)

