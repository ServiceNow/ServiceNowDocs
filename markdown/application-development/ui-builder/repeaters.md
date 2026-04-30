---
title: Add repeaters to components
description: In UI Builder, use repeaters to repeat one or more components with results from a data resource.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure components and repeaters \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add repeaters to components

In UI Builder, use repeaters to repeat one or more components with results from a data resource.

## Before you begin

Role required: ui\_builder\_admin

## About this task

The repeater component acts as a basic loop that repeats the data you provide in multiple components within UI Builder. Repeaters use an array or an array of objects. For example, the array `[{"task": "A"},{"task": "B"}]` repeats the content inside it two times. Repeaters enable you to [bind](../concept/ui-builder-glossary.md#) values to a data array property. `@item.value.{property_name}` binds the values to the component inside the repeaters. If you want to bind a task, you can bind it as `@item.value.task`, and the repeater displays the correct value.

Components inside a repeater repeat the number of items in the data source, regardless of whether the component output is made dynamic or not. For example, say that you place a Header component inside a repeater with three data elements but don't change the Label field. Then you see three instances of the Header with the same output Label.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Open the editor for the page where you want to add the repeater.

    If you haven't created a page for your experience, see [Create a page in UI Builder](create-page.md) for more information on how to create a page.

4.  Connect a data resource to your page.

    For example, add the **Look up multiple records** data resource to your page. See [Add and configure data resources to a page](add-data-resources.md) for more information on connecting a data resource.

    1.  In the data resource drawer, select **+ Add data resource**.

    2.  In the modal, search for the **Look up multiple records** data resource and select **Add**.

    3.  In the **Table** field, enter `Incident`.

    4.  In the **Max results** field, enter `5`.

        The **Look up multiple records** data resource is configured.

        ![Data resource configuration with Incident table selected, "opened" and "short description" return fields added, max results set to 5.](../image/uib-repeater-data-resource.png)

    5.  Close the modal.

5.  Select an existing container or create a column layout.

    See [Organize components in UI Builder pages](../concept/work-layouts.md) for more information.

6.  Add the repeater component to your page.

    ![Arrow pointing to repeater component in the toolbox.](../image/uib-add-repeater.png)

    For information about adding components, see [Add and configure components](add-components.md#).

7.  In the **Configure** tab, select **None - Configure the component manually**.

8.  In the **Configure** tab, add an array that defines the data for repeated components.

    1.  Point to **Data array** and select the Bind data icon \(![Dynamic data binding icon.](../image/uib-dynamic-data-binding-button.png)\).

    2.  Under **Data types**, select **Data resource**.

    3.  In the next column, select the **Look up multiple records 1** pill.

    4.  Under **Pill view**, double-click or drag **results** to add the **@data.look\_up\_multiple\_records\_1.results** output.

    5.  Select **Apply**.

        The results from the data resource are bound to the repeater component. Within the repeater, one component represents each result.

        ![Data binding configuration with @data.look_up_multiple_records_1.results added](../image/uib-repeater-array.png)

9.  Under the repeater that you added in the previous step, select **+ Add content**.

    ![Content tree with a black arrow pointing to the Add content link under the repeater component.](../image/uib-repeaters.png)

10. Add a **Heading** component.

11. In the **Configure** tab, select **None - Configure the component manually**.

12. Configure the component you nested in the repeater.

    For example, bind the **displayValue** to the component. See [Connect data to your components](connect-data.md) for more information.

    1.  Move your cursor to the **Label** field and select the Bind data icon \(![Dynamic data binding icon.](../image/uib-dynamic-data-binding-button.png)\).

    2.  Under **Data types**, select **Repeater**.

    3.  Under **Pill view**, select the **value** pill.

    4.  In the next column, select the **number** pill.

    5.  In the next column, double-click or drag **displayValue** to add the **@item.value.number.displayValue** output.

    6.  Select **Apply**.

        The **displayValue** is bound to the Heading component.

        ![Data binding configuration with @item.value.number.displayValue added](../image/uib-repeater-component-config.png)

13. Select **Save**.

    The component you bound to the data resource appears on the stage and is repeated five times, once for each result returned from the Incident table.

14. View and test your page by selecting the **Preview** button.

    A tab opens to display the page preview with repeated data.


**Parent Topic:**[Configure components and repeaters \(advanced feature\)](../concept/configure-comp-and-repeaters.md)

