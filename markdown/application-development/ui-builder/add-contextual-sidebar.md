---
title: Add a contextual sidebar
description: Add a contextual sidebar to a page with UI Builder to display related content using a vertical tab structure.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add a contextual sidebar

Add a contextual sidebar to a page with UI Builder to display related content using a vertical tab structure.

## Before you begin

Role required: ui\_builder\_admin

## About this task

You can configure the contextual sidebar in the same way you would configure a tab component. Each vertical tab in the contextual sidebar renders custom content. You can place components in each tab for quick access directly from the page.

For example, a document creation page might have the attachments component on one tab, enabling you to attach files related to the document that you're working on. On another tab, there could be a nested comments component, enabling you to add and view comments related to the document.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md). For information about creating a page variant, see [Create a page variant](create-variant.md)

4.  On the stage, open the toolbox by selecting the **+ Add content** button.

5.  Select the **Single column** layout tile.

6.  In the column, open the toolbox by selecting the **+** icon.

7.  Select the **Contextual sidebar** component to add it to your page.

    ![UI Builder editor with the toolbox open, showing a black arrow pointing to the contextual sidebar component.](../image/uib-acs-toolbox.png)

    The contextual sidebar appears on the stage, and the Tabs section appears in the configuration panel.

8.  In the configuration panel under the Tabs section, select the settings icon \(![Settings icon.](../image/uib-acs-settings-icon.png)\) to configure the tab.

    1.  On the form, fill in the fields.

<table id="table_usy_s1c_wtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tab label

</td><td>

Label that displays on the tab for your page.

</td></tr><tr><td>

Icon

</td><td>

Icon that appears next to the tab label. **Note:** Icons aren't required.

</td></tr><tr><td>

Hide tab

</td><td>

Option to hide or display the tab.

</td></tr></tbody>
</table>    2.  Select **Save**.

9.  On the stage in the contextual sidebar, open the toolbox by selecting the **+** icon.

10. Select the component that you want to add to the tab.

    The component displays under the tab in the content tree. For more information, see [Add and configure components](add-components.md#).

11. To add another tab, select **+ Add** under the Tabs section.


## What to do next

For detailed information about the configuration of the contextual sidebar and its properties, see [Tabs UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/now-tabs/uib-setup) on the ServiceNow Developer Site.

**Parent Topic:**[Customize UI Builder pages using components](../concept/work-components.md)

