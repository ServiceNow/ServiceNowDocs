---
title: Exploring the 360º view
description: After you have successfully set up your data registries for the tables you use, you can use the 360º view feature to view the relationships between a selected record and related objects, such as controls, risks, and entity types.After data registries have been set up, you can launch 360º view from any record screen in any GRC workspace application to view relationships between the various types of data associated with the selected record.In the 360º view, you can select any relationship to view details.As you navigate through 360º view relationship visualizations, the breadcrumbs along the top edge keep track of where you've been and allow you to return to previously viewed information.If you have defined different views, you can select them from any 360º view visualization.You can configure some functionality enhancements for the 360º view of each record as part of the GRC updates.
locale: en-US
release: zurich
product: GRC: 360 Degree Relationship Visualization
classification: grc-360-degree-relationship-visualization
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [360° Relationship Visualization, Common GRC features, Governance, Risk, and Compliance]
---

# Exploring the 360º view

After you have successfully set up your data registries for the tables you use, you can use the 360º view feature to view the relationships between a selected record and related objects, such as controls, risks, and entity types.

When you launch the 360º view from a particular record, the relationships between the selected record and all associated objects are displayed in a distinctive visualization that allows you to instantly understand how the objects interact with one another. The visualization is directly linked to your data, making it easy to navigate and analyze relationships in context. You can interact with the displayed records to explore additional details, such as drilling down into them for deeper insights.

![360º view](../image/360-rel-viz.png "360º view for the Risk: Loss of Availability entity")

The screen above shows the relationships that you set up in the data registry for the selected main object \(in this case, the Risk: Loss of Availability entity\). As you can see, one entity and one control apply to the main object. And the main object includes a range of relationships related to risk response tasks, internal risk events, and risk assessments. Additionally, there is a risk statement relationship upstream from the main object. All these relationships to the main object are available to you at a glance.

**Parent Topic:**[360° Relationship Visualization](grc-360-deg-rel-vis.md)

## Launch the 360º view

After data registries have been set up, you can launch 360º view from any record screen in any GRC workspace application to view relationships between the various types of data associated with the selected record.

### Before you begin

Role required: data registry reader

### Procedure

1.  Navigate to any GRC workspace, for example the Compliance Workspace.

2.  Open a record for which you want to open in the 360º view.

    ![Record in workspace](../image/360-button.png "Record in workspace")

    **Note:** Depending on the record screen, you may have to select the ellipsis icon to view the **360º view** button.

3.  Select **360º view**.

    ![Relationship visualization](../image/360-rel-viz.png "360º view of selected record")

    **Note:** If you launch the 360º view before configuring your data registries, or if you select an object within the 360º view that has not been configured, the visualization screen opens in fallback \(or unconfigured\) mode. All one-to-many and many-to-many relationships for the object are automatically calculated and displayed in the view.

    A system property called `sn_data_registry.max_count_of_fallback_relationships` allows you to define the maximum number of relationships to display in the 360º view. The default is 25.


## Drilling-down for 360º details

In the 360º view, you can select any relationship to view details.

For example, you can select the **Risks** relationship to view details on four risks.

![Drilling down on Risks](../image/drill-down.png "Drilling down on risks")

You can then select one of the risk records to view relationships specific to that risk record.

![Showing relationships for a selected record](../image/change-relationship-view.png "Showing relationships for a selected risk")

## Navigating the 360º view using breadcrumbs

As you navigate through 360º view relationship visualizations, the breadcrumbs along the top edge keep track of where you've been and allow you to return to previously viewed information.

![360º view breadcrumbs](../image/breadcrumbs.png "360º view breadcrumbs")

Clicking the **Entity: ACME Americas** breadcrumb returns you to a visualization of those relationships.

## Selecting different 360º views

If you have defined different views, you can select them from any 360º view visualization.

![Selecting a different view](../image/select-view.png "Selecting a different view")

The Compliance view presents you with relationships for the main object that are specific to compliance, as you configured it.

![Compliance view](../image/compliance-view.png "Compliance view")

**Related topics**  


[Configure 360º views](set-up-360-data-reg.md#)

## Enhancements in the 360º view

You can configure some functionality enhancements for the 360º view of each record as part of the GRC updates.

The following enhancements and bug fixes are supported with the updated 360º view:

-   Displaying an interactive donut chart: You can enable the **Show Visualization** option for each record and select the display columns in the **Group by** list. See the following example.

    ![Show Visualization option for a record.](../../grc-common-workspace/image/show-visualization-option-record.png "Show Visualization option for a record")

    When you enable the **Show Visualization** option for a record, the 360º view is displayed. In the 360º view, you can view all the objects that are associated with the record as shown in the following example.

    ![360º view for a record.](../../grc-operational-res-ws/image/360-degree-view.png "360º view for a record")

    When you click any sector of the donut chart, the related lists that are associated with the selected object are refreshed. When you click an object pill, it displays the donut chart for the selected object in the side-panel.

-   Configuring the Group by list: You can configure the number and order of the columns in the Group by list. When you update the columns in the Group by list as shown in the following example, the donut chart is refreshed for the selected columns.

    ![Sequence of the columns in the Group by list.](../../grc-common-workspace/image/group-by-field-sequence-of-columns.png "Sequence of the columns in the Group by list")

    When you select a specific order of the columns in the Group by list, the same order of the columns is reflected in the UI. The first column that is displayed in the Selected list is the default value in the display for the customers.

-   Order of the pills: You can configure the order of the pills for each section in the **Order** field. If you have not configured the order of the pills and all the pills have the same order value \(for example, if each pill has an order value of 1\), the pills appear alphabetically.
-   The defect fixes are as follows:
    -   Defect fix on the related lists: A defect on the related lists was fixed. A new sys\_relationship field was added in the code to avoid a conflict among the related lists that refer to the same table.
    -   Defect fix for the Apple iPad Pro devices: Earlier, multiple vertical and horizontal scrolls were displayed in the default view on the smaller Apple iPad devices such as the 12.9-inch \(0.328 meter\) and 16-inch \(0.406 meter\) Apple iPad Pro devices. The defect related to the view on the smaller Apple iPad devices has been fixed. You can see the entire 360º component on an Apple iPad device without needing to scroll the view.
    -   Defect fix on the navigation path: A defect that is related to the caching issue that existed in the prior releases was fixed. You can now view the navigation path correctly for the records.

