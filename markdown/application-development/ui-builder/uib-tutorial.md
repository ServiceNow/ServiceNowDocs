---
title: UI Builder tutorial
description: Learn how to use the basics of UI Builder to create a page called My Tutorial.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Exploring UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# UI Builder tutorial

Learn how to use the basics of UI Builder to create a page called My Tutorial.

## Before you begin

Role required: ui\_builder\_admin

In this UI Builder tutorial, you perform the following tasks to build a [page](../concept/ui-builder-glossary.md#) in UI Builder:

-   Start UI Builder.
-   Create a page for your workspace or custom portal experience. For more information about creating pages, see [Create a page in UI Builder](create-page.md).
-   Change the layout of the page to have two columns. For more information, see [Organize components in UI Builder pages](../concept/work-layouts.md).
-   Build your page by adding two container [components](../concept/ui-builder-glossary.md#).
-   Rename your container components in the content tree.
-   Add a **Heading** component and a **Button** component to the first container. Add a **data visualization component** to the second container. For more information about components, see [Customize UI Builder pages using components](../concept/work-components.md).
-   Configure your components as follows:
    -   Link the button to the ServiceNow® website.
    -   Connect the **Data visualization** component to a data source to display task data. For more information about data resources, see [Dynamically expose data in UI Builder pages \(advanced feature\)](../concept/data-resources.md).
-   Save your page often.
-   Preview your page to see how it looks in a browser.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

    You can also type `UI Builder` directly in the **Filter navigator**.

    ![Starting UI Builder.](../image/UIB-start-UIBuilder-video.gif "Start UI Builder")

2.  From the UI Builder home page, choose an experience you want to work in.

    If you don’t see any experiences listed in which to work, contact your administrator to get access to an experience or create an experience. For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).

3.  Create a page.

<table id="choicetable_n3q_gmd_jjb"><thead><tr><th align="left" id="d70438e252">

To do this task

</th><th align="left" id="d70438e255">

Do the following

</th></tr></thead><tbody><tr><td id="d70438e261">

**Create a page**

</td><td>

1.  Select the **+** icon in the **Pages and variants** section.

![Create page button on the experience view page.](../image/create-page-icon.png)

2.  Select **Create a new page**.

![Page type selection modal.](../image/page-create-popup.png)

3.  Select **Create from scratch instead**.

![Create from scratch instead button.](../image/create-page-scratch.png)

4.  Enter the name of your new page. The name can be anything you want. In this example, you can type `My tutorial page`.
5.  In the **Path** field, a path is automatically entered based on your page name. In this example, the Path is `my-tutorial-page`. The path is the URL of the page. You can change this path to anything you want, but the path must be unique. The path has to be lowercase and contain no spaces. The **URL preview** shows what the path of your page will be.

![Create a page called My tutorial page.](../image/tutorial-name-page.png)

6.  Select **Continue**.
7.  \(Optional\) Add parameters to your page URL.
8.  Select **Looks good**.
9.  Enter the name of your page variant. The name can be anything you want. In this example, you can type `My first page variant`.
10. Add an audience for the page variant by selecting **+ Add an audience**. In this example, select **Admin**.
11. Select **Continue**.
12. On the next screen, select **Build responsive**.
13. Select **Create**.
14. After your page is created, the page editor screen appears. You can change advanced settings such as the **URL settings** and **Variant** settings. For this tutorial, you can skip these advanced options. For more information on changing advanced settings, see [Create a UI Builder page: Advanced settings](../concept/work-pages.md#create_page_advanced_settings).
 ![UI Builder page editor showing the new page created in the tutorial.](../image/tutorial-page-editor.png "UI Builder Page Editor")

</td></tr></tbody>
</table>    Congratulations! You created your tutorial page! The page is empty of content. You add components to the page to build functionality to it. Components are the building blocks of a page. UI Builder comes with many components ready for you to add to your page. Components can be as simple as a **Heading**, or as complex as a **List**.

4.  Change the layout of the page to a two-column layout.

    For more information about layouts, see [Organize components in UI Builder pages](../concept/work-layouts.md).

<table id="choicetable_hgv_b1x_d4b"><thead><tr><th align="left" id="d70438e448">

To do this task

</th><th align="left" id="d70438e451">

Do the following

</th></tr></thead><tbody><tr><td id="d70438e457">

**Change the layout of the page to two columns**

</td><td>

1.  Select the **Body** level of the **Content** tree to highlight the page.
2.  Select **+ Add content** in the content tree.

![Pointer selecting + Add content in the content tree.](../image/qs-add-component.png)

3.  Select the **Two columns** layout.

![Arrow pointing to the two columns layout in the toolbox.](../image/tutorial-two-columns-select.png)

4.  The two column layout appears.

![The two column layout shown on the stage.](../image/tutorial-two-columns-on-stage.png)

</td></tr></tbody>
</table>5.  Add a **Heading** component, and a **Button** component to the left column.

<table id="choicetable_q1g_4fl_vnb"><thead><tr><th align="left" id="d70438e526">

To do this task

</th><th align="left" id="d70438e529">

Do the following

</th></tr></thead><tbody><tr><td id="d70438e535">

**Add a heading component to your left-column container**

</td><td>

You can add components to the page in different ways. For more information on the ways you can add components to your page, see [Table 1](../concept/work-components.md#addcomponentstable).1.  Select the **+** button in the middle of the left column.
2.  Type `Heading` in the search field.
3.  Select the **Heading** component to add it to your container. A heading component is a way to add text or a title to your page.
4.  Select **None** in the list of presets in the configuration panel.

![Adding a heading component to a column.](../image/tutorial-add-heading.gif)

5.  Select the component name in the configuration panel to see the **Component label** and **Component ID**. You can change these to anything you want, as long as they’re unique.

![Updating the component label and ID.](../image/tutorial-heading-label.png)

6.  Select **Apply**.
7.  Configure your **Heading** component. Component authors configure components to expose the appropriate properties required to set up their components.
    -   Set the style to **Header-primary**. The Style changes the class of the heading text, like font, weight, and color. For example, if you select **Header-secondary**, the text is smaller. Different headings sizes are useful if you have two headings and want the second heading smaller that the primary heading.
    -   Enter `My Tutorial` as the heading text in the **Label** field.
    -   Leave the Level as **1**.

![Heading label field in the component configure tab with My tutorial added.](../image/tutorial-heading-label-changed.png)

</td></tr><tr><td id="d70438e641">

**Add and configure a button component to your left-column container**

</td><td>

Add a **Button** component to your page. Configure the button by changing the text and the way that it looks. Then change what happens when you click the button by adding an event handler for the button. The event handler adds an action to the button to link to the ServiceNow® home page. So when you click the button, the ServiceNow® home page opens in a new tab of your browser. For more information about configuring components, see [Components](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/components).

 1.  Select the **+** on the bottom edge of the heading component that we added in the previous section.

![Arrow pointing to the + icon to add components after the heading.](../image/tutorial-add-component-icon.png)

2.  Type `Button` in the search field.
3.  Select the **Button** component in the list.

For more information on adding components to your page, see [Table 1](../concept/work-components.md#addcomponentstable).

4.  Select the component name in the configuration panel to see the **Component label** and **Component ID**. You can change these to anything you want, as long as they’re unique.
5.  Configure the button component as follows.
    -   Enter `Home Page` in the Label field to change the name of your button.
    -   Change the Size to **Large**.
    -   Enter `home` in the **Icon** search field.
    -   Select **Home Outline**.

![Home page button configuration.](../image/tutorial-home-button-config.png)

6.  Add an event handler to configure what action applies to the button.
    -   Select the **Events** tab in the configuration panel.
    -   Under Button clicked, select **+ Add a new event handler**.

![Arrow pointing to the + Add event handler link.](../image/tutorial-event-handler-add.png)

    -   Under Inherited event handlers, select **Link to destination**.
    -   Click **Select destination**.
    -   In the **Select destination** screen, select **External URL**.
    -   Type your URL. For this tutorial, type `https://www.servicenow.com` Select **OK**.
    -   Select **Add**.

![Configured event handler for the button component.](../image/tutorial-button-event.png)

For more information about event handlers, see [Manage actions in UI Builder pages](../concept/work-events.md).

7.  Select **Save**. It is always a good idea to save your page often as you work.
8.  Select **Preview**.
9.  Test the button you created in the previous steps.


</td></tr></tbody>
</table>    You added and configured the **Heading** and **Button** component for your page.

    ![UI Builder page with a heading and button configured.](../image/tutorial-heading-and-button.png)

6.  Add a **Data visualization** component to the container.

    A data visualization component contains data that you display in a visual manner. Configure the data visualization component parameters. Then, add a data resource to it.

<table id="choicetable_j31_whl_vnb"><thead><tr><th align="left" id="d70438e874">

To do this task

</th><th align="left" id="d70438e877">

Do the following

</th></tr></thead><tbody><tr><td id="d70438e883">

**Add and configure a data visualization component to your right-column container**

</td><td>

You can add components to the page in different ways. For more information on the ways you can add components to your page, see [Table 1](../concept/work-components.md#addcomponentstable).1.  Select the **+** button in the middle of the right column.
2.  In the **Search** field, start typing `Data visualization` until you see the **Data visualization** component, then select the component to add it to your page.
3.  Select the component name in the configuration panel to see the **Component label** and **Component ID**. You can change these to anything you want, as long as they’re unique.
4.  Add a data resource to your data visualization component to bring in customer account data.
    -   Select the data visualization component, then select the **Configure** tab.
    -   Select **Add data source**.
    -   Type `Task [task]` in the search field and look for a task that is available on your UI Builder instance.
    -   Select **Add this source**.

![Adding the data source to the data visualization component.](../image/tutorial-data-vis-add.gif)

5.  Select **Data visualization type** drop-down and select **Dial**. You can choose a variety of visualization types to best suit your data.
6.  Select **Header and border** in the configuration panel.
7.  Enter `My Tasks` in the **Chart title** field.

![Arrow pointing to the chart title field.](../image/tutorial-data-vis-title.png)

</td></tr></tbody>
</table>    You’ve added a **Data visualization** component to the right column and configured it. You also added a data resource to bring in customer account data.

7.  Save the new page one last time.

<table id="choicetable_md1_c5m_vnb"><thead><tr><th align="left" id="d70438e1012">

To do this task

</th><th align="left" id="d70438e1015">

Do the following

</th></tr></thead><tbody><tr><td id="d70438e1021">

**Save your page**

</td><td>

1.  In the far right corner of UI Builder, select **Save**.
2.  Now that you saved your page, you can access it in your experience at any time.


</td></tr></tbody>
</table>8.  Now preview your page to see what it looks like in a browser.

<table id="choicetable_cyg_qg2_24b"><thead><tr><th align="left" id="d70438e1054">

To do this task

</th><th align="left" id="d70438e1057">

Do the following

</th></tr></thead><tbody><tr><td id="d70438e1063">

**Preview your page**

</td><td>

1.  Select **Preview** in the UI Builder header.
2.  See the heading in the left column of your page.
3.  Select the **Home Page** button. The ServiceNow® home page opens in another browser tab. Close the browser tab to go back to your preview page.
4.  See the customer account data visualization in the right column of your page.

![Selecting Preview to view the tutorial page.](../image/tutorial-preview.gif "Preview your tutorial page")

</td></tr></tbody>
</table>    Congratulations! You completed the UI Builder tutorial.


## Result

1.  Created a page in UI Builder.
2.  Changed the layout of your page to have two columns.
3.  Added a **Heading** component as a title to your left column.
    -   Changed the text of the heading.
    -   Changed the label of the heading.
4.  Added a button component below your heading component.
    -   Configured your button.
    -   Added an event handler for your button.
    -   Added an event handler to set up a link to a web page. When you click the button, it opens the web page.
5.  Changed the label for the right column.
6.  Added a **Data visualization** component.
    -   Configured the data visualization component.
    -   Added a data resource to bring in task data.
7.  Saved your new page.
8.  Previewed your page.

**Parent Topic:**[Exploring UI Builder](../concept/create-custom-experience.md)

