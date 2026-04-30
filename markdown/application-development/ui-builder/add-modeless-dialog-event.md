---
title: Add modeless dialog event to a UI Builder page
description: Learn how to add and configure a modeless dialog event, such as open, close, or minimize in UI Builder. A modeless dialog is a floating window containing content above a page.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Create modeless dialogs in UI Builder, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add modeless dialog event to a UI Builder page

Learn how to add and configure a modeless dialog event, such as open, close, or minimize in UI Builder. A modeless dialog is a floating window containing content above a page.

## Before you begin

Role required: ui\_builder\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Open or create a page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md).

4.  Add a modeless dialog to the page.

    For more information about how to create a modeless dialog, see [Add modeless dialog to a UI Builder page](add-modeless-dialog.md).

5.  Add a component to the page, such as a button, to take action on the modeless dialog.

    For more information about how to create a button that interacts with a modeless dialog, see [Add modeless dialog to a UI Builder page](add-modeless-dialog.md).

6.  Select the button component in the content tree or on the stage.

7.  In the configuration panel, select the **Events** tab.

8.  Select **+ Add event handler**.

    ![Button bare configure panel shown with one black arrow pointing to events tab and a second black arrow pointing to the + Add event handler option.](../image/modeless-dialog-event-handler.png)

9.  From the Event handler preview window, select an action to assign to the button.

    There are five modeless dialog event handlers available.

    ![Black arrow pointing to the Modeless dialog events listed in the Event handler preview window.](../image/modeless-dialog-event-handler-list.png)

    **Note:** For any of the event handlers, select **Script** in the **Mode** drop-down if you prefer to work in the script editor.

<table id="choicetable_dzv_llh_wnb"><thead><tr><th align="left" id="d46702e211">

To add a modeless dialog event handler

</th><th align="left" id="d46702e214">

Do the following

</th></tr></thead><tbody><tr><td id="d46702e220">

**Open Modeless Dialog**

</td><td>

Opens a modeless dialog. For example, add a button labeled Compose email and configure the button to open a modeless dialog containing the Email composer \(mini\) component.-   **Heading**: Type a heading for the modeless dialog.
-   **Minimized Heading**: Type a heading that is displayed when a user selects the minimized dialogs drop-down icon on the page.
-   **Category**: Type a category name to group the modeless dialog.
-   **Modeless Dialog**: Select the modeless dialog to open.
-   **Single instance**: Select this option to enable users to open only one instance of the modeless dialog. Leave this option unselected to enable users to open multiple instances of the modeless dialog. For example, if the button opens a modeless dialog containing the Email composer \(mini\) component and you don't select the single instance option, users can open multiple modeless dialog windows to compose email messages.
-   **Modeless Dialog Instance ID**: If you select the **Single instance** option, specify the modeless dialog instance ID that should be opened on click. Move your mouse over the field and select the **Bind data** icon. In **Data types** select **Modeless Dialog**. Drag the instanceID pill to the top section and select **Apply**.
-   **When to trigger** \(Advanced option\): Select **Always** to have the component \(in this example, the button\) always open the modeless dialog. Select **Conditionally** to add an event handler condition. For more information about event handler conditions, see [Supported functions in the UI Builder component formula editor](add-components.md#).


</td></tr><tr><td id="d46702e298">

**Close Modeless Dialog**

</td><td>

Closes a modeless dialog. Use this option if you want to configure a component, such as a button, to close the modeless dialog from outside the modeless dialog window.-   **Modeless Dialog Instance ID**: Specify the modeless dialog instance ID that should be closed on click.
-   **When to trigger** \(Advanced option\): Select **Always** to have the component \(in this example, the button\) always close the modeless dialog. Select **Conditionally** to add an event handler condition. For more information about event handler conditions, see [Supported functions in the UI Builder component formula editor](add-components.md#).


</td></tr><tr><td id="d46702e335">

**Minimize Modeless Dialog**

</td><td>

Minimizes an open modeless dialog. Use this option if you want to configure a component, such as a button, to minimize the modeless dialog from outside the modeless dialog window.-   **Modeless Dialog Instance ID**: Specify the modeless dialog instance ID that should be minimized on click.
-   **When to trigger** \(Advanced option\): Select **Always** to have the component \(in this example, the button\) always minimize the modeless dialog. Select **Conditionally** to add an event handler condition. For more information about event handler conditions, see [Supported functions in the UI Builder component formula editor](add-components.md#).


</td></tr><tr><td id="d46702e372">

**Update Modeless Dialog**

</td><td>

Updates the specified fields on a modeless dialog. For example, add a button labeled Update Heading to the footer of a modeless dialog and configure the button to update the heading of the component in the modeless dialog.-   **Heading**: Type new heading text for the modeless dialog that should be added when the button is selected.
-   **Minimized Heading**: Type new minimized heading text that should be added when the button is selected.
-   **Category**: Type a new category name that should be added when the button is selected.
-   **Modeless Dialog**: Select the modeless dialog to update.
-   **Modeless Dialog Instance ID**: Specify the modeless dialog instance ID that should be updated on click.
-   **Is Dirty**: Select this option to mark the modeless dialog as dirty.
-   **When to trigger** \(Advanced option\): Select **Always** to have the component \(in this example, the button\) always update the modeless dialog. Select **Conditionally** to add an event handler condition. For more information about event handler conditions, see [Supported functions in the UI Builder component formula editor](add-components.md#).


</td></tr><tr><td id="d46702e436">

**Dirty Modeless Dialog**

</td><td>

Marks a modeless dialog as dirty.-   In **Modeless Dialog Instance ID**, specify the modeless dialog instance ID to mark as dirty.
-   **When to trigger** \(Advanced option\): Select **Always** to have the component \(in this example, the button\) always marked as dirty. Select **Conditionally** to add an event handler condition. For more information about event handler conditions, see [Supported functions in the UI Builder component formula editor](add-components.md#).


</td></tr></tbody>
</table>10. Select **Add**.


## Result

The configured event handler displays in the configuration panel **Events** tab for the component.

![Black arrow pointing to the open modeless dialog event handler on the configuration panel events tab for the button bare component.](../image/modeless-dialog-event-handler-added.png)

**Parent Topic:**[Create modeless dialogs in UI Builder](../concept/uib-modeless-dialog.md)

