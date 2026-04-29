---
title: Create dynamic filtered card displays
description: Create an interactive card layout to display records, add a dropdown to filter visible cards by name, and configure each card to open the full record in another UI Builder page when selected.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 12
keywords: [UI Builder, UIB, Components, Repeater, Heading, Label value, Stylized text, Highlighted value, Dropdown, Card base container, Use case]
breadcrumb: [Learn components by example, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create dynamic filtered card displays

Create an interactive card layout to display records, add a dropdown to filter visible cards by name, and configure each card to open the full record in another UI Builder page when selected.

## Before you begin

Role required: ui\_builder\_admin

## About this task

This example shows how to bind data to components so you can display record information in custom layouts. For example, you can present records as selectable cards rather than in a traditional list view. For this procedure, the data comes from the Incident table.

This procedure uses UI Builder components to create dynamic, interactive layouts. For more information on how to configure components, see:

-   [Add and configure components](add-components.md#)
-   [UI Builder Quick Bits: Navigating Component Configuration](https://www.servicenow.com/community/next-experience-blog/ui-builder-quick-bits-navigating-component-configuration/ba-p/3181624)

<table id="table_exc_zzf_dhc"><thead><tr><th>

Component

</th><th>

Documentation links

</th></tr></thead><tbody><tr><td>

Card Base Container

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/now-card?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-card/uib-setup%23properties)

</td></tr><tr><td>

Dropdown

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/now-dropdown?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-dropdown/uib-setup%23properties)

</td></tr><tr><td>

Heading

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/now-heading?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-heading/uib-setup%23properties)

</td></tr><tr><td>

Highlighted value

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/now-highlighted-value?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-highlighted-value/uib-setup%23properties)

</td></tr><tr><td>

Label value

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/now-label-value-inline?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-label-value-inline/uib-setup%23properties)

</td></tr><tr><td>

Stylized text

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/now-stylized-text?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-stylized-text/uib-setup%23properties)

</td></tr></tbody>
</table>## Procedure

1.  Part 1: Build the card layout

    Add a repeater linked to a data resource and create the card containers that display each record.

2.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

3.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

4.  Create a page from scratch.

    For more information about how to create a page, see [Create a page in UI Builder](create-page.md).

5.  Create a data resource to pull records from the Incident table.

    Data resources expose data from tables and records to the page. In this example, we add a data resource to pull records from the incident table so we can display them using components. For more information, see [Add and configure data resources to a page](add-data-resources.md).

    1.  In the **Data and scripts** drawer, under **Data resources**, select **+ Add data resource**.

    2.  Select **Look up multiple records** and then select **Add**.

    3.  Select the **look\_up\_multiple\_records\_1** ID to open the **Data resource details** form.

    4.  Replace the text in the **Data resource label** field with `Incident lookup`.

        The **Data resource ID** field auto-populates.

    5.  Select **Apply**.

    6.  In the **Edit Incident lookup** dialog, fill in the fields:

<table id="table_kvg_n1c_vgc"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Enter `incident`, then select it from the list.

</td></tr><tr><td>

Return fields

</td><td>

1.  Select **+ Add**.
2.  Enter `Caller`, select it to add it to the **Selected** column, then clear the search box.
3.  Repeat the above step for **Priority** and **Short description**.

![Choose fields modal showing Caller, Priority, and Short description.](../image/comp-ex-dfc-data-resource-fields.png)

4.  Select **Apply**.


</td></tr><tr><td>

Max results

</td><td>

Enter `25`.

</td></tr></tbody>
</table>        ![Edit data resource dialog for "Incident lookup" with callouts highlighting the Table, Return fields, and Max results fields.](../image/comp-ex-dfc-data-resource.png)

    7.  Select the **X** in the upper right to close the dialog.

    8.  Select **Save**.

6.  Add a single column layout to hold the components.

    1.  In the content tree, under **Body**, select **+ Add content**.

    2.  Select **Single column** and then select **+ Add**.

    3.  With **Column 1** selected in the content tree, navigate to **Layout** in the configuration panel and set the **Direction** to **Row**.

        ![Configuration panel for single column layout, with a cursor hovering over the Direction > Row property.](../image/comp-ex-dfc-layout-row.png)

