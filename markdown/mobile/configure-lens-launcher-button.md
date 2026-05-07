---
title: Configure a Lens launcher button
description: Add a ServiceNow AI Lens button to input form screens to enable users to quickly extract data from attachments and complete forms faster.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Now Assist, Now Assist for Mobile, Mobile Platform]
---

# Configure a Lens launcher button

Add a ServiceNow AI Lens button to input form screens to enable users to quickly extract data from attachments and complete forms faster.

## Before you begin

Role required: admin

**Note:**

ServiceNow AI Lens is currently not supported in ALP / Quick Actions and is only supported on input form screens that use the screen presentation style.

If any Inputs in an input form screen have the **DisableAILensAutoFill** attribute set to true, the input won’t be updated.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the input form screen on which you want to configure the launcher button, or select **New** to create an input form screen.

    See [Configure an input form screen](../task/parameter-screen-config.md) for instructions on how to create an input form screen.

4.  Under the **Presentation style** category, set the style to **Screen** to allow the addition of function instances.

5.  Select **New** under the function instance option that corresponds to where you want the button to appear, then complete the fields in the **Function instance** form.

<table><thead><tr><th align="left" id="d109368e144">

Option

</th><th align="left" id="d109368e147">

Steps

</th></tr></thead><tbody><tr><td id="d109368e153">

**__Top icon function instances__**

</td><td>

Creates a button in the top header. -   **Name** — Enter a name for the function instance.
-   **Display label** — Enter a display label. This is the label that is visible to end users.
-   **Icon** — Select an icon. This field is required for this option.
-   **Function** — Select **New** to display the function form.


</td></tr><tr><td id="d109368e189">

**__Top menu function instances__**

</td><td>

Creates a button under the three-dot menu in the top header. -   **Name** — Enter a name for the function instance.
-   **Display label** — Enter a display label.
-   **Icon** — Select an icon \(optional\).
-   **Function** — Select **New** to display the function form.


</td></tr></tbody>
</table>6.  Select a **Name** for your function.

7.  Select **Lens launcher** from the **Type** field.

8.  In the **Data** field, select the table relating to what the input form is representing.

9.  Select **Save**.


## Result

A lens launcher button now appears in the location you selected — either in the top header or under the three-dot menu. When a user taps the button, Lens opens in the context of the table you configured, allowing users to interact with the associated data directly from the mobile interface.

-   **[Add optional prompts to the ServiceNow AI Lens Launcher](add-optional-prompts.md)**  
Add optional prompts to the ServiceNow AI Lens launcher button.
-   **[Enable attachment IDs for write-back actions](making-attachment-ids-available-for-write-back-actions.md)**  
Enable write-back actions to use attachment IDs in your ServiceNow AI Lens launcher button.
-   **[Configure Lens launcher using scripted screen](config-lens-launcher-scripted-screen.md)**  
Configure a ServiceNow AI Lens launcher button with scripted screen.

**Parent Topic:**[Configuring Now Assist for Mobile](configuring-now-assist-mobile.md)

