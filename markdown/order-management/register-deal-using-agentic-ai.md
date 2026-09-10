---
title: Register a deal using agentic AI
description: Use the Deal Registration AI agent to process deal registrations and manage the entire deal registration process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/register-deal-using-agentic-ai.html
release: australia
topic_type: concept
last_updated: "2026-08-21"
reading_time_minutes: 4
keywords: [deal registration, AI agent, PRM, partner, Otto]
breadcrumb: [Partner Relationship Management, Use, Sales Customer Relationship Management]
---

# Register a deal using agentic AI

Use the Deal Registration AI agent to process deal registrations and manage the entire deal registration process.

## Deal Registration AI agent overview

The Deal Registration AI agent works to assist in managing the life cycle of deal registrations, either independently or under supervision. You can use the AI agent to do the following:

-   Capture deal information through natural language intake
-   Validate account and consumer records automatically
-   Process deal details and extract structured information
-   Provide pre-submission summary for review and approval
-   Create deal records upon confirmation
-   Escalate to live agent when needed

To modify the Deal Registration AI agent duplicate it, and adjust the settings according to your requirements. You can activate the AI agent by making triggers active and setting the display settings to include the ServiceNow Otto panel.

**Important:** When you modify an AI agent or tool, make sure that you update all instructions accordingly.

## Prerequisites to use an AI agent

The prerequisites to use an AI agent are as follows:

-   Make sure that the ServiceNow Otto panel is turned on.
-   Set up the work schedule for deal agents:
    -   Navigate to **All** &gt; **Agent schedule** &gt; **Work schedule**.
    -   Create a work schedule for deal agents.
-   Duplicate the AI agent and activate the triggers.

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn't necessary.

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

## To run the AI agent autonomously

To run the AI agent autonomously, you must first duplicate the AI agent, and then proceed with the following steps:

1.  Activate the AI agent.
2.  Activate all components within the AI agent.
3.  Activate the trigger to invoke the AI agent automatically. The triggers for each AI agent must be unique. If you prefer to invoke it manually, activating the trigger is not necessary.

## Deal Registration AI agent use cases

To access the use case:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Use cases**.
2.  Select **Deal Registration**.

## Deal Registration AI agents

The following table lists the Deal Registration AI agents.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

|AI agent|AI agent role|
|--------|-------------|
|Deal intake AI agent|Initiates the deal registration flow. This agent supports deal agents by capturing deal information through natural language and extracting structured data.|
|Deal validation AI agent|Handles validation of account and consumer records, product information, and deal structure. Recommends actions based on validation results.|
|Inbound communication AI agent|Initiates the inbound response handler flow. This agent supports deal agents by retrieving and analyzing the latest communication records. Based on its analysis, it recommends necessary actions required to move forward with the deal.|
|Deal fulfillment AI agent||

## Roles required to create an AI agent

The roles required to activate and access the AI agent are as follows.

|Roles|Responsibilities|
|-----|----------------|
|Deal Registration AI admin|Configure the AI agent. Change AI settings. Create and manage new agents and tools.|
|Deal Registration AI user|Interact with AI using the ServiceNow Otto panel.|
|Workflow Configurator||
|Agent Administrator||

## Registering a deal

To register a deal, perform the following steps:

1.  Navigate to **All** &gt; **AI Agent Studio**.
2.  Review the information in the Describe and connect screen, make the necessary updates to ensure that the use case adapts to your requirements, and then select **Save and Continue**.
3.  In the Define trigger screen, activate the triggers that adapt to your requirements, or create your own triggers, and then select **Save and Continue**.
4.  In the Select display screen, perform the following steps:
    1.  Select where you want the use case output to be displayed.
    2.  Use the arrow next to it to add roles that can access the use case.
    3.  **Note:** The `deal_agent` is the default role for the use case.

5.  Select **Save and test**.

The agent executes the testing in AI Agent Studio for the use case.

In the ServiceNow Otto panel, the agent receives a notification as soon as the interaction is generated, which enables them to follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in Customer Service Management by using the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/request-gen-ai-capabilities-csm-now-assist-panel.md).

**Parent Topic:**[Using Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-partner-relationship-management.md)

