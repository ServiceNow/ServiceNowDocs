---
title: Pre-built setup topics for Virtual Agent
description: Use pre-built setup topics to create a standard welcome greeting and a conversation closing. In addition, setup topics can provide user feedback and surveys, as well as error handling.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Pre-built setup topics for Virtual Agent

Use pre-built setup topics to create a standard welcome greeting and a conversation closing. In addition, setup topics can provide user feedback and surveys, as well as error handling.

For more information about setup topics, see [Setting up chat experiences for Virtual Agent users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-conversation-settings.md).

For a complete list of setup topics that are included with Virtual Agent, see [Working with setup topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/working-setup-topics.md).

## Dynamic Greeting Topic

Users receive a dynamic, time-based greeting at the beginning of a conversation from a virtual agent. The greeting includes addressing the user by first name with the time of day, referencing any incident or request the user may have open, and mentioning outage information if an outage is occurring or planned. For example:

"Good morning, John. You currently have \[x\] incidents and \[x\] requests open. We are aware of \[outage\] with \[service\] that began at \[start time\]".

When the end time is known, the virtual agent includes the message:

"The \[outage\] is planned to end at \[end time\]".

**Note:** If there are no incidents, requests, or outages these messages do not display.

The dynamic greeting is followed by the standard greeting, which asks the user to enter information.

For more information about configuring the greeting setup topic, see [Change the Virtual Agent greeting messages in the Greeting setup topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-welcome-topic-selection-msgs.md).

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](../concept/using-itsm-va.md)

