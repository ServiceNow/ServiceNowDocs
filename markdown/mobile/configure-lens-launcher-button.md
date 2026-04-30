---
title: Configure Lens launcher button
description: Add a ServiceNow AI Lens button to input form screens to allow users to quickly extract data from attachments and complete forms faster.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-12-02"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist, Now Assist for Mobile, Mobile Platform]
---

# Configure Lens launcher button

Add a ServiceNow AI Lens button to input form screens to allow users to quickly extract data from attachments and complete forms faster.

## Before you begin

Role required: admin

**Note:** ServiceNow AI Lens is currently not supported in ALP / Quick Actions and is only supported on input form screens that use the screen presentation style.

**Note:** If any Inputs in an input form screen have the **DisableAILensAutoFill** attribute set to true, the input won’t be updated.

## Procedure

1.  Navigate to **All** &gt; **__sys\_sg\_parameter\_screen.list__**.

2.  Select the input form screen on which you want to configure the launcher button.

3.  In the **Settings** tab, locate the **Presentation style** field and set it to **Screen** to allow the addition of function instances.

4.  Select the input form screen on which you want to configure the launcher button.

5.  Navigate to the **Settings** tab.

6.  Locate the **Presentation style** field and set it to **Screen** to allow the addition of function instances.

    **Note:** When **Presentation style** is **Screen**, only one button instance can be configured on an input form screen, positioned either at the **Top** or **Top icon** location. Currently, the buttons are limited to the write-back type.

7.  Navigate to the **Function instances belonging to Screen** tab.

8.  Select the **New** button to create a new button function \(**sys\_sg\_button\_instance**\).

9.  Set the function’s type to **Lens Launcher**.

10. Select **Submit** to save your button.


-   **[Add optional prompts to the ServiceNow AI Lens Launcher](add-optional-prompts.md)**  
Add optional prompts to the ServiceNow AI Lens launcher button.
-   **[Enable attachment IDs for write-back actions](making-attachment-ids-available-for-write-back-actions.md)**  
Enable write-back actions to use attachment IDs in your ServiceNow AI Lens launcher button.
-   **[Configure Lens launcher using scripted screen](config-lens-launcher-scripted-screen.md)**  
Configure a ServiceNow AI Lens launcher button with scripted screen.

**Parent Topic:**[Configuring Now Assist for Mobile](configuring-now-assist-mobile.md)

