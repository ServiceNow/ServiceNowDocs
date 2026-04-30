---
title: Customize the Connect audio notification sound
description: You can replace the default Connect audio notification sound with an audio file of your choice.
locale: en-US
release: zurich
product: Connect
classification: connect
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Connect administration, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Customize the Connect audio notification sound

You can replace the default Connect audio notification sound with an audio file of your choice.

## Before you begin

Role required: admin

[Upload the audio file](https://www.servicenow.com/docs/access?context=t_UploadAnAudioFile&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) you want to use as the notification sound.

Role required: admin

## About this task

The audio notification sound is used for all Connect conversation types, including Connect Support conversations.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Audio Files**.

2.  Locate the audio file you want to use as the notification sound and copy the **Name** value.

3.  Navigate to **Connect** &gt; **Administration** &gt; **Properties**.

4.  Locate the property called **Audio file to play to notify users of new messages, support conversation transfers and @mentions in Connect** \(**connect.notification.audio\_alert**\) and replace the default value with the name of the audio file.

5.  Click **Save**.


## Result

End users receive audio notifications when sending and receiving support chats. Support agents only receive audio notifications for inbound chats when the chat window is not in focus.

