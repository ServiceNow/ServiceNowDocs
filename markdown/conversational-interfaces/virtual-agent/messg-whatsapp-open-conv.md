---
title: Closing idle WhatsApp chat conversations
description: Enable agents to effectively manage their active WhatsApp chat conversations by automatically closing idle conversations after they have been inactive for a pre-configured amount of time.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Conversational Integration with WhatsApp \(powered by Twilio\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Closing idle WhatsApp chat conversations

Enable agents to effectively manage their active WhatsApp chat conversations by automatically closing idle conversations after they have been inactive for a pre-configured amount of time.

The Virtual Agent conversations are configured for the WhatsApp messaging app. By default, any conversations abandoned by requesters remain open or idle until they are automatically closed daily by the **Time Out Abandoned VA Conversations** scheduled job. For more information, see [Closing Virtual Agent and Agent Chat conversations](va-open-conversations.md).

As an administrator, you can change the default timeout period for idle Virtual Agent conversations configured for the WhatsApp messaging app by setting the **com.glide.cs.whatsapp\_idle\_timeout** system property to the number of seconds that abandoned conversations remain open after the requester's last response. The system property value must be less than the time interval set for the **Time Out Abandoned VA Conversations** scheduled job, set to two hours \(7200 seconds\) by default. Because the **com.glide.cs.whatsapp\_idle\_timeout** system property isn't available by default, you must add it with the data type set to integer. For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

