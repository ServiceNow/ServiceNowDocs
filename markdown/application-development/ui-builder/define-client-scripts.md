---
title: Define and bind client scripts to components
description: Add and edit client scripts in UI Builder so that you can update the client state through events. You can bind these scripts to any component by using an event handler.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Define and bind client scripts to components

Add and edit client scripts in UI Builder so that you can update the client state through events. You can bind these scripts to any component by using an event handler.

## Before you begin

Role required: ui\_builder\_admin

## About this task

You can create JavaScript client scripts in UI Builder by using the Now Code editor. Then, you can add the client script as an [event handler](../concept/ui-builder-glossary.md#) to update the client state, emit a handled event of your page, or execute a [data resource](../concept/ui-builder-glossary.md#) operation. For example, you could write a script to increment a date or counter, and bind the script to a component event, like a button click. For more information about the Now Code Editor, see [Edit code with the Now Code Editor \(advanced feature\)](../../now-code-editor/concept/now-code-editor.md).

With these scripts, you can do the following actions:

-   Get available data, manipulate the data, and store it in the client state.
-   Access data resource results.
-   Execute data resource operations.
-   Dispatch events.

## Procedure

1.  Navigate to **All** &gt; **Now experience framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).

3.  Open or create a page.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md).

4.  If you do not have any components on your page, add a component to your page.

    For example, you can add a Heading component. For more information, see [Add and configure components](add-components.md#).

5.  Select **+** next to **Client scripts**.

    ![Arrow pointing to the client scripts button in the side bar.](../image/client-scripts-open-shelf.png)

6.  Name your script.

    A descriptive name helps you know what the script does. It also makes it easier to find the script later when you add it to an event handler. The following example shows a simple date client script.

7.  Write your script to perform an action.

    For example, you could write a simple date script that you bind to a component. ![Example script of a client script.](../image/client-scripts-date-example.png)

8.  Add a **Script include** or **Associated components**, which shows up in the `imports` parameter of your client script function.

9.  Select the component on your page that you want to bind the script to and then select **Events**.

10. Select **+Add a new event handler**, select the script that you created under **Scripts**, and then select **Add**.

    The following example shows a date client script.

    ![Scripts listed in add event handler screen.](../image/client-scripts-date-event.png)

11. Select **Save**.

12. To preview your scripted component, select ![Preview button that opens the page variant.](../image/preview-button.png).


**Parent Topic:**[Dynamically expose data in UI Builder pages \(advanced feature\)](../concept/data-resources.md)

