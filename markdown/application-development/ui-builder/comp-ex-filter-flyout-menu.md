---
title: Filter records by priority with a flyout menu
description: Configure a flyout menu that filters a task record list based on priority.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [UI Builder, UIB, Components, Flyout menu, Record list, List, Use case]
breadcrumb: [Learn components by example, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Filter records by priority with a flyout menu

Configure a flyout menu that filters a task record list based on priority.

## Before you begin

Role required: ui\_builder\_admin

This procedure uses UI Builder components to create dynamic, interactive layouts. For more information on how to configure components, see:

-   [Add and configure components](add-components.md#)
-   [UI Builder Quick Bits: Navigating Component Configuration](https://www.servicenow.com/community/next-experience-blog/ui-builder-quick-bits-navigating-component-configuration/ba-p/3181624)

<table id="table_exc_zzf_dhc"><thead><tr><th>

Component

</th><th>

Documentation links

</th></tr></thead><tbody><tr><td>

Flyout menu

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/now-flyout-menu?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-flyout-menu/uib-setup%23properties)

</td></tr><tr><td>

Record list

</td><td>

[Usage Guidelines](https://horizon.servicenow.com/workspace/components/record-list?release=zurich)

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create a page from scratch.

    For more information about how to create a page, see [Create a page in UI Builder](create-page.md).

4.  Select **Add content** on the stage or in the content tree to open the toolbox, then add a **Record list** component to the page.

5.  In the **Data and scripts** panel, select the **List Controller** data resource that was auto-created with the record list component.

    1.  Set **Table** to Task.

    2.  Set **Record count limit** to `25`.

    3.  Under **Returned fields**, add the fields you want to display in the list \(for this example, add **Number**, **Short description**, **Priority**, and **State**\).

6.  In the **Data and scripts** panel, select **Client state parameters** and then select **Add**.

7.  Configure the client state parameter:

    1.  Set **Name** to `priorityFilter`.

    2.  Set **Type** to **JSON**.

    3.  Set **Initial value** to `["1","2","3","4","5"]` so all task records display on page load.

8.  Select the **List Controller** data resource again, then select **Edit fixed filter**.

9.  Configure the filter condition:

    1.  Set the first field to `Priority`.

    2.  Set the operator to `is one of`.

    3.  Hover over the third field and select the bind data icon ![](../image/uib-dynamic-data-binding-button.png).

    4.  In the data binding modal, select **Client states**, then double-click or drag the `priorityFilter` pill to move it to the area above.

    5.  Select **Apply** to confirm the binding.

    6.  Select **Apply** to save the condition.

10. Add and configure a Flyout menu component.

    1.  In the content tree, hover over **Record list** and select the **Configure** icon ![](../image/uib-configure-icon.png).

    2.  Select **Add before**.

    3.  Search for **Flyout menu**, select it from the toolbox and then select **Add**.

    4.  In the configuration panel, hover over **List items**, then select **Edit**.

    5.  Set the **Mode** to **JSON** and replace the existing code with the following array:

        ```
        [
          {"id": "1", "label": "1 - Critical"},
          {"id": "2", "label": "2 - High"},
          {"id": "3", "label": "3 - Moderate"},
          {"id": "4", "label": "4 - Low"},
          {"id": "5", "label": "5 - Planning"}
        ]
        
        ```

    6.  Select **Apply**.

11. In the content tree, locate the **trigger** slot under **Flyout menu** and select **Add content**.

12. Add a button from the toolbox.

    This button will open the flyout menu.

13. Configure the flyout menu to update the list and refresh the data resource when the user selects an item.

    1.  In the configuration panel, select the **Events** tab.

    2.  Under **Flyout menu selected items set**, select **Add handler**.

    3.  Select the **Set client state parameter** handler, then select **Continue**.

    4.  Set the following properties:

<table id="table_krr_ftc_vgc"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Client State Parameter Name

</td><td>

Select **priorityFilter** from the list.

</td></tr><tr><td>

Value to use after triggering event

</td><td>

1.  Hover over the field and select the bind data icon ![](../image/uib-dynamic-data-binding-button.png).
2.  Select **Data types**, then **Event payload**.
3.  Under **Pill view**, double-click or drag the **value** pill to move it to the area above.
4.  Select **Apply** to confirm the binding.
5.  Select **Add**.


</td></tr></tbody>
</table>    5.  In the **Events** tab in the configuration panel, select **Add handler** underneath the event we added in the previous step.

    6.  Locate **List Controller**, select the **REFRESH** handler, then select **Continue**.

        ![Events modal with the List Controller - Data refresh requested handler selected.](../image/comp-ex-ffm-events.png)

    7.  Select **Add**.

    8.  Select **Save**.

14. Preview and test the page.

    ![Preview of UI Builder page showing the record list filtered for a specific priority.](../image/comp-ex-ffm-result.png)


**Parent Topic:**[Learn components by example](../concept/learning-components-by-example.md)

