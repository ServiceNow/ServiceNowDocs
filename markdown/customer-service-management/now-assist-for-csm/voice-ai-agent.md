---
title: AI voice agent in CSM
description: Use the AI voice agent to create cases and check case status through natural, conversational voice calls.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-02-02"
reading_time_minutes: 2
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use agentic AI in CSM, Now Assist for CSM, Customer Service Management]
---

# AI voice agent in CSM

Use the AI voice agent to create cases and check case status through natural, conversational voice calls.

## AI voice agent overview

The AI voice agent streamlines customer interactions by integrating with contact center platforms including Genesys and Twilio.

The AI voice agent enables customers to get case status and create cases entirely through voice commands. This solution reduces manual intervention, improves service resolution times, and delivers consistent functionality across all supported contact center partners.

## Key Capabilities

The AI voice agent helps with case management by using natural, conversational voice interactions:

-   Check the status of your cases just by asking.
-   Create cases without filling out any forms.
-   If an issue is complicated, the agent can quickly connect you to a human.
-   It supports multiple languages, making it easy for customers around the world to use.
-   All interactions are recorded for auditing and quality checks.
-   Customer data stays safe and separated to protect privacy.

## Benefits

With the AI voice agent, there’s improvement in both customer experience and operational efficiency:

-   Support teams spend less time answering routine questions because the agent handles case status checks and updates.
-   Customers don't need training or knowledge of internal processes—The agent guides them.
-   Customer satisfaction increases because the service is faster, easier, and more intuitive.

## CSM AI voice agent

There are two AI voice agents for CSM. Each agent is associated with a voice service acting as a virtual customer service agent and can be configured with welcome messages, voice profiles, and fallback options like human agent routing or case creation. This setup enables efficient, AI-driven support for customers.

|AI voice agent|Description|
|--------------|-----------|
|Case status|Provides users with comprehensive status updates for cases based on the case number. Designed for users who need quick and reliable access to case details, including state, creation date, assigned agent, latest update, and a summary of the case.|
|Create case|Lets customers log cases using voice input by guiding them through a clear, step‑by‑step conversation that captures and validates required details. It creates the case, and confirms successful submission.|

AI voice agents are managed through AI Agent Studio. To configure a new agent:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**, then select the AI agents tab.
2.  Open the **Add** drop-down list.
3.  Select an AI voice agent to create a voice-enabled agent for case management.

This interface enables admins to [create a AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a-voice-enabled-ai-agent.md), connect to [supported contact center providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrating-voice-service-with-ccaas-providers.md), and deploy fully functional AI voice agents for case management. For deployment and configuration info, see [Deploy AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/deploy-ai-agents-for-voice.md).

**Note:**

-   To enable customer access and use of AI voice agents, an admin must install the plugin Customer Service Management AI agent collection
-   To modify the AI voice agents, duplicate it, and adjust the settings according to your requirements.

**Important:**

-   When you modify an AI agent, or a tool, make sure that you update all instructions accordingly.
-   In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

