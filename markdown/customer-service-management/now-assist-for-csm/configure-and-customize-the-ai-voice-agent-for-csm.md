---
title: Configure and customize the AI Voice Agent for Now Assist for CSM
description: Configure the AI Voice Agent to let callers check case status, create cases, and update existing cases through voice interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/configure-and-customize-the-ai-voice-agent-for-csm.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-06-03"
reading_time_minutes: 3
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [AI voice agent, Use agentic AI in CSM, Now Assist for CSM, Customer Service Management]
---

# Configure and customize the AI Voice Agent for Now Assist for CSM

Configure the AI Voice Agent to let callers check case status, create cases, and update existing cases through voice interactions.

## Before you begin

Verify the following prerequisites are in place before you begin:

-   Now Assist for CSM is activated on your instance.
-   A supported CCaaS integration is configured. Supported providers are Genesys, Twilio, NICE, Five9, 3CLogic, and Amazon Connect.
-   The platform-level AI Voice Agent plugin is auto-installed. No separate installation is required.
-   Your instance is on Zurich Patch 4 or Yokohama Patch 11 at minimum.

The AI Voice Agent for Now Assist for CSM includes the following default agents:

-   Case Status AI Voice Agent — retrieves live case state, priority, assigned group, product, and latest work notes.
-   Create Case AI Voice Agent — collects issue description and creates a new CSM case in real time.
-   Update Case AI Voice Agent — updates an existing case after identifying the case, collecting the fields to update, and validating the changes.

**Note:** The default agents are starting points and must be cloned and grounded with your organization's specific instructions before deploying to production.

Role required: admin

## Procedure

1.  Configure the Voice Assistant in Assistant Designer.

    The Voice Assistant connects your telephony channel to the AI Platform.

    1.  Navigate to **Conversational Interfaces** &gt; **Assistant Designer** to create a voice agent.

    2.  Select your CCaaS provider and enter the integration credentials from your CCaaS account.

    3.  Under **Security Settings**, define your authentication method.

        Use PIN \(SoftPin\) for B2C deployments it validates the caller's PIN against the User table on the AI Platform via the phone keypad. The caller enters their PIN via the phone keypad, which is validated against the User table on the AI Platform. Alternative methods include SMS Code, Knowledge Factors, OTP, and Okta Push Notification.

    4.  Set the voice assistant name, greeting language, and voice personality.

        Supported languages include English, German, Spanish, French, French Canadian, Brazilian Portuguese, Dutch, Italian, Korean, and Mandarin.

2.  Duplicate and ground the default CSM Voice Agent in AI Agent Studio.

    1.  Navigate to **AI Agent Studio** &gt; **Create and Manage** &gt; **AI Agent** and locate the agents under the CSM Voice Agent collection.

    2.  Select the three-dot menu for each agent and select **Duplicate**.

        Cloning creates a copy you can configure without modifying the default baseline.

    3.  Ground the cloned agent by updating the agent instructions, record operation tools, and any business-specific context.

        Update the following:

        -   Agent instructions to reflect your company's policies, terminology, and expected caller interactions.
        -   Record operation tools scoped to the correct tables and fields relevant to your case data.
        -   Business-specific context the LLM needs to generate accurate, on-brand responses.
    4.  Add tools to the cloned agent as needed.

        Available tools include:

        -   RAG Search tool — retrieves relevant knowledge articles during the call. Scope this to two to three knowledge bases most relevant to your voice channel to maintain low response latency.
        -   Subflows or script tools — trigger additional workflows on case creation or update.
        -   MCP Server tool — connects to external agentic systems if needed.
3.  Map the cloned Voice Agent to the Voice Assistant.

    1.  Return to Assistant Designer and add the duplicated agent to your Voice Assistant configuration.

    2.  Configure fallback behavior for scenarios where the AI does not return a result or a call exceeds the 10-minute limit.

        Available fallback options:

        -   Transfer to live agent — the caller is transferred with a transcript summary and detected intent pre-populated in the agent workspace.
        -   Generate a case via Record Producer — automatically creates the appropriate record type such as a case type, if no live agents are available.
4.  Test the Voice Agent using a live call to the configured phone number.

    Use the following resources to validate and review call outcomes in AI Agent Studio:

    -   Interactions table — full transcript logged per call as soon as the call ends.
    -   Execution Plans table — step-by-step tool invocation log for debugging unexpected agent behavior.
    -   Analytics dashboard — accessible from the Analytics tab in Assistant Designer. Tracks total voice conversations, deflection rates, conversation outcomes, and satisfaction scores.

## Result

The AI Voice Agent is configured and ready to handle customer voice interactions for case status inquiries, case creation, and case updates. Customers can check open case statuses, submit case updates, and create cases through guided voice interactions without requiring a live agent.

## What to do next

Monitor the Analytics dashboard weekly during early production to review deflection rates, conversation outcomes, and CSAT scores. Review Execution Plans regularly to tune agent instructions based on tool invocation patterns.

