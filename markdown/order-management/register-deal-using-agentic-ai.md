---
title: Register a deal using agentic AI
description: The Deal Registration Agent assists users in submitting deal registrations and perform specific actions, such as updating fields, managing products, and retrieving deal details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/register-deal-using-agentic-ai.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [deal registration, AI agent, PRM, partner, Otto]
breadcrumb: [Partner Relationship Management, Use, Sales Customer Relationship Management]
---

# Register a deal using agentic AI

The **Deal Registration Agent** assists users in submitting deal registrations and perform specific actions, such as updating fields, managing products, and retrieving deal details.

## Deal Registration Agent overview

The Deal Registration AI agent is an assistant that enables you to manage the creation, update, and submission of deal registrations, including management of their product line items. Invoke this agent to create, draft, update, or submit a deal registration, or to add, remove, or verify products on an existing one. It resolves user-named products against the product catalog and adds them as deal registration line items. Using natural language, the AI agent gathers deal information, validates records, and automates submission through an integrated approval process. You can use the Deal Registration AI agent to do the following:

-   Create, draft, submit a new deal registration \(for a business account or an individual consumer\)
-   Add products to a deal registration
-   Remove a product from a deal registration
-   Verify whether a specific product is already on a deal registration
-   Update a field on a deal registration
-   Show or retrieve deal registration details

To modify the Deal Registration Agent, duplicate it and adjust the settings for your requirements. You can activate the AI agent by making triggers active and setting the display settings to include the ServiceNow Otto panel.

For information about how to create and register a deal, see [Deal Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/deal-registration-management.md).

**Note:** When you modify an AI agent or tool, verify that you update all instructions.

## Prerequisites for using the Deal Registration Agent

Before using the Deal Registration AI agent, complete the following prerequisites:

-   Confirm that the ServiceNow Otto panel is turned on.
-   Duplicate the AI agent and activate the triggers.

**Note:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md) and then complete the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger is not necessary.

    There might be AI agents installed on your instance that aren't used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/find-ai-agents.md).


## Deal Registration Workflow

To access the Deal Registration workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Workflows**.
2.  Review the information in the Define the specialty screen, make any necessary updates, and then select **Save and Continue**.
3.  In the Add trigger screen, activate the triggers for your requirements or create your own triggers, and then select **Save and Continue**.
4.  Select **Deal Registration**.

The AI agent executes the testing in AI Agent Studio for the workflow.

In the ServiceNow Otto panel, the agent receives a notification when the interaction is generated. The agent can then follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in Customer Service Management by using the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/request-gen-ai-capabilities-csm-now-assist-panel.md).

## Deal Registration AI agent

The following table lists the Deal Registration AI agents.

|AI agent|AI agent role|
|--------|-------------|
|Deal Registration Agent|Helps to create, draft, update, or submit a deal registration, or to add, remove, or verify products on an existing one.|

**Note:** In the Define availability screen for the AI agent, confirm that the **Status** field is enabled to activate the AI agent.

## Roles that can access Deal Registration AI agent

The following roles can access the Deal Registration AI agent:

|Role|User Type|Access Point|
|----|---------|------------|
|Enterprise Deal Registration Relationship Manager|Internal|Now Assist Panel|
|Enterprise Deal Registration Relationship Contributor|Internal|Platform workspace|
|Enterprise B2B Deal Registration Agent|Internal|Platform workspace|
|Enterprise B2C Deal Registration Agent|Internal|Platform workspace|
|Enterprise Deal Registration Agent|Internal|Platform workspace|
|Partner B2B Deal Registration Initiator|External|Partner portal|
|Partner B2C Deal Registration Initiator|External|Partner portal|
|Partner B2B Sales Representative|External|Partner portal|
|Partner B2C Sales Representative|External|Partner portal|

## Deal registration with the Now Assist panel

To register a deal, use the Now Assist panel to start the Deal Registration workflow.

1.  Navigate to **Workspaces** &gt; **CRM Workspace**.
2.  Launch the ServiceNow Otto chat panel by selecting the ServiceNow Otto icon \[Omitted image "icon-otto-outline-24.svg"\] Alt text:.
3.  Type your query in natural language, for example, `Create a deal`.

    The invoice dispute assist agentic workflow invokes the invoice dispute support assistant AI agent.

    The Deal Registration workflow invokes the Deal Registration agent.

    \[Omitted image "deal-reg-workflow.png"\] Alt text: Deal Registration workflow

4.  When prompted, provide the required details, such as the channel partner name and account.

    After you provide the required details, the agent validates the information.

5.  Review the confirmed details. If any information is incorrect, update it when the agent prompts you.

    The deal is created, and the deal registration number is displayed.

    \[Omitted image "deal-reg-workflow2.png"\] Alt text: Deal registration workflow-deal created


**Parent Topic:**[Using Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-partner-relationship-management.md)

**Related topics**  


[Using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/now-assist-csm-using.md)

