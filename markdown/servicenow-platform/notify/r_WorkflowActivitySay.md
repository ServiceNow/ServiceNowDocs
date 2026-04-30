---
title: Say workflow activity
description: The say workflow activity allows you to play a message, using text to speech, on a Notify call.
locale: en-US
release: yokohama
product: Notify
classification: notify
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Notify workflow activities, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Say workflow activity

The **say** workflow activity allows you to play a message, using text to speech, on a Notify call.

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|Text to say|Specify the text to read.|
|Language|Select the language and locale to use when reading text.|
|Advanced|Select this check box to use a script to define the language and message, instead of using the **Text to say** and **Language** values.|
|Script|Define a script to set what text is read on the call. The script must return a string that defines the language and the text to read. For example, to play an English-language message, return \{language: 'en-US', text: 'Text to read'\}.|

**Parent Topic:**[Notify workflow activities](../concept/c_NotifyActivities.md)

