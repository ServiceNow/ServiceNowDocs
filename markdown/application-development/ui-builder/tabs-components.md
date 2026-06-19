---
title: Add tabbed content to UI Builder pages
description: Use the Tabs component to add tabbed content to pages in UI Builder.Use an empty container tab to manually create a static set of tabs on your page.Use the Tabs component to create a set of repeater tabs by linking tabs to a data array.Create a set of tabs on a page by linking to a related list.Use page collection tabs to recreate the same tabs across multiple pages in UI Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/tabs-components.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add tabbed content to UI Builder pages

Use the Tabs component to add tabbed content to pages in UI Builder.

Create additional navigation on your UI Builder page by adding a Tabs component to your page. Use the Tabs component to nest components within tabs on your page. Tabs can be configured as either horizontal tabs at the top of the content, or as vertical tabs on the left or right side of the content.

Tabs can be organized in the configuration panel to reorder how they are displayed on the UI Builder page. Add custom labels and icons to tabs to provide unique visual identifiers for navigating across tabs. These changes can be viewed in real-time as you edit the Tabs component.

You can add one of the following types of tabs to your UI Builder page:

-   Empty container tab
-   [Repeater](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/ui-builder-glossary.md) tab
-   Related list tab
-   Page collection tabs

The tabs component supports any combination of static tabs, repeated tabs, related list tabs, and page collection tabs. Alternatively, you can still use the Viewport tab mode to add a series of viewports.

**Parent Topic:**[Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-components.md)

## Add empty container tabs

Use an empty container tab to manually create a static set of tabs on your page.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/create-page.md).

4.  Select the **+ Add content** button on the stage to open the toolbox.

    \[Omitted image "open-toolbox-on-stage.png"\] Alt text: Arrow pointing to the + icon that opens the toolbox.

5.  Select a **Single column** layout.

6.  Next, select the **+** icon in the column to open the toolbox.

7.  Add a **Tabs** component to your page.

    \[Omitted image "tabs-toolbox-options.png"\] Alt text: Arrow pointing to tabs component in the toolbox.

    For more information on how to add a component to a page, see [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-components.md).

8.  Select **+ Add tab** on the stage.

    \[Omitted image "tabs-add-tab.png"\] Alt text: Arrow pointing to the tabs + add option in the configuration panel.

9.  Select **Start from an empty container**.

    \[Omitted image "tabs-select-empty.png"\] Alt text: Start from an empty container option selected.

10. Select **Next**.

11. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Tab label|Label for the tab to display on your page.|
    |Icon|Icon to appear next to the tab label. Icons are not required.|
    |Hide tab|Whether to hide or display the tab.|

12. Select **Create**.

    The new tab displays in the **Tabs** component.

13. Select the new tab.

14. Select **+** icon.

    \[Omitted image "tabs-add-component-in-tab.png"\] Alt text: Arrow pointing to the + icon to add a component to the demo tab.

15. Select the component that you want to add to the tab.

    Components display under the tab in which they’re nested in the content tree. For more information, see [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-components.md).


### Result

Your page shows the two tabs that you created. Select each tab to further configure them, add styling, or add an event handler. For more information on styling, see [Change the default appearance of components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-styling-to-component.md). For more information on adding an event handler, see [Manage actions in UI Builder pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-events.md).

## Add repeater tabs

Use the Tabs component to create a set of repeater tabs by linking tabs to a data array.

### Before you begin

Role required: admin

### About this task

You can use [repeater](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/ui-builder-glossary.md) tabs to create multiple tabs based on the data array you provide. You can pass the icon, label, count, and fields as a key in the object. Use the label key to add names to tabs. Use the field key to pass information to repeater tabs. You can bind a data broker, client state, or a client script to the data array provider to return the array of objects with the correct schema.

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/create-page.md).

4.  Select the **+ Add content** button on the stage to open the toolbox.

    \[Omitted image "open-toolbox-on-stage.png"\] Alt text: Arrow pointing to the + on the stage that opens the toolbox.

5.  Select a **Single column** layout.

6.  Next, select the **+** icon in the column to open the toolbox.

7.  Add a **Tabs** component to your page.

    \[Omitted image "tabs-toolbox-options.png"\] Alt text: Arrow pointing to the tabs component in the toolbox.

    For more information on how to add a component to a page, see [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-components.md).

8.  Select **+ Add tab** on the stage.

    \[Omitted image "tabs-add-tab.png"\] Alt text: Arrow pointing to + Add option in the configuration panel.

9.  Select **Use a repeater**.

    \[Omitted image "tabs-select-repeater.png"\] Alt text: Use a repeater selected in the tab selection modal.

10. Select **Next**.

11. Enter a label for the repeater tab in the **Placeholder tab label** field.

    This label is assigned to the first repeater tab and is the only tab displayed in the page preview.

12. Select **Edit** in the **Data array** field.

    \[Omitted image "tabs-edit-repeater.gif"\] Alt text: Open the data array editing modal.

