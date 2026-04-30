---
title: Customize citation message
description: Inline citations are intended to show from which ServiceNow knowledge articles the response is generated. This can include information from attachments and knowledge blocks, or from external content such as Microsoft SharePoint and Confluence. Inline citations also appear when the user is presented with an action to perform, for example, within a Virtual Agent topic or a catalog item.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-26"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Customize citation message

Inline citations are intended to show from which ServiceNow knowledge articles the response is generated. This can include information from attachments and knowledge blocks, or from external content such as Microsoft SharePoint and Confluence. Inline citations also appear when the user is presented with an action to perform, for example, within a Virtual Agent topic or a catalog item.

## Before you begin

For more information about Now Assist in Virtual Agent citations, see [Using Now Assist in Virtual Agent](../concept/using-now-assist-in-va.md).

Role required: admin

## Procedure

1.  To change the citation text within the **Sources** section of an LLM-generated message before auto-executing the first step in the action, navigate to **All** &gt; **sys\_cs\_context\_profile.list**.

2.  Select an assistant.

3.  In the **Custom Greetings and Setup Messages** tab, select **Starting "\{0\}"** to modify the LLM-generated message in the citation.

    ![Customize the LLM-generated message in the citation.](../image/NAinVA-context-profile-list.png "Customize the LLM-generated message in the citation")

4.  Select **Update**.


