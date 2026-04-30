---
title: Create modals in UI Builder
description: Use modals in UI Builder with components to provide alerts or calls to action for a user. UI Builder comes with modals to save time and effort.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create modals in UI Builder

Use modals in UI Builder with components to provide alerts or calls to action for a user. UI Builder comes with modals to save time and effort.

## What Modals are

Modals, also known as dialogs, are windows that overlay another content window. Modals take control of the user experience. Users cannot interact with the overlaid window until the modal is closed. Modals can contain different types of content such as:

-   Static text
-   Dynamic text
-   Forms
-   Images
-   Buttons

UI Builder has preconfigured modals available. You can add a modal to your component. Then, configure the content of the modal, and how it displays on the screen. Add an event handler to the modal to perform an action when a user selects it. The action can alert a user about something, or ask a user to confirm an action. A modal is a way to ensure that a user knows what is happening. For example, a modal may ask a user to confirm a selection before continuing whatever action they are performing on the main page.

## Modal Anatomy

Modals in UI Builder can have:

-   Modal header
-   Modal content
-   Close dialog button \(no action taken by the modal\)
-   At least one Modal button \(action can be taken by the modal\)

![Diagram showing the different parts of modals.](../image/modal-anatomy-graphic.png)

## Modal types

Different types of modals are available in UI Builder, as shown in the following table.

|Modal type|Description|
|----------|-----------|
|Alert|An Alert modal provides information relating to the component action. For example, when a user presses a delete button, you could have an alert pop-up that lets the user know they cannot undo a delete action.|
|Confirm|A Confirm modal asks a user to confirm the component action. For example, when a user presses a delete button, the user would have to confirm the deletion of data. You can choose the confirm options from the primary and secondary button label fields, such as Yes/Cancel.|
|Confirm and destroy|A Confirm and destroy modal is more directive, usually relating to deleting or erasing content. It lets the user know the seriousness of an action, and asks them whether they want to proceed with the action.|
|Custom|Custom modals address scenarios that are not handled using the standard modals. Custom modals can be thought of as a container component on a modal. You can add a custom layout, components, events, and data resources just like you do on a page. The custom modal uses layouts to let you fully design what information you want in the modal. Layouts also decide where the information sits within the modal screen. You can use Cascading Style Sheets \(CSS\) styling to change the visual look of the modal.|
|iframe|Use iframe to bring content into your modal from existing iframe content from a URL and data.|
|Modal viewport|Dynamically pass content into your viewport modal through an event binding using a client script.|

## Event handlers and modals

Expose events to modals to handle call-to-action events. For example, a primary action, secondary action, and so on. You configure the data by adding an event handler and invoking a data resource. It is as simple as adding a new event handler for the component that has a modal. Or you can add an event handler to the modal itself. You select the event that you want associated with the component or modal and add it. See [Add modal to component](../task/modals-uib.md) for detailed instructions.

-   **[Add modal to component](../task/modals-uib.md)**  
Learn how to add a modal in UI Builder. A modal is a window that appears when you click a component. For example, a modal might display when a delete button component is clicked, prompting the user to confirm deleting a record.

**Parent Topic:**[Customize UI Builder pages using components](work-components.md)

