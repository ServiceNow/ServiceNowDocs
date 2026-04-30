---
title: Fetch data from multiple sources
description: Learn how to obtain data from different sources to use in a single component.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Multi-table data configuration, Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Fetch data from multiple sources

Learn how to obtain data from different sources to use in a single component.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Place the card base container component in a repeater and use multi-table data configuration to present all active incidents and problems created in the last two years.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create &gt; Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create a page from scratch.

    For more information about how to create a page, see [Create a page in UI Builder](create-page.md).

4.  Add a multi-table data resource.

    1.  In the data shelf, select **+ Add data resource**.

        ![Data shelf with black arrow pointing to add data resource option.](../image/multi-table-data-source1.png)

    2.  In **Search**, enter `multi-table`.

    3.  Select **Multi-table data**.

        ![Data resource pop-up with black arrow pointing to search field and black arrow pointing to multi-table data resource.](../image/multi-table-data-source2.png)

    4.  Select **Add**.

5.  Configure the first data source.

    1.  In **Data sources**, select **+ Add**.

        ![Multi-table data resource options with black arrow pointing to add option next to the data sources field.](../image/multi-table-data-source3.png)

    2.  In **Table**, enter `incident` and select the **Incident** table.

    3.  In **Sort field**, enter `number` and select **Number**.

    4.  In **Name**, enter `Incident`.

    5.  In **Return fields**, add **Number**, **State**, **Description**, and **Active**.

        ![Add data sources pop-up with all fields completed.](../image/multi-table-data-source4.png)

    6.  Select **Edit conditions**.

    7.  Build the condition **Active is true**.

    8.  Select **and**.

    9.  Build the condition **Created on Last 2 years**.

        ![Conditions popup with two conditions displayed.](../image/multi-table-data-source5.png)

    10. Select **Apply**.

    11. Select **Apply**.

6.  Configure the second data source.

    1.  In **Data sources**, select **+ Add**.

    2.  In **Table**, enter `problem` and select the **Problem** table.

    3.  In **Sort field**, enter `number` and select **Number**.

    4.  In **Name**, enter `Problem`.

    5.  In **Return fields**, add **Number**, **State**, **Description**, and **Active**.

        When creating a multi-table data resource, each data source should have the same return fields specified and in the same order. This helps ensure that the data displayed on the page is consistent and accurate.

        ![Add data sources pop-up with all fields completed.](../image/multi-table-data-source6.png)

    6.  Select **Edit conditions**.

    7.  Build the condition **Active is true**.

    8.  Select **and**.

    9.  Build the condition **Created on Last 2 years**.

    10. Select **Apply**.

    11. Select **Apply**.

    12. Select the **X** to close the **Edit Multi-table data** pop-up.

7.  Select **Save**.

8.  Add the heading component.

    1.  In the content tree, select **+ Add content** under **Body**.

    2.  In **Search** enter `heading`.

    3.  Select the **Heading** component.

    4.  In the configuration panel, on the **Configure** tab, select **None - Configure the component manually**.

    5.  In **Label**, delete the default text and enter `Active incidents and problems created in last two years`.

        ![Configure tab for heading component with black arrow pointing to completed label field.](../image/multi-table-data-source7.png)

    6.  Select **Save**.

9.  Add a container.

    1.  In the content tree, select **+ Add content** under **Heading 1**.

    2.  On the **Layouts** tab, in the **Advanced** section, select **Flexbox**.

        ![Toolbox with layout tab displayed and black arrow pointing to flexbox option.](../image/multi-table-data-source8.png)

    3.  In the configuration panel, on the **Configure** tab, select **None - Configure the component manually**.

    4.  In **Sizing**, set the **Width** by entering `300`.

        ![Styles tab for container component with black arrow pointing to completed width field.](../image/multi-table-data-source9.png)

    5.  Select **Save**.

10. Add the repeater component.

    1.  In the content tree, select **+ Add content** under **Container 1**.

    2.  In **Search** enter `repeater`.

    3.  Select the **Repeater** component.

    4.  In the configuration panel, on the **Configure** tab, select **None - Configure the component manually**.

    5.  Select **Save**.

    6.  In the configuration panel, on the **Configure** tab, hover over the **Data array** field and select the bind data icon.

        ![Configure panel for repeater component with black arrow pointing to data array field bind data icon.](../image/multi-table-data-source10.png)

    7.  Under **Data types** select **Data resource**.

    8.  Select **Multi-table data 1**.

    9.  Select **output** &gt; **data** &gt; **GlideMultiDatasource\_Query** &gt; **getMultiDatasourceData**.

    10. Double-click \(or use the keyboard shortcut\) on the **items** pill.

        ![Data binding modal with black arrow pointing to items pill.](../image/multi-table-data-source11.png)

        Check that the top section is accurate.

        ![Data binding modal with black arrow pointing to top section.](../image/multi-table-data-source12.png)

    11. Select **Apply**.

    12. Select **Save**.