7.  Add and configure a repeater on your page with data binding.

    Data binding is the process of associating data exposed by a data resource with a component. In this example, we bind the results of our **Incident lookup** data resource to the **Data array** property of the repeater component. For more information, see [Connect data components](../concept/connect-data-components.md).

    1.  In the content tree, under **Column 1**, select **+ Add content**.

    2.  Enter `Repeater`, then select it in the toolbox and then select **Add**.

    3.  Select **Cancel** to close the preset window.

    4.  Keeping **Repeater 1** selected, in the configuration panel, hover over the **Data array** field and select the bind data icon ![](../image/uib-dynamic-data-binding-button.png).

        ![Configurational panel for repeater, with a cursor hovering over the bind data icon.](../image/comp-ex-dfc-bind-data.png)

    5.  In the **Bind data to Data array** dialog, under **Data types**, select **Data resource**.

    6.  Select the **Incident lookup** pill, then double-click or drag the **results** pill to move it to the area above.

        ![Data binding modal showing the selection of data resource pills to configure the repeater.](../image/comp-ex-dfc-repeater.png "Bind data to Data array")

    7.  Select **Apply** to confirm the binding.

    8.  In the configuration panel, select the **Styles** tab, select **Enable styles**, then fill in the fields:

        |Field|Value|
        |-----|-----|
        |Type|**Grid**|
        |Columns|`4`|
        |Gap|**S**|

    9.  Select **Save**.

8.  Create the card display.

    1.  In the content tree, under **Repeater 1**, select **+ Add content**.

    2.  Enter `Card Base Container`, select the component, then select **+ Add**.

    3.  In the configuration panel, select the **Configure** tab and set the **Interaction** to **Click**.

    4.  In the configuration panel, select the **Styles** tab and set the **Width** to `300`px.

    5.  Set the **Height** to `200`px.

        ![Configuration panel for Card Base Container, with callouts highlighting the Width and Height fields.](../image/comp-ex-dfc-card-style.png)

9.  Part 2: Add components and bind data

    Add components to each card and configure them to display record details by binding the appropriate fields.

10. Add components to the card base container.

    1.  In the content tree, under **Card Base Container 1**, select **+ Add content**.

    2.  Add the following components in the order listed below and edit each in the configuration panel:

        **Tip:** To keep all components nested in **Card Base Container**, add the first component, then use **Add after** from the configure icon ![](../image/uib-configure-icon.png) for each one that follows.

        If a preset window appears, select **Cancel** to close it.

        1.  Heading: No initial configuration required
        2.  Label value: In the **Configure** tab, in the **Label** field, enter `Caller:`
        3.  Stylized text: In the **Configure** tab, set the **HTML tag** to **Paragraph**
        4.  Highlighted value: In the **Styles** tab, set the **Width** to `100`px
        ![UI Builder editor with callouts highlighting the Repeater and its nested components in the content tree.](../image/comp-ex-dfc-cards.png)

    3.  Select **Save**.

11. Bind data from the incident records to the components we added in the previous step.

    |Component|Field|Path|
    |---------|-----|----|
    |Heading|**Label**|`value > number > displayValue`|
    |Label value|**Value**|`value > caller_id > displayValue`|
    |Stylized text|**Text**|`value > short_description > displayValue`|
    |Highlighted value|**Label**|`value > priority > displayValue`|

    1.  In the content tree, select the component listed in the table.

    2.  In the configuration panel, on the Configure tab, hover over the specified field and select the bind data icon ![](../image/uib-dynamic-data-binding-button.png).

    3.  In the data binding modal:

        -   On the left, select **Repeater** under **Data types**.
        -   On the right, under **Pill view**, follow the path listed in the table by selecting each pill in order \(for example, for Heading, select **value**, then **number**, then **displayValue**\).
    4.  When you reach the final pill \(**displayValue**\), double-click or drag it to move it to the area above, then select **Apply**.

    5.  Repeat the process for each row in the table.

        ![UI Builder editor showing data-bound values on each card.](../image/comp-ex-dfc-cards2.png)

    6.  Select **Save**.

