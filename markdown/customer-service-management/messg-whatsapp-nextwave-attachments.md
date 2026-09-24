---
title: Handle media attachments in WhatsApp on NextWave
description: Send and receive images, documents, and video links between agents and customers through the WhatsApp channel on the NextWave off-Glide architecture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/messg-whatsapp-nextwave-attachments.html
release: brazil
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [WhatsApp, attachments, media, NextWave]
breadcrumb: [WhatsApp on NextWave, Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Handle media attachments in WhatsApp on NextWave

Send and receive images, documents, and video links between agents and customers through the WhatsApp channel on the NextWave off-Glide architecture.

## Before you begin

Role required: **sn\_customerservice\_agent**

The WhatsApp Direct Integration channel must be configured and active.

## About this task

The WhatsApp channel on NextWave supports the following attachment types between agents and customers:

-   Images
-   Documents
-   Video links

Attachment upload, transmission, and rendering operate through the NextWave off-Glide pipeline with functional parity to the Glide-based implementation. Attachment metadata and interaction history are preserved.

## Procedure

1.  Open the WhatsApp interaction in the CRM Workspace.

2.  To send an attachment, select the attachment control in the message input area and choose a file.

    Supported file types and size limits are governed by WhatsApp Cloud API constraints. Files that exceed these constraints are rejected with a message to the sender.

3.  To view an inbound attachment, select the media item in the conversation thread.

    Inbound attachments from customers are attached to the interaction record and are retrievable by the agent. Attachment metadata \(file name, type, size\) is captured automatically.


## Result

Media attachments are exchanged between ServiceNow and WhatsApp through the NextWave off-Glide pipeline. Attachment metadata and interaction history remain intact.

