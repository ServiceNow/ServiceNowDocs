---
title: Add modal to component
description: Learn how to add a modal in UI Builder. A modal is a window that appears when you click a component. For example, a modal might display when a delete button component is clicked, prompting the user to confirm deleting a record.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Create modals in UI Builder, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add modal to component

Learn how to add a modal in UI Builder. A modal is a window that appears when you click a component. For example, a modal might display when a delete button component is clicked, prompting the user to confirm deleting a record.

## Before you begin

Role required: ui\_builder\_admin

## About this task

A modal is a screen that appears when an event handler is triggered by an event such as a button being clicked. The following procedure shows an example of how to add a Confirm modal and an associated event handler to a button component.

## Procedure

1.  Navigate to **All** &gt; **Now experience framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Open or create a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md).

4.  Add a modal to the page.

    1.  Select the **+** icon in the content tree next to **Modals and popovers**.

        ![Arrow pointing to + next to Modals and popovers line item in content tree.](../image/add-modal-selection.png)

    2.  Choose a modal type such as **Confirm**.

        ![Modal options, with Confirm modal highlighted.](../image/add-modal-options.png)

        |Modal type|Description|
        |----------|-----------|
        |Alert|An Alert modal provides information relating to the component action. For example, when a user presses a delete button, you could have an alert pop-up that lets the user know they cannot undo a delete action.|
        |Confirm|A Confirm modal asks a user to confirm the component action. For example, when a user presses a delete button, the user would have to confirm the deletion of data. You can choose the confirm options from the primary and secondary button label fields, such as Yes/Cancel.|
        |Confirm and destroy|A Confirm and destroy modal is more directive, usually relating to deleting or erasing content. It lets the user know the seriousness of an action, and asks them whether they want to proceed with the action.|
        |Custom|The Custom modal uses layouts to let you fully design what information you want in the modal. Layouts also decide where the information sits within the modal screen. You can use Cascading Style Sheets \(CSS\) styling to change the visual look of the modal, such as background color.|
        |iframe|Use iframe to bring content into your modal using existing iframe content from a URL and data.|
        |Modal viewport|Dynamically pass content into your viewport modal through an event binding using a client script. See [Bind an event to a component](bind-event-component.md) for more information on binding an event to a component.|

    3.  Configure the modals as shown in the table.

        Configure each modal differently, depending on what the modal requires. Change what information goes into the modal, the size of the modal, and how it looks. You can add an event handler to the modal that performs the action for the modal, such as opening or closing the modal.

<table id="table_cgy_k23_wnb"><thead><tr><th>

Modal

</th><th>

Configuration

</th></tr></thead><tbody><tr><td>

Alert![Alert modal configure options tab.](../image/modal-alert-config.png)

</td><td>

-   Add a header, which is the title of the modal.
-   Write the content that you want displayed in the modal. The content tells the user what the alert is.
-   Add text for the button label. It can be anything you want, such as **OK**, **Yes**, and so on.
-   Choose the size of the modal on the screen. Select **Small**, **Medium**, **Large**, or **Fullscreen**.
-   Enable or disable **Prevent Default Button Action**, depending on whether you want the modal to close based on the default action.
-   Enable or disable **Defer modal content loading**. If you disable it, the modal loads with the page. If you enable it, the modal doesn't load when the page loads.
-   Select **Events** &gt; **Add event mapping** to add an event handler to the modal.
-   Select an event handler to apply to the modal, then select **Add** to add it to the page. Choose from inherited or page-level event handlers. Event handlers perform an action such as open or close a modal. Depending on the modal type, you can refresh data for the App Shell data source, the user session for GraphQL, or a user session for Transform.


</td></tr><tr><td>

Confirm![Confirm modal configure options tab.](../image/modal-confirm-config.png)

</td><td>

-   Add a header, which is the title of the modal.
-   Write the content that you want displayed in the modal. The content tells the user what the alert is.
-   Add text for the primary button. The primary button is the main action button for users, such as **Yes**, **Add**, and so on.
-   Add text for the secondary button. The secondary button is usually the no choice for users, such as **Cancel**, **No**, and so on.
-   Choose the size of the modal on the screen. Select **Small**, **Medium**, **Large**, or **Fullscreen**.
-   Enable or disable **Prevent Default Primary Button Action**, depending on whether you want the modal to close based on the default action.
-   Enable or disable **Prevent Default Secondary Button Action**, depending on whether you want the modal to close based on the default action.
-   Enable or disable **Defer modal content loading**. If you disable it, the modal loads with the page. If you enable it, the modal doesn't load when the page loads.
-   Select **Events** &gt; **Add event mapping** to add an event handler to the modal.
-   Select an event handler to apply to the modal. Choose from inherited or page-level event handlers. Event handlers perform an action such as open or close a modal. Depending on the modal type, you can refresh data for the App Shell data source, the user session for GraphQL, or a user session for Transform.

![Image shows the event handler options for a modal.](../image/modal-event-handler.png)

</td></tr><tr><td>

Confirm or destroy![Confirm and destroy modal configure options tab.](../image/modal-confirm-destroy-config.png)

</td><td>

