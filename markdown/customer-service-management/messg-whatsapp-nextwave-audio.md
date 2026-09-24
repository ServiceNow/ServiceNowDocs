---
title: Use audio features in WhatsApp on NextWave
description: Play back customer voice messages and record agent voice messages in WhatsApp conversations on the NextWave off-Glide architecture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/messg-whatsapp-nextwave-audio.html
release: brazil
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [WhatsApp, audio, voice message, NextWave]
breadcrumb: [WhatsApp on NextWave, Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Use audio features in WhatsApp on NextWave

Play back customer voice messages and record agent voice messages in WhatsApp conversations on the NextWave off-Glide architecture.

## Before you begin

Role required: **sn\_customerservice\_agent**

## About this task

Customers can record and send audio messages through WhatsApp, and agents can play them back in the CRM Workspace on NextWave. Agents can also record and send voice messages to customers where the channel supports it.

Audio file format, size, and duration constraints are governed by the WhatsApp Cloud API specifications.

## Procedure

1.  Play back a customer voice message
2.  Open the WhatsApp interaction in the CRM Workspace.

3.  Locate the audio message in the conversation thread and use the playback controls \(play, pause, seek\) to listen.

    Audio messages are stored as a link in the interaction's conversation history attachment. Failed audio uploads or playback errors display an appropriate message.

4.  Record and send a voice message
5.  Select the voice recording control in the message input area.

    The recording UI provides start, stop, and cancel controls with recording-in-progress feedback.

6.  Record your message and send it to the customer.

    The voice message is delivered in a format supported by WhatsApp. If the recording fails or cannot be uploaded, an agent-facing message describes the error.


## Result

Audio messages are exchanged between agents and customers through the NextWave off-Glide pipeline. Audio files are stored as part of the interaction's conversation history.

