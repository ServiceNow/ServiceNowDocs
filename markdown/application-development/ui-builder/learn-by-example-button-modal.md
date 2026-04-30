---
title: Create a button that opens a modal
description: After you've created your demo experience and added a blank page, you can edit the page variant as needed. For the sake of this demo, you can create a button and a modal, and configure the button to open the modal.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a record page using a template, Learn UI Builder by example, Learning UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create a button that opens a modal

After you've created your demo experience and added a blank page, you can edit the page variant as needed. For the sake of this demo, you can create a button and a modal, and configure the button to open the modal.

## Before you begin

Role required: ui\_builder\_admin

## Procedure

1.  Open the UI Builder page for your demo experience.

    ![UI Builder visual editor.](../image/visual-editor.png "UI Builder visual editor")

2.  Click the **+ Add content** button on the stage to open the toolbox.

3.  Select a **Single column** layout.

4.  Next, click the **+** icon in the column to open the toolbox.

5.  Select the **Button** component to add it to the stage.

    ![Components tab with arrow pointing to Button component.](../image/add-button.png "Add a button")

    **Note:** When you have selected the component, the Page configuration pane includes some presets you can use to automatically configure components on compatible pages. For the sake of this exercise, however, you will be configuring the component manually. For more information on presets, see [Customize UI Builder pages using components](../concept/work-components.md).

6.  Select **Add**.

7.  In the Page configuration pane, select **Configure the component manually**.

8.  In the Page content pane, select **Button 1** and, in the Configuration pane, change the button label to **Open modal**.

9.  Select **Save**.

10. In the Page content pane, click the plus icon next to **Modals** and select an **Alert** modal.

    ![Modals panel with Alert modal selected.](../image/new-modal.png "Add an Alert modal")

11. Select **Save**.

12. In the Page contents pane, select **Button 1** and, in the Configuration pane, select the **Events** tab.

13. Select **+ Add event handler** and, under **Inherited event handlers**, select **Open or close modal dialog**.

    ![Show/hide modal configuration.](../image/show-hide-modal.png "Show/hide modal configuration")

14. Activate the **Open modal dialog** and, select **Alert 1** in the **Modal** field, and select **Add**.

15. Select **Save**.

16. Select **Preview**.

17. When the preview opens, select **Open modal**.

    The modal you defined opens.

    ![Open modal with button.](../image/open-modal-with-button.png "Open modal with button")

18. Select **Got it** in the modal, and then select the browser back button to return to the experience main screen.


## What to do next

Select the **Next topic** link to learn how to create a page using a template.

**Parent Topic:**[Create a record page using a template](learn-by-example-create-page-with-template.md)