-   Add a header, which is the title of the modal.
-   Write the content that you want displayed in the modal. The content tells the user what the alert is.
-   Add text for the primary button. Primary is the main action button for users, such as **Delete** or **Erase**.
-   Add text for the secondary button. The secondary button is usually the no choice for users, such as **Cancel**, **No**, and so on.
-   Choose the size of the modal on the screen. Select **Small**, **Medium**, **Large**, or **Fullscreen**.
-   Enable or disable **Prevent Default Primary Button Action**, depending on whether you want the modal to close based on the default action.
-   Enable or disable **Prevent Default Secondary Button Action**, depending on whether you want the modal to close based on the default action.
-   Enable or disable **Defer modal content loading**. If you disable it, the modal loads with the page. If you enable it, the modal doesn't load when the page loads.
-   Select **Events** &gt; **Add event mapping** to add an event handler to the modal.
-   Select an event handler to apply to the modal. Choose from inherited or page-level event handlers. Event handlers perform an action such as open or close a modal. Depending on the modal type, you can refresh data for the App Shell data source, the user session for GraphQL, or a user session for Transform.

![Event handler options for a modal.](../image/modal-event-handler.png)

</td></tr><tr><td>

Custom![Custom modal configure options tab.](../image/modal-custom-config.png)

</td><td>

-   Choose a layout for your modal. You can use a flexbox or CSS grid layout. These layouts let you add content in your modal however you want.
-   Use styling options to change how your modal looks. You can apply any standard CSS styling to your modal, such as background color and padding. For more information about styling, see [Change the default appearance of components](add-styling-to-component.md#).
-   Add components to the containers within the custom modal.
-   Select **Events** &gt; **Add event mapping** to add an event handler to the modal.
-   Select an event handler to apply to the modal. Choose from inherited or page-level event handlers. Event handlers perform an action such as open or close a modal. Depending on the modal type, you can refresh data for the App Shell data source, the user session for GraphQL, or a user session for Transform.

![Image shows the event handler options for a modal.](../image/modal-event-handler.png)

</td></tr><tr><td>

iframe![Iframe modal configure options tab.](../image/modal-iframe-config.png)

</td><td>

-   Add a header, which is the title of the modal.
-   Add a source URL that points to your existing iframe content.
-   Set the parameters and initial data that you want to iframe.
-   Choose the size of the modal on the screen. Select **Small**, **Medium**, **Large**, or **Fullscreen**.
-   Turn on **disable sandbox** to lift the following restrictions: allow-forms, allow-modals, allow-popups, allow-presentation, allow-same-origin, allow-scripts, and allow-downloads options. Turn off the **disable sandbox** to only lift the allow-scripts option.
-   Enable or disable **Defer modal content loading**. If you disable it, the modal loads with the page. If you enable it, the modal doesn't load when the page loads.
-   Select **Events** &gt; **Add event mapping** to add an event handler to the modal.
-   Select an event handler to apply to the modal. Choose from inherited or page-level event handlers. Event handlers perform an action such as open or close a modal. Depending on the modal type, you can refresh data for the App Shell data source, the user session for GraphQL, or a user session for Transform.

![Image shows the event handler options for a modal.](../image/modal-event-handler.png)

</td></tr><tr><td>

Modal viewport![Modal viewport modal configure options tab.](../image/modal-modal-viewport-config.png)

</td><td>

-   Choose the size of the modal on the screen. Select **Small**, **Medium**, **Large**, or **Fullscreen**.
-   Enable or disable **Hide Padding**.
-   Enable or disable **Hide Close Button**. If you enable it, the close button does not display in the modal.
-   Enable or disable **Defer modal content loading**. If you disable it, the modal loads with the page. If you enable it, the modal doesn't load when the page loads.
-   Select **Events** &gt; **Add event mapping** to add an event handler to the modal.
-   Select an event handler to apply to the modal. Choose from inherited or page-level event handlers. Event handlers perform an action such as open or close a modal. Depending on the modal type, you can refresh data for the App Shell data source, the user session for GraphQL, or a user session for Transform.

![Image shows the event handler options for a modal.](../image/modal-event-handler.png)

-   Select the viewport component within the modal viewport.

![Arrow pointing to a viewport in the content tree.](../image/uib-modal-viewport-content-tree.png)

-   Select **+ Add** in the Configure tab to add a page collection to the viewport.
-   Select a page collection from the list and click **Add**.


</td></tr></tbody>
</table>5.  Add a component to your page to trigger the modal you just added, such as a button component.

    See [Add and configure components](add-components.md#) for more information.

6.  Select the **Events** tab in the configuration panel.

7.  Select **+ Add event handler**.

    ![Arrow pointing to the add event handler option for the button component.](../image/modal-button-event.png)

8.  Select **Open or close modal dialog**.

9.  Select the modal you created in the previous steps using the **Modal** drop-down.

10. Click **Add**.

    ![Event handler configuration screen showing the open or close modal dialog settings.](../image/modal-open-button-event.png)

11. When you finish configuring the modal, close it.

    Notice in the content tree that the modals you create sit above the body of your page structure.

    ![Content tree with modals listed.](../image/modal-content-tree.png)

12. Click **Save**.


**Parent Topic:**[Create modals in UI Builder](../concept/Modals-overview.md)

