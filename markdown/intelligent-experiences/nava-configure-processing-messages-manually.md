---
title: Configure processing messages
description: Configure processing messages to control the status updates that appear in the chat interface while Now Assist works on a request. You can customize the text of processing messages to better reflect your organization's terminology or the specific actions your AI agents perform.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist Admin features, Now Assist, Enable AI experiences]
---

# Configure processing messages

Configure processing messages to control the status updates that appear in the chat interface while Now Assist works on a request. You can customize the text of processing messages to better reflect your organization's terminology or the specific actions your AI agents perform.

## Before you begin

Role required: admin

## Procedure

1.  In the filter navigator field, enter `sys_properties.list`.

2.  In the selection fields, select **Name** from the drop-down list and enter `processing_messages` in the Search field.

3.  Configure these properties:

    -   sn\_aia.og\_ao.enable\_processing\_messages - Enable or disable processing messages.
    -   glide.ui.processing\_message.collapse - Controls collapsing of processing messages.

**Parent Topic:**[Configuring Now Assist Admin features](../../now-assist-admin/concept/configuring-na-landing.md)