13. Configure the data array in the JSON editor.

    |Key|Data type|Description|
    |---|---------|-----------|
    |icon|String|Name of the icon that appears in UI Builder.|
    |label|String|Required. Display name of the tab in UI Builder.|
    |count|Number|Value to provide on the tab label. Dynamically bind to a data broker or a client script that will be displayed on the label.|
    |fields|Object|Object that can be used to store information and to pass down to the components in the tabs.|

14. Select **Apply**.

    The data array field displays the data array configuration.

    \[Omitted image "tabs-repeater-settings.png"\] Alt text: Repeater settings with a custom data array.

15. Select **Create**.

    The new repeater tab appears on the page and in the content tree.

    \[Omitted image "tabs-repeater-placeholder.png"\] Alt text: Placeholder repeater tab highlighted on the page.

16. Select **Save**.

17. Add components to the repeater tab.

18. Select \[Omitted image "preview-button.png"\] Alt text: Preview button that opens your page in runtime, which is a preview of how the page looks on a web page. to verify that the repeater tabs display correctly on your page.


## Add related list tabs

Create a set of tabs on a page by linking to a related list.

### Before you begin

Role required: admin

### About this task

The related list tab automatically populates tabs based on the record that your page is displaying. For example, by default the related lists for the user table are Roles, Groups, Delegates, and Visibility domains. If your page is displaying a user record, then creating a related list tab adds all four of these related lists as tabs on your page. You can preview the page to see the related lists that were added. A record controller is required to create related list tabs. To add a controller to your page, see [Bind data to UI Builder pages using controllers \(advanced feature\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/controllers.md) for more information.

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/create-page.md).

4.  Select the **+ Add content** button on the stage to open the toolbox.

    \[Omitted image "open-toolbox-on-stage.png"\] Alt text: Arrow pointing to the + Add content button that opens the toolbox.

5.  Select a **Single column** layout.

6.  Next, select the **+** icon in the column to open the toolbox.

7.  Add a **Tabs** component to your page.

    \[Omitted image "tabs-toolbox-options.png"\] Alt text: Arrow pointing to tabs component in the toolbox.

    For more information on how to add a component to a page, see [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-components.md).

8.  Select **+ Add tab** on the stage.

    \[Omitted image "tabs-add-tab.png"\] Alt text: Add tabs to the tab component.

9.  Select **Display related lists for a record**.

    \[Omitted image "tabs-select-related-list.png"\] Alt text: Display related list for a record selected.

10. Select **Next**.

11. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Placeholder tab label|Placeholder label to appear on the preview tab of your page.|
    |Hide tab|Whether you want to hide or display the tab.|
    |Record Controller|Record controller with the related list.|

12. Select **Create**.

    The new related list tab displays in the **Tabs** section of the configuration panel. Only one placeholder tab appears in the page preview. The green icon next to the related list tab in the content tree shows how many tabs appear on your page.

    \[Omitted image "uib-tabs-related-icon.png"\] Alt text: Icon showing how many related list tabs display on your page.

13. Select **Save**.

14. View and test your page by selecting \[Omitted image "preview-button.png"\] Alt text: Preview button that opens your page in runtime, which is a preview of how the page looks on a web page..


## Add page collection tabs

Use page collection tabs to recreate the same tabs across multiple pages in UI Builder.

### Before you begin

Role required: admin

### About this task

A page collection is a group of prebuilt globally available pages. Use page collection tabs to render each page in a page collection as a tab. You can select an existing page collection or can create your own. A controller is required to add a page collection. For more information about page collections, see [Page collections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/page-collections.md).

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/create-page.md).

4.  Select the **+ Add content** button on the stage to open the toolbox.

    \[Omitted image "open-toolbox-on-stage.png"\] Alt text: Arrow pointing to the + on the stage that opens the toolbox.

5.  Select a **Single column** layout.

6.  Next, select the **+** icon in the column to open the toolbox.

7.  Add a **Tabs** component to your page.

    \[Omitted image "tabs-toolbox-options.png"\] Alt text: Arrow pointing to the tabs component in the toolbox.

    For more information on how to add a component to a page, see [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-components.md).

8.  Select **+ Add tab** on the stage.

    \[Omitted image "tabs-add-tab.png"\] Alt text: Arrow pointing to + Add option in the configuration panel.

9.  Select **Add a page collection**.

    \[Omitted image "tabs-select-page-collection.png"\] Alt text: Tab selection modal with add a page collection option highlighted.

10. Select **Next**.

11. Select a page collection from the list or create a collection by selecting **+ Create collection**.

    To create your own page collection, see [Create a page collection across multiple UI pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/create-page-collection.md).

    \[Omitted image "page-collection-list.png"\] Alt text: Page collection selection screen with option to create a collection.

12. Select **Add**.

    The new page collection tab displays in the **Tabs** section of the configuration panel. Only one placeholder tab displays in the page preview.

    \[Omitted image "tabs-page-collection-placeholder-tab.png"\] Alt text: Page collection tab highlighted on the page.

13. Select **Save**.

14. View and test your page by selecting \[Omitted image "preview-button.png"\] Alt text: Preview button that opens the page variant..


