---
title: Enable voice input for ServiceNow Otto panel
description: Give users the option to use their voice when interacting with the ServiceNow Otto panel to make the panel more accessible. Voice input enables you to use the panel without needing to use a keyboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-voice-input-for-now-assist-panel.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring AI skills, AI Admin Hub, Enable AI experiences]
---

# Enable voice input for ServiceNow Otto panel

Give users the option to use their voice when interacting with the ServiceNow Otto panel to make the panel more accessible. Voice input enables you to use the panel without needing to use a keyboard.

## Before you begin

**Note:** Voice input is automatically activated when the ServiceNow Otto panel is activated. As of the Zurich Patch 4 release, voice input is configured in [Enable additional chat features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/additional-chat-features.md) and not with this option.

You must have installed at least one ServiceNow Otto application with a skill that uses the ServiceNow Otto panel. See [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md) for more information about supported skills.

Role required: sn\_generative\_ai.nsa\_admin

## About this task

You can give users the option to use voice input in the ServiceNow Otto panel. This feature provides an additional input method to interact with ServiceNow Otto skills in English. Once it’s enabled, users can choose to activate this feature in their personal accessibility preferences by toggling on **Enable voice input for the ServiceNow Otto panel**. See [Configure Next Experience accessibility preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-accessibility-preferences.md) for more information about setting personal accessibility preferences.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, and mobile users on the go, such as field service agents.

The voice input feature is not supported in regulated markets.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Otto Admin** &gt; **ServiceNow Otto Experiences**.

    If you’re already in the AI Admin Hub console, navigate to the ServiceNow Otto Experiences page.

2.  Go to the ServiceNow Otto panel tab.

3.  In the Settings section, turn on the toggle for **Voice Input**.


## Result

Users can choose whether they can use their voice to interact with the ServiceNow Otto panel in their Next Experience accessibility preferences.

**Parent Topic:**[Configuring AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-na-landing.md)

