---
title: IT Service Management AI agent collection Notify users with Twilio agentic workflow
description: Use the Twilio SMS text AI agent to help streamline communication processes and enhance workflow efficiency.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [ITSM, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Notify users with Twilio agentic workflow

Use the Twilio SMS text AI agent to help streamline communication processes and enhance workflow efficiency.

## Notify users with Twilio overview

Using the Notify users with Twilio agentic workflow, send text messages via SMS to recipients manually to help improve the time required for subject matter expert response.

To modify the Notify users with Twilio agentic workflow, duplicate it, and adjust the settings according to your requirements.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Notify users with Twilio agentic workflow

Send messages from a Twilio number to a recipient's phone number.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Twilio texting**.

**Important:** To enable the display of the Notify users with Twilio agentic workflow, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see Twilio Spoke.

## AI agents used in the Notify users with Twilio agentic workflow

The Twilio SMS text AI agent is used to generate text using the Notify users with Twilio agentic workflow.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

**Note:** The itil role is added by default. You can change the role for the agent. If you change the role, you must also change the role in the following two flow action ACLs:

-   sn\_itsm\_aia.look\_up\_incoming\_phone\_numbers
-   sn\_itsm\_aia.send\_sms



In the ServiceNow AI Agent Studio, the human agent gets notified as soon as a text message is generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

**Related topics**  


[bundle-platcap.t_ConfigureNotifyWithTwilio]