11. Add the card base container component within the repeater.

    1.  In the content tree, select **+ Add content** under **Repeater 1**.

    2.  Locate and select the **Card Base Container** component.

    3.  In the configuration panel, on the **Configure** tab, select **None - Configure the component manually**.

    4.  Select the **Styles** tab.

    5.  To add a little space around the cards, go to **Spacing**, select **Margin**, and then select **M** \(for medium\).

        ![Styles panel for card base container component with black arrow pointing to margin option and the medium margin setting.](../image/multi-table-data-source13.png)

    6.  Select **Save**.

12. Add the heading component within the card base container.

    1.  In the content tree, select **+ Add content** under **Card Base Container 1**.

    2.  Locate and select the **Heading** component.

    3.  In the configuration panel, on the **Configure** tab, select **None - Configure the component manually**.

    4.  In the configuration panel, on the **Configure** tab, delete the default text in **Label**.

    5.  Point to the **Label** field and select the bind data icon.

    6.  Under **Data types** select **Repeater**.

    7.  Select **value** &gt; **fields**.

    8.  Select the top pill and in the last column check for **displayValue** with an incident or problem number.

    9.  Double-click \(or use the keyboard shortcut\) on the **displayValue** pill with an incident or problem number.

        ![Data binding modal with black arrow pointing to display value pill.](../image/multi-table-data-source14.png)

        Check that the top section is accurate.

        ![Data binding modal with black arrow pointing to top section.](../image/multi-table-data-source15.png)

    10. Select **Apply**.

    11. On the **Configure** tab, select the **Hide bottom margin** option.

        ![Configure panel for heading component with black arrow pointing to hide bottom margin option.](../image/multi-table-data-source16.png)

    12. Select **Save**.

13. Add the first stylized text component to show the description of the incident or problem.

    1.  In the content tree, point to **Heading 2**, select the menu \(three vertical dots\) icon, and select **Add after**.

        ![Content tree with black arrow pointing to menu icon and black arrow pointing to add after option in floating menu.](../image/multi-table-data-source17.png)

    2.  Locate and select the **Stylized text** component.

    3.  In the configuration panel, on the **Configure** tab, select **None - Configure the component manually**.

    4.  In the configuration panel, on the **Configure** tab, delete the default text in **Text**.

    5.  Point to the **Text** field and select the bind data icon.

    6.  Under **Data types** select **Repeater**.

    7.  Select **value** &gt; **fields**.

    8.  Select the third pill in the list and in the last column check that the **displayValue** contains no information.

    9.  Double-click \(or use the keyboard shortcut\) on the **displayValue** pill with no value.

        ![Data binding modal with black arrow pointing to display value pill.](../image/multi-table-data-source18.png)

        Check that the top section is accurate.

        ![Data binding modal with black arrow pointing to top section.](../image/multi-table-data-source19.png)

    10. Select **Apply**.

    11. To reduce the text size, go to the **Configure** tab and change the **HTML tag** to **Paragraph**.

    12. Select **Save**.

14. Add the second stylized text component to show the state of the incident or problem.

    1.  In the content tree, point to **Stylized text 1**, select the menu \(three vertical dots\) icon, and select **Add after**.

    2.  Locate and select the **Stylized text** component.

    3.  In the configuration panel, on the **Configure** tab, select **None - Configure the component manually**.

    4.  In the configuration panel, on the **Configure** tab, delete the default text in **Text**.

    5.  Point to the **Text** field and select the bind data icon.

    6.  Under **Data types** select **Repeater**.

    7.  Select **value** &gt; **fields**.

    8.  Select the second pill in the list and in the last column check that the **displayValue** contains a state such as **Resolved** or **In Progress**.

    9.  Double-click \(or use the keyboard shortcut\) on the **displayValue** pill with a state value.

        ![Data binding modal with black arrow pointing to display value pill.](../image/multi-table-data-source20.png)

        Check that the top section is accurate.

        ![Data binding modal with black arrow pointing to top section.](../image/multi-table-data-source21.png)

    10. Select **Apply**.

    11. To reduce the text size, go to the **Configure** tab and change the **HTML tag** to **Paragraph**.

    12. Select **Save**.

15. Select **Preview**.

    The page heading is at the top. Each card contains a heading with the incident or problem number. The cards also show the description \(if one is available\) of the incident or problem and the state. Data is being pulled successfully from two sources: the incident table and the problem table.

    ![Preview overlay showing heading and card base container components configured with multi-table data sources.](../image/multi-table-data-source22.png)

16. Select the **X** to close the preview overlay.


**Parent Topic:**[Multi-table data configuration](../concept/multi-source-data-configuration.md)

