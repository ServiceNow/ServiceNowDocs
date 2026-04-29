---
title: Create custom controllers \(Advanced feature\)
description: Build custom controllers to use across experiences. Easily connect reusable data, scripts, and events to your page and set up inputs, outputs, and events.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create custom controllers \(Advanced feature\)

Build custom controllers to use across experiences. Easily connect reusable data, scripts, and events to your page and set up inputs, outputs, and events.

## Before you begin

Role required: ui\_builder\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select **Create**.

3.  Select **Controller**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to track your controller internally.|
    |Description|Short description to help find your controller. Write a description that helps page builders understand what content is included in the controller.|

5.  Select **Create**.

    The controller building window opens.

    ![Controller building window with no data added.](../image/controller-builder-window.png)

6.  Add data resources.

    1.  Select **+ Add data resource**.

    2.  Select a data resource from the list.

    3.  Select **Add**.

    4.  Configure the data resource.

    5.  Select **Save**.

7.  Add an external controller dependencies.

    1.  Select **+ Add external controller dependency**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify your external controller dependency.|
        |Label|Label to help find your external controller dependency.|
        |Controller|Select a controller for your external controller dependency.|

    3.  Select **Save**.

8.  Add client state parameters.

    1.  Select **Client sate parameters**.

    2.  Select **+ Add**.

    3.  Enter a unique name for the client state parameter.

    4.  Select the type from the dropdown.

    5.  Enter an initial value in the field.

    6.  Select **Save**.

    For more information about client state parameters, see [Client state parameters](../concept/client-state-parameters.md).

9.  Add client scripts.

    1.  Select the **+** icon next to **Client scripts**.

    2.  Write your script to perform an action.

    3.  Add a **Script include** or **Associated components**, which shows up in the `imports` parameter of your client script function.

    4.  Select **Apply**.

    5.  Select **Save**.


## What to do next

Use the custom controller you just created by [adding the controller to a page.](../concept/controllers.md#)

**Parent Topic:**[Dynamically expose data in UI Builder pages \(advanced feature\)](../concept/data-resources.md)

