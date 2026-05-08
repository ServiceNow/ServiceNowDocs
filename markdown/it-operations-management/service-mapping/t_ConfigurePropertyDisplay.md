---
title: Modify display for CI attributes
description: You can control what configuration item \(CI\) attributes the system displays in the Properties pane of service instance maps.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Modify display for CI attributes

You can control what configuration item \(CI\) attributes the system displays in the Properties pane of service instance maps.

## Before you begin

Get familiar with the notion of views. For more information on views, see View Management.

Decide for which CI classes you need to modify display.

Decide whether you want to modify display for parent CI classes to see the view change in all their child CI classes. To check the parent CI class of a CI class, perform the steps below:

**Note:** The Service Mapping user interface refers to CI classes as CI types.

1.  Navigate to **System Definition** &gt; **Tables**.
2.  Set the search field to **Name**, and enter the relevant CI class.

    The list of all CI class that match the name is displayed.

3.  Check the **Extends table** column to see the parent CI class.

Role required: service\_mapping\_admin or app\_service\_admin

## About this task

When working with service instance maps, the Properties pane displays attributes for CIs and connections you select in a map. Since there is a large number of attributes to display, you may want to choose which attributes are displayed, and in what order.

The attributes and their order of display is determined by a combination of the CI type definition and the view for this CI type.

CMDB stores CI class in the form of a hierarchy where some CI classes are parents to other CI classes, who automatically derive their parent's attributes in addition to attributes you configure specifically for child CI classes. CI class hierarchy is used widely for configuring CI behavior, relationships, and display.

![Child CI classes derive attributes from their parents.](../image/CITypeHierarchyDiagram.png "Child CI classes derive attributes from their parents")

The view that controls the attribute display in service instance maps is called **sa\_map\_properties**. You can assign this view to new CI classes or modify the view for CI classes which already use it. Use the CI type hierarchy to configure the **sa\_map\_properties view**:

-   The parent CI class at the top of the hierarchy is **cmdb**.
-   If you do not define the view for a child CI class, the system displays attributes derived from the parent with the addition to all the attributes of this child CI class.

    ![A view is configured only for the parent CI class, not the child CI class.](../image/CITypeViewParentViewDiagram.png)

-   If you define a view for a child CI class, it includes only the attributes that you specifically added to the child CI class. The system does not display any of its parent attributes automatically.

    ![A separate view is configured for the child CI class.](../image/CITypeViewChildViewDiagram.png)

-   If you do not add a parent CI class or its child CI class to the view, the system uses the ascendant CI class that was added to the view in addition to all attributes of all parent CI classes in the hierarchy between this child CI classes and the parent CI class that is added to the view.

    ![No separate view is configured for the CI class or the child CI class.](../image/CITypeViewParentofParentViewDiagram.png)


For example, if you define the **sa\_map\_properties** view for the CI class for Windows Servers, the Properties pane displays the same attributes for all Windows Servers: CI type \(class\), Class, Model ID, and name.

![The Properties pane displaying the same attributes for CIs belonging to the same class.](../image/CITypeViewExample.png "CIs belonging to the same class")

You can modify the view at any time.

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  In the service instance map, select the CI whose attributes you want to change.

3.  In the **Properties** pane, click **Detailed Properties**.

    ![The graphic shows the Detailed Properties link in the Properties pane.](../image/MapCIDetailsPropertiesPaneDetailedlink.png)

4.  In the CI Detailed Properties page, click the **Additional actions** icon and select **Configure &gt; Form Layout**.

5.  In the **View name** list under **For view and section**, define which view you want to modify:

    ![The graphic shows the View name list.](../image/MapCIPropertiesFormViewAndSection.png)

    -   Select **sa\_map\_properties** if it appears in the list, or
    -   If **sa\_map\_properties** does not appear in the list:
        1.  Select **New**.
        2.  In the **View name** field, enter `sa_map_properties`.
        3.  Click **OK**.
6.  Use the slushbucket to add or remove attributes from the view.

7.  Click **Save**.

8.  Return to the service instance map and reselect the CI for which you changed the view.

    The **Properties** pane displays the attributes that you configured for the view.

9.  If necessary, repeat the procedure for other CI classes.


**Related topics**  


[View CI attributes in an application service map](t_ViewCIDetails.md)

