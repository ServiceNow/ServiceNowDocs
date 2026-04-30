---
title: Enable configuration of components with inherited controllers in component builder
description: Learn how components can inherit page resources.Configure components to automatically inherit controllers and data resources when placed on pages.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-08-06"
reading_time_minutes: 2
breadcrumb: [Component Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Enable configuration of components with inherited controllers in component builder

Learn how components can inherit page resources.

Using component builder, developers add data resources in two ways: directly within the component or through inheritance from the page.

## Direct configuration

When you add data resources directly to a component, they remain contained within that component. These internal data resources are not visible or accessible when the component is placed on a page.

## Inheritance

You can configure a component to inherit data resources from the page where it's placed. When inheritance is enabled, the component scans for data resources of the same type and automatically connects to them. For example, a component configured to inherit form controllers will look for form controllers on the page. This allows the component to be used across different page contexts and leverage existing data resources without manual configuration each time.

When you place a component configured for inheritance on a page, the inheritance behavior works as follows:

|Matching resources found|Behavior|
|------------------------|--------|
|No match found|Creates a new resource of the same type using the component's initial configuration|
|One|Connects to that resource|
|Multiple|Connects to the first instance of that resource|

**Parent Topic:**[Component Builder](component-builder-uib.md)

## Enable configuration of components with inherited controllers

Configure components to automatically inherit controllers and data resources when placed on pages.

### Before you begin

Role required: ui\_builder\_admin

### About this task

In this Component Builder example, we will create a text component and configure it to inherit the List controller. We will then place it on an list page where the component connects to the List controller and displays the appropriate table name.

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select **Create** from the UI Builder home page.

    ![UI Builder home page with the Create component button.](../image/create-component-button.png)

3.  Select **Component**.

4.  In the form, enter the following values:

    |Field|Value|
    |-----|-----|
    |Name|`Table Reference`|
    |Categories|**Content**|
    |Description|`Text component that displays the name of the current page's table`|
    |Icon|\(Default\)|

5.  Select **Create**.

6.  Add a data resource to the component.

    1.  In the data resource drawer, select **+ Add data resource**.

    2.  On the left, select **List Controller**.

    3.  On the right, select **Advanced configurations** to expand the section.

    4.  Select the **Inherit configurations from parent** option to enable the property.

    5.  Select **Add**.

    ![Select a data resource modal with List controller selected and Inherit configurations from parent enabled.](../image/inherit-controllers-inherit.png)

7.  Create the component.

    1.  In the content tree, select **+ Add content**.

    2.  Select **Single column**, then select **Add**.

    3.  In the content tree, select **+ Add content** under **Column 1**.

    4.  Select a **Stylized text**, then select **Add**.

    5.  Select **Cancel** to close the preset window.

8.  Configure the component to use the List controller.

    1.  In the configuration panel, hover over **Text** and select the bind data ![](../image/data-icon.png) icon.

    2.  On the left, select the **Formulas** tab, then double-click **CONCAT**.

    3.  In the upper section, double-click **value1** to edit the field and enter `"List showing records from "`.

    4.  Double-click **values** to edit the field and enter `@data.list_controller_1.tableLabel`.

    5.  Select **Apply**.

9.  Select **Save** to save your work.

    Your custom component is now available in the toolbox and ready for use in a page.

10. Place the component on a list page to see it automatically inherit the List controller and display the table name.

    ![UI Builder editor showing custom component inheriting the list controller and displaying the table name.](../image/inherit-controllers-result.png)


