---
title: Create modeless dialogs in UI Builder
description: Use modeless dialogs on a UI Builder page to add a floating window that enables you to interact with both the window content and the page content below.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create modeless dialogs in UI Builder

Use modeless dialogs on a UI Builder page to add a floating window that enables you to interact with both the window content and the page content below.

The Modeless Dialog component is a floating window containing components and content that appears over a UI Builder page. You can do actions in the modeless dialog while still viewing and interacting with the page below. Multiple modeless dialog windows can be added to a single page. Modeless dialogs can be resized, moved to a new position on a page, and minimized.

Modeless dialogs are different than modals, which pop up but block interaction with the page until the modal is closed. Modeless dialogs are also different than popovers, which close after you click outside the popover.

Common modeless dialog use cases include creating a record, composing an email, using chat, adding work notes or comments, reading help information, or adding/viewing attachments in the modeless dialog.

## Anatomy of a modeless dialog

A modeless dialog consists of three parts:

-   When you add a modeless dialog to a page, the header includes a preconfigured minimize icon, expand icon, and close icon. Other actions can be configured if needed, for example, configure an action in a button to open the modeless dialog in a new tab.
-   Add any component from the UI Builder toolbox, for example, Email composer, Attachments, or Agent chat, into the body. You can apply layouts and configure the component as if you were adding the component to a page.
-   If needed, provide additional buttons or content in the footer at the bottom of the modeless dialog.

![New modeless dialog with header, body, footer section identified with text.](../image/modeless-dialog-anatomy.png)

-   **[Add modeless dialog to a UI Builder page](../task/add-modeless-dialog.md)**  
Learn how to add a modeless dialog in UI Builder. A modeless dialog is a floating window containing content above a page.
-   **[Add modeless dialog event to a UI Builder page](../task/add-modeless-dialog-event.md)**  
Learn how to add and configure a modeless dialog event, such as open, close, or minimize in UI Builder. A modeless dialog is a floating window containing content above a page.

**Parent Topic:**[Customize UI Builder pages using components](work-components.md)

