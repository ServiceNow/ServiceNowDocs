---
title: Closing idle LINE chat conversations
description: Enable agents to effectively manage their active LINE chat conversations by automatically closing conversations after they have been inactive for a pre-configured amount of time.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Conversational Integration with LINE, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Closing idle LINE chat conversations

Enable agents to effectively manage their active LINE chat conversations by automatically closing conversations after they have been inactive for a pre-configured amount of time.

The Virtual Agent conversations are configured for the LINE messaging app. By default, any conversations abandoned by requesters remain open or idle until they are automatically closed daily by the **Time Out Abandoned VA Conversations** scheduled job. For more information, see [Closing Virtual Agent and Agent Chat conversations](va-open-conversations.md).

As an administrator, you can change the default timeout period for idle Virtual Agent conversations configured for the LINE messaging app by setting the **com.glide.cs.line\_idle\_timeout** system property to the number of seconds that abandoned conversations remain open after the requester's last response. The system property value must be less than the time interval set for the **Time Out Abandoned VA Conversations** scheduled job, set to two hours \(7200 seconds\) by default. Because the **com.glide.cs.line\_idle\_timeout** system property isn't available by default, you must add it with the data type set to integer. For more information, see Add a system property.

