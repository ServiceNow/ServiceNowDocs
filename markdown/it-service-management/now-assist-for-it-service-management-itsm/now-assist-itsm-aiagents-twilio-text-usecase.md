---
title: IT Service Management AI agent collection Notify users with Twilio agentic workflow
description: Use the Twilio SMS text AI agent to help streamline communication processes and enhance workflow efficiency.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-twilio-text-usecase.html
release: xanadu
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI]
breadcrumb: [Use agentic workflows in ITSM, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Notify users with Twilio agentic workflow

Use the Twilio SMS text AI agent to help streamline communication processes and enhance workflow efficiency.

## Notify users with Twilio overview

Using the Notify users with Twilio agentic workflow, send text messages via SMS to recipients manually to help improve the time required for subject matter expert response.

**Note:** The Notify users with Twilio agentic workflow doesn’t have a trigger and is invoked manually.

To modify the Notify users with Twilio agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Important:** When you modify a agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Notify users with Twilio agentic workflow

Send messages from a Twilio number to a recipient's phone number.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Twilio texting**.

**Important:** To enable the display of the Notify users with Twilio agentic workflow, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see [Twilio Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/integrate-applications/integration-hub/twilio-spoke.md).

## AI agents used in the Notify users with Twilio agentic workflow

The Twilio SMS text AI agent is used to generate text using the Notify users with Twilio agentic workflow.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

**Note:** The itil role is added by default.

In the ServiceNow AI Agent Studio, the human agent gets notified as soon as a text message is generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/request-gen-ai-capabilities-itsm-now-assist-panel.md).

**Parent Topic:**[Using agentic workflows in Now Assist for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-ai-agents-use-cases.md)

**Related topics**  


[Configure Notify with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/notify/t_ConfigureNotifyWithTwilio.md)

