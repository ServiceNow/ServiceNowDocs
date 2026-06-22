---
title: Enable synchronous support in Virtual Agent API
description: You can support synchronous mode for your conversation with primary bot.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/virtual-agent-api-enable-synchronous-support.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-01-22"
reading_time_minutes: 1
breadcrumb: [Use, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Enable synchronous support in Virtual Agent API

You can support synchronous mode for your conversation with primary bot.

## Before you begin

Role required: admin

Confirm to exclude the Bot to Bot channel from Agent Chat.

1.  Navigate to **All**, and then enter `sys_properties.list` in the filter.
2.  Select the **com.glide.cs.exclude.liveagent.support** system property to open it.
3.  Add **Bot To Bot** to the **Value** field.

    \[Omitted image "va-api-exclude-liveagent-btb.png"\] Alt text: The Value field for the system property contains "Alexa,Google Assistant,Bot to Bot." These channels are excluded from supporting Agent Chat.

4.  Select **Update**.

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_channel.list` in the navigation filter.

2.  Select the Bot to Bot record.

3.  Clear the **Enable Notifications** check box to disable it.

4.  Clear the **Support typing indicator** check box to disable it.

5.  Select the **Synchronous** check box.

    \[Omitted image "va-api-synchronous-mode.png"\] Alt text: Bot to Bot channel configuration for Synchronous mode shows Enable Notifications and Support typing indicator boxes as unselected. The Synchronous box is selected.

    **Note:** If the **Synchronous** field is not visible, you can [configure the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/configure-form-layout.md) to show it.

6.  Select **Update**.


**Parent Topic:**[Using Virtual Agent API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/use-virtual-agent-api.md)

