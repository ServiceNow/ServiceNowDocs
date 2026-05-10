---
title: Agentic AI in the Virtual Agent application
description: Use AI agents in Virtual Agent to autonomously resolve tasks.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Agentic AI in the Virtual Agent application

Use AI agents in Virtual Agent to autonomously resolve tasks.

## Platform Requester AI agents

View tickets and make updates to them from Now Assist in Virtual Agent, the Now Assist panel, or Microsoft Teams using the Request Status AI agent. For more information, see [Platform Request status AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ticket-status-aia.md).

## ITSM AI agents used in Virtual agent

The **DEMO Password reset agent** is a demo AI agent that provides requesters with password reset instructions for the account that they need help with. The agent guides the users with these instructions from KB articles in their self-service portal. When you install the Now Assist for IT Service Management plugin \(sn\_itsm\_gen\_ai\) along with the demo data, you can use the **DEMO Password reset agent** to provide you with password reset instructions.

**Note:** The agent is shipped inactive by default.

To activate, in the **Select channels and status** screen:

-   Enable the **Allow** button in the **Engage via Virtual Agent assistants** section.
-   In the **Chat assistants** field, select **Now Assist in Virtual Agent \(default\)** to use the AI agent from the Virtual Agent.
-   In the **Activation status** section, enable the **This AI agent is active** button.

![image.now-assist-demo-password-reset-agent1]![image.now-assist-demo-password-reset-agent2]

The DEMO Password reset agent uses the ESC Portal Default Search Profile. ![image.itsm-demo-pw-reset-agent-search-profile]

