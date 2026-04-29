---
title: Integrate voice assistant with mobile app launcher
description: Configure your voice assistant to be accessible through the voice launcher functions in mobile app.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-01-20"
reading_time_minutes: 1
breadcrumb: [Deploy AI voice agents, Now Assist AI agents, Enable AI experiences]
---

# Integrate voice assistant with mobile app launcher

Configure your voice assistant to be accessible through the voice launcher functions in mobile app.

## Before you begin

Role required: virtual\_agent\_admin or admin

-   You must have a voice assistant created in Assistant Designer
-   Mobile app voice launcher function must be configured using Now Assist for Mobile before you can assign it to an assistant. See [Configure Mobile AI Voice Agent](https://www.servicenow.com/docs/access?context=config-mobile-ai-voice-agent&version=australia&pubname=australia-mobile&ft:locale=en-US) for more information.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Assistants**.

2.  Find the voice assistant that you want to connect to a mobile app voice launcher and select **Edit**.

3.  Select **Communication channels** in the Settings tab and select **Mobile channels** tab.

    ![Voice launcher function selection in mobile channel configuration](../image/voice-agents-voice-launcher-function-configuration.png "Voice launcher function setup")

4.  In Voice launcher functions, select from the **Add voice launcher function** drop-down to add a voice launcher function to open the assistant in voice mode.

5.  In Chat launcher functions, select from the **Add chat launcher function** drop-down to add a chat launcher function to open the assistant in chat mode.

6.  In Prominent action button override, select from the **Add tab override** drop-down to allow a prominent action button to launch the assistant.

    The prominent action button overrides what’s been defined in the chat launcher and voice launcher functions. See  for more information on configuring the prominent action button.

7.  Select **Save** to save the configuration.


