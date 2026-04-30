---
title: Differences between Notify-Twilio and Notify-Twilio Direct
description: Describes the differences between the Notify-Twilio and Notify-Twilio Direct drivers, including architecture, workflows, Twilio support, and task-initiated conference calls.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Differences between Notify-Twilio and Notify-Twilio Direct

Describes the differences between the Notify-Twilio and Notify-Twilio Direct drivers, including architecture, workflows, Twilio support, and task-initiated conference calls.

|Notify-Twilio \(com.snc.notify.twilio\)|Notify-Twilio Direct \(com.snc.notify.twilio\_direct\)|
|---------------------------------------|------------------------------------------------------|
|This plugin is deprecated. Notify - Twilio Direct Driver now replaces this plugin.|Provides next generation integration with Twilio and Notify.|
|Uses Java SDK based integration with Twilio.|It is a JavaScript based driver which uses platform provided outbound REST APIs to connect to Twilio.|
|NA|Adds support for various advanced SMS features such as Co-pilot messaging, Twilio Notify bulk SMS.|
|NA|Adds support for various functionalities in conference calls such as view the participant who is speaking on the conference call, disable beep when someone enters/exits a conference, advanced call features like machine detection and so on.|

**Parent Topic:**[Notify reference](../concept/notify-reference-section.md)