12. Use a script to define the color of the priority for each record.

    1.  In the content tree, select **Highlighted value 1**.

    2.  In the configuration panel, on the Configure tab, hover over **Color** and select the bind data icon ![](../image/uib-dynamic-data-binding-button.png).

    3.  Select the **Use script** icon ![](../image/uib-use-script-icon.png) in the upper right.

    4.  Replace the existing code with the following:

        ```
        function getPriorityColor(record) {
            let priority = record.api.item.value.priority.value;
        
            switch (priority) {
                case '1':
                    return 'critical';
                case '2':
                    return 'high';
                case '3':
                    return 'moderate';
                case '4':
                    return 'low';
                case '5':
                    return 'gray';
                default:
                    return 'gray';
            }
        }
        ```

    5.  Select **Apply**.

    Verify that the highlighted value changes color depending on the priority of the record.

    ![UI Builder editor showing highlighted value in a different color, depending on record priority.](../image/comp-ex-dfc-cards3.png)

13. Part 3: Add filtering with dropdown

    Configure a dropdown event to update a client state parameter and refresh the data resource, filtering the card display.

14. Create a client state parameter to track user selections.

    The client state parameter can be modified by components when they trigger events. For more information, see [Client state parameters](../concept/client-state-parameters.md).

    1.  In the **Data and scripts** drawer, next to **Client state parameters**, select the **+** icon.

    2.  In the **Edit client state parameters** dialog, fill out the fields:

        -   Name: `selected_caller`
        -   Type: **String**
        -   Initial value: empty
    3.  Select **Apply.**

15. Edit the data resource to use the client state parameter as a conditional value.

    1.  In the **Data and scripts** drawer, select the **Incident lookup** data resource.

    2.  Select **Edit conditions**.

        ![Edit Incident lookup dialog with a highlight over the Edit conditions button.](../image/comp-ex-dfc-edit-conditions.png)

    3.  In the **Conditions** dialog, enter **Caller** in the first field and select it from the list.

    4.  Leave the second field as is.

    5.  Hover over the third field and select the bind data icon ![](../image/uib-dynamic-data-binding-button.png).

    6.  In the data binding modal, select **Client states**, then double-click or drag the `selected_caller` pill to move it to the area above.

    7.  Select **Apply** to confirm the binding.

    8.  Select **Apply** to save the condition.

        ![Conditions modal showing the condition, Caller is selected_caller.](../image/comp-ex-dfc-conditions.png)

    9.  Select the **X** in the upper right to close the **Incident lookup** dialog.

16. Create a second data resource to query users from the user table.

    1.  In the **Data and scripts** drawer, select the **+**, then select **Data resource**.

    2.  Select **Look up multiple records** and then select **Add**.

    3.  Select the **look\_up\_multiple\_records\_1** ID to open the **Data resource details** form.

        ![Edit data resource dialog with a highlight over the label and ID fields.](../image/comp-ex-dfc-data-resource2.png)

    4.  Replace the text in the **Data resource label** field with `sys_user_lookup`.

        The **Data resource ID** field auto-populates.

    5.  Select **Apply**.

    6.  In the **Edit sys\_user\_lookup** dialog, fill in the fields:

<table id="table_hgn_d3t_wgc"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Enter `User (sys_user)` and then select it from the list.

</td></tr><tr><td>

Return fields

</td><td>

1.  Select **+ Add**.
2.  Enter `Name`, then select it from the list to add it to the **Selected** column.
3.  Select **Apply**.


</td></tr><tr><td>

Order by

</td><td>

Enter `Name`, then select it from the list.

</td></tr><tr><td>

Max results

</td><td>

Enter `250`.

</td></tr></tbody>
</table>    7.  Select the **X** in the upper right to close the dialog.

    8.  Select **Save**.

    This data resource looks up users from the user table. We will reference this data to populate the dropdown in the next step.

17. Add and configure a dropdown component.

    1.  In the content tree, hover over **Column layout 1** and select the **Configure** icon ![](../image/uib-configure-icon.png).

    2.  Select **Add before**.

    3.  Search for **Dropdown**, select it from the toolbox and then select **Add**.

    4.  In the configuration panel, navigate to the specified tab and configure the following fields:

<table id="table_bn3_crc_vgc"><thead><tr><th>

Tab

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Configure

</td><td>

In the **Placeholder text** field: Enter `Select a caller`.

</td></tr><tr><td>

Configure

</td><td>

In the **Variant** field: Select **Primary**.

</td></tr><tr><td>

Configure

</td><td>

