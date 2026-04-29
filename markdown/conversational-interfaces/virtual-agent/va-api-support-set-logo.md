---
title: Setting logo for the primary bot in Virtual Agent API
description: You can customize your agent chat interface by setting a logo for the primary bot that appears in the chat history.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure to support chat history, Use, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Setting logo for the primary bot in Virtual Agent API

You can customize your agent chat interface by setting a logo for the primary bot that appears in the chat history.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `live_profile.list` in the filter.

2.  Select **New**.

3.  On the Live Profile New Record form, fill in the fields.

<table id="table_esq_ylr_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the live profile, such as `bot logo`.

</td></tr><tr><td>

Type

</td><td>

Type of the live profile. Enter `Other`.

</td></tr><tr><td>

Document

</td><td>

Table associated with the live profile.1.  Select the Search icon ![Search icon.](../images/icon-search.png).
2.  In the Select the document dialog box, specify the following information:
    -   **Table name**: Select **Provider Channel Identity \[sys\_cs\_provider\_application\]**.
    -   **Document**: Select the provider application for your bot. Select `VA Bot to Bot Provider Application`.
3.  Select **OK**.


</td></tr><tr><td>

Photo

</td><td>

Image \(logo\) for the bot profile.

</td></tr><tr><td>

Short description

</td><td>

Text that describes the live profile.

</td></tr></tbody>
</table>4.  Click **Update**.


**Parent Topic:**[Configure to support chat history in Virtual Agent API](va-api-support-chat-history.md)

