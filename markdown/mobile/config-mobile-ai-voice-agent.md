---
title: Configure Mobile AI Voice Agent
description: Follow these steps to enable the Mobile AI Voice Agent feature for your mobile app users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist, Now Assist for Mobile, Mobile Platform]
---

# Configure Mobile AI Voice Agent

Follow these steps to enable the Mobile AI Voice Agent feature for your mobile app users.

## Before you begin

Role required: admin

-   Make sure that Now Assist is enabled in the instance. For more information, see [Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
-   Ensure you have the appropriate permissions and licensing for AI voice capabilities, and that you have a Now Assist Voice assistant created in Assistant Designer. For more information, see [Create an AI voice assistant](https://www.servicenow.com/docs/access?context=create-an-ai-voice-service&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_button.list**.

2.  Select the button to which you want to add the Voice Agent or select **New** to create a new one.

3.  Enter a title for your button in the **Name** field.

4.  Set the **Type** to **Voice Launcher** to launch Voice Assistant directly, or **Chat launcher** to launch Voice Assistant from Virtual Agent.

5.  Set **Context** to **Global**.

6.  Right-click and select **Save**.

7.  Navigate to **All** &gt; **sys\_sg\_button\_instance.list**.

8.  Select the record that you want to assign your voice launcher or chat launcher button to, or select **New** to create a new one.

9.  Fill in the **Name**, **Parent table**, and **Label** fields.

10. Under **Function**, select the Voice Agent or Virtual Agent button you chose in step 2.

11. Under **Location**, select where on the page the button will be displayed.

12. Right-click and select **Save**.

13. Navigate to Assistant Designer to assign your voice function instance to a Now Assist voice assistant.

    For steps on how to configure your function with a voice assistant, see [Integrate voice assistant with mobile app launcher](https://www.servicenow.com/docs/access?context=integrate-voice-assistant-with-mobile-app-voice-launcher&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


**Parent Topic:**[Configuring Now Assist for Mobile](configuring-now-assist-mobile.md)