In the **List items** field:1.  Hover over the field and select the bind data icon ![](../image/uib-dynamic-data-binding-button.png).
2.  In the data binding modal, select the **Use script** icon ![](../image/uib-use-script-icon.png).
3.  Replace the existing code with the following:

**Tip:** You can select the format code icon ![](../image/comp-ex-dfc-format-code-icon.png) to make the code more readable.

    ```
function evaluateProperty({ api, helpers }) {
    const userArray = api.data.sys_user_lookup.results;

    let outputArray = [];

    for (let i = 0; i < userArray.length; i++) {
        const obj = {
            'id': `${userArray[i]._row_data.uniqueValue}`,
            'label': `${userArray[i].name.displayValue}`
        };
        outputArray.push(obj);
    }

    return outputArray;
}
    ```

4.  Select **Apply**.


</td></tr><tr><td>

Styles

</td><td>

Width: Enter `200`.

</td></tr><tr><td>

Styles

</td><td>

Padding: Select **Padding**, then choose **M** from the list.

</td></tr></tbody>
</table>18. Configure the dropdown with events so that it can modify the client state parameter we created.

    1.  With **Dropdown 1** selected in the content tree, select the **Events** tab in the configuration panel, then select **Add event mapping**.

    2.  Select the **Selected items changed** event, then select **Continue**.

    3.  Select the **Set client state parameter** handler, then select **Continue**.

    4.  Set the following properties:

<table id="table_krr_ftc_vgc"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Client State Parameter Name

</td><td>

Select **selected\_caller** from the list.

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

    6.  Locate **Incident lookup \(1\)**, select the **REFRESH** handler, then select **Continue**.

        ![Events modal with the Incident lookup - REFRESH handler selected.](../image/comp-ex-dfc-dropdown-events.png)

    7.  Select **Add**.

    8.  Select **Save**.

    After configuring the dropdown, selecting a caller updates the `selected_caller` client state parameter and refreshes the data resource to display that caller's records.

19. Part 4: Enable record navigation

    Configure each card so that selecting it opens the record page using the sys\_id from the repeater data.

20. Create another page in your experience that opens the record.

    1.  Return to the experience view by selecting the name of your experience \(for example, "Demo Experience"\) in the upper left.

    2.  Select the **+** next to **Pages**, then select **Create a new page**.

    3.  Hover over the **Standard record** template and select **Use template**.

    4.  Name your page `Incident record page` and select **Continue**.

    5.  Select **Looks Good**, then select **Create**.

21. Return to your original page by selecting the name of your experience in the upper left, then choosing your page from the experience view.

22. Add an event to the cards so that selecting a card opens its record on the page we created.

    1.  Select **Card Base Container 1** in the content tree.

    2.  In the configuration panel, select the **Events** tab, then select **Add event mapping**.

    3.  Select the **Card clicked** event, then select **Continue**.

    4.  Select the **Open page or URL** handler, then select **Continue**.

    5.  Select **Pages in current experience**.

    6.  Select **Incident record page**.

    7.  In the form, fill in the fields:

<table id="table_sks_4wc_vgc"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

table

</td><td>

Enter `incident`

</td></tr><tr><td>

sysId

</td><td>

1.  Hover over the **sysId** field and select the bind data icon ![](../image/uib-dynamic-data-binding-button.png).
2.  Locate **Data types** on the left and select **Repeater**.
3.  In the **Pill view**, select **value**, then **\_row\_data**, then double-click **uniqueValue**.
4.  Select **Apply**.


</td></tr></tbody>
</table>    8.  Select **Select**.

        ![Select page destination modal.](../image/comp-ex-dfc-card-events.png)

    9.  Select the check box to enable the **Open in new tab** property.

    10. Select **Add**.

    11. Select **Save**.

23. Preview and test the page.

    1.  Select **Preview**.

    2.  In the dropdown, select a user such as "Fred Luddy," "Carol Coughlin," or "Bow Ruggeri" to filter the cards.

        **Note:** Some users do not have related incident records, so selecting those users will result in no cards being displayed.

    3.  Select a card to view the full record in a new tab.

    ![Preview of UI Builder page showing the card display filtered for a specific user.](../image/comp-ex-dfc-result.png)


**Parent Topic:**[Learn components by example](../concept/learning-components-by-example.md)

