---
title: Add modeless dialog to a UI Builder page
description: Learn how to add a modeless dialog in UI Builder. A modeless dialog is a floating window containing content above a page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/add-modeless-dialog.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Create modeless dialogs in UI Builder, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add modeless dialog to a UI Builder page

Learn how to add a modeless dialog in UI Builder. A modeless dialog is a floating window containing content above a page.

## Before you begin

Role required: ui\_builder\_admin

The following steps walk you through the process of configuring a button to open a modeless dialog containing the Attachments component.

**Note:** The procedure outlined here is just one example of how to use modeless dialogs. There are infinite possibilities. Add and configure modeless dialogs to meet your business needs.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Open or create a page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/create-page.md).

4.  In the content tree, move your mouse to **Modeless dialogs**, select the + icon, and select the **Modeless dialog** component.

    \[Omitted image "modeless-dialog-create.png"\] Alt text: Modeless dialogs option shown in content tree with the + icon selected and window containing the Modeless dialog component opened.

5.  If the modeless dialog doesn't appear on the stage automatically, select the new modeless dialog named **Modeless dialog default** in the content tree.

6.  In the configuration panel **Configure** tab, view the presets that were added automatically with the modeless dialog, for example, the width, height, position, and enable drag setting.

    \[Omitted image "modeless-dialog-presets.png"\] Alt text: Modeless dialog configuration panel with Configure tab showing presets.

    All of these preset properties can be edited, if necessary.

    **Note:** For more information about Modeless Dialogs advanced properties, see the [ServiceNow Developer site](https://developer.servicenow.com/dev.do#!/reference/next-experience/vancouver/now-components/now-modeless-dialog/overview).

7.  In the data resources drawer, the **Modeless dialog** controller was added automatically.

    \[Omitted image "modeless-dialog-controller.png"\] Alt text: Black arrow pointing to the Modeless dialog controller in the data resources drawer.

8.  In the content tree, select **+ Add content** under **Modeless dialog default &gt; actions** to add content to the modeless dialog header.

9.  Search for and select the **Stylized text** component.

10. In the **Stylized text** configuration panel, select **None** to configure the component manually.

    \[Omitted image "modeless-dialog-header-config.png"\] Alt text: Stylized text configuration panel with black arrowing pointing to the None option.

    If the **Record subheading** preset was automatically added, select the drop-down arrow, select **None**, and select **Remove** on the **Configure** tab.

    \[Omitted image "modeless-dialog-preset-remove.png"\] Alt text: Stylized text component configuration panel with black arrows pointing to the preset drop down and the None option.

11. If not open already, select **Configure** to open the configure tab.

12. In **Text**, remove the sample text and type `Add Attachments`.

    \[Omitted image "modeless-dialog-header-text.png"\] Alt text: Stylized text configure tab with black arrow pointing to text field.

13. Select **Save** in the UI Builder header.

14. In the content tree, select **+ Add content** under **Modeless dialog default &gt; content &gt; Container** to add content to the modeless dialog body.

15. Select the **Attachments** component.

16. In the **Attachments** configuration panel, if not selected already, select **Record attachments** and **Apply** to configure the component with a preset.

    \[Omitted image "modeless-dialog-component-preset.png"\] Alt text: Attachments component configuration panel with black arrow pointing to Record attachments preset option.

    For more information about configuring the Attachments component, see the [ServiceNow Developer site](https://developer.servicenow.com/dev.do#!/reference/next-experience/vancouver/shared-components/now-record-common-attachments-connected/overview).

17. You could add content to the modeless dialog footer, but in this example leave the footer empty.

18. Select **Save**.

    Notice in the content tree that the modeless dialog and all of its components are listed above the **Body** of your page structure. Also, the **Minimized dialogs dropdown** component is added to the page automatically \(and is listed under the **Body** in the content tree\) to provide the functionality for the minimize icon in the modeless dialog header.

    \[Omitted image "modeless-dialog-content-tree.png"\] Alt text: Content tree with black arrows pointing to the modeless dialog default component, the body, and the minimized dialogs drop down component.

19. In the content tree, select **Body**.

20. Add a button component and configure it to open the modeless dialog.

    1.  In the content tree, select the **Menu** icon next to **Body** and select **Add content**.

    2.  On the **Layouts** tab, select **Single column**.

        A new column layout containing a single column is added to the bottom of the page.

    3.  On the stage, select the + icon in the new column layout.

        \[Omitted image "modeless-dialog-add-button.png"\] Alt text: Single-column layout with a black arrow pointing to the + icon in the column.

    4.  Search for and select the **Button bare** component.

        \[Omitted image "modeless-dialog-button-bare.png"\] Alt text: Toolbox displayed with black arrow pointing to search field containing the term button and another black arrow pointing to the Button bare component.

    5.  In the configuration panel, on the **Configure** tab, select **None** to configure the component manually.

    6.  Select the **Events** tab in the configuration panel.

    7.  Select **+ Add event handler**.

        \[Omitted image "modeless-dialog-event-handler.png"\] Alt text: Button bare configure panel shown with one black arrow pointing to events tab and a second black arrow pointing to the + Add event handler option.

    8.  In the list at left, select **Open Modeless dialog** \(you may need to scroll down in the list\).

    9.  Type `Attachments` in **Minimized Heading**.

    10. Select **Modeless dialog default** in **Modeless dialog**.

        There are other options that can be configured here, including a heading and a category.

    11. Select **Add**.

        \[Omitted image "modeless-dialog-add-event.png"\] Alt text: Event handler window with black arrows pointing to the Open Modeless Dialog option, the minimized heading field, the modeless dialog field, and the add button.

    12. Select the **Configure** tab.

    13. Type `Add Attachments` in **Label**.

        \[Omitted image "modeless-dialog-button-label.png"\] Alt text: Button bare component configure tab with black arrow pointing to the label field.

21. Select **Save**.

22. Select the drop-down arrow next to **Preview** in the UI Builder header and select **Open URL path** in the list.

23. Select the **Add Attachments** button to test the modeless dialog.

    The modeless dialog opens above the main page with the heading at the top and the Attachments component below.

24. To test the minimize functionality, select the minimize icon on the modeless dialog.

    \[Omitted image "modeless-dialog-minimized-heading.png"\] Alt text: Modeless dialog heading with black arrow pointing to the minimize icon.

    The modeless dialog is minimized and can be accessed from the Minimized dialogs drop down.

25. Select the minimized dialogs icon and then select **Attachments** to open the modeless dialog window again.

    \[Omitted image "modeless-dialog-minimized-component.png"\] Alt text: Minimized dialogs component selected with the drop down showing the draft email option.


**Parent Topic:**[Create modeless dialogs in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/uib-modeless-dialog.md)

