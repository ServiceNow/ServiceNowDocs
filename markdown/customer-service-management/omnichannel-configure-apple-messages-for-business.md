---
title: Configure Apple Messages for Business
description: Apple Messages for Business integration enables customers to start secure conversations from the Messages app on Apple devices. Agents manage these interactions in CSM Workspace with full customer context, case details, and conversation history.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/omnichannel-configure-apple-messages-for-business.html
release: australia
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 3
keywords: [Apple Messages for Business, omnichannel, CSM Workspace, conversational integration, messaging channel]
breadcrumb: [Configure consumer messaging apps, Configure omnichannel, Configure, Customer Service Management]
---

# Configure Apple Messages for Business

Apple Messages for Business integration enables customers to start secure conversations from the Messages app on Apple devices. Agents manage these interactions in CSM Workspace with full customer context, case details, and conversation history.

Customers expect to reach support through familiar messaging channels. Apple Messages for Business integration connects the native Messages app on Apple devices to Customer Service Management \(CSM\) Workspace, allowing customers to start conversations without leaving their preferred messaging platform.

When a customer starts a conversation through Apple Messages for Business, the CRM Workspace creates an interaction and links it to the customer's profile, case history, and conversation context, when available. When the user is not logged in, a live agent does a lookup and verifies in the CRM Workspace to link the customer account. Agents can accept these conversations as work items, review related information, and respond without losing conversation history. Virtual Agent can handle initial requests, and Advanced Work Assignment \(AWA\) routes escalated conversations to appropriate agents.

Customers can use Apple Messages for Business to ask questions, resolve issues, schedule appointments, or make purchases. Conversations can transition between automated and agent-assisted support without losing context. This integration reduces channel switching and provides consistent service across support experiences.

Here's an example of a customer service journey using Apple Messages for Business application for omnichannel, seeking shopping assistance with virtual and live agents.

Maya, a premium customer, starts an Apple Messages for Business conversation with Luxe Boutique Collective to get help selecting a gift. CSM creates an interaction, associates it with Maya's profile, purchase history, and conversation history, and starts the flow with Virtual Agent.

Virtual Agent asks qualifying questions, suggests products, checks availability, and offers self-service appointment options. When the Virtual Agent can't resolve the request, the conversation escalates with the transcript and context preserved. AWA routes the work item to Jordan, a live agent, who reviews the context in CSM Workspace and consults Priya, a product specialist, for recommendations.

Priya shares product details and images. Jordan sends appointment options. Maya completes the purchase using Apple Pay. The full interaction remains available for future follow-up across automated and agent-assisted support.

\[Omitted image "omnichannel-apple-messages-for-business-integration-MMASSET0022372.png"\] Alt text: Use case example workflow displaying shopping assistance with virtual and live agents using Apple Messages for Business.

## Apple Messages for Business implementation workflow

Complete these tasks to implement [Conversational Integration with Apple Messages for Business](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/integration-apple-mssg.md). See [Exploring Conversational Integration with Apple Messages for Business](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/exploring-va-apple-msg-business.md) for more information.

|Task|Description|Role|
|----|-----------|----|
|1. [Install Conversational Integration with Apple Messages for Business](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-apple-install.md)|Install the Conversational Integration with Apple Messages for Business plugin from the ServiceNow Store.|Admin, Sys Admin|
|2. [Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/va-integration-messaging-apps.md)|Review the Virtual Agent messaging app integration framework to understand supported channels, rich control capabilities, and live agent transfer patterns.|Admin|
|3. [Set up the integration on Apple Messages for Business](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/set-up-apple-messages.md)|Create and configure Apple Business Register account and obtain the Business ID.|Admin|
|4. [OAuth setup for Apple Messages for Business](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/oauth-setup-apple.md)|Set up OAuth authentication credentials between Apple and ServiceNow.|Admin|
|5. [Integrating the Conversational Integration with Apple Messages for Business app with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-apple-integrating-apps.md)|Link the Apple Messages for Business channel to CSM and configure auto-creation rules.|Admin|
|6. [Capturing information from a user in a Apple Messages for Business chat conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-apple-capture-info.md)|Configure data extraction for customer profile from Apple Messages.|Admin|
|7. [Set up CRM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-workspace-set-up.md)|Design workspace with agent profile cards, rich media widgets, and loyalty status.|CSM Admin|
|8. [Transfer Apple Messages for Business chat conversations to live agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/messg-apple-live-agent-conv.md)|Configure smooth handoff from Virtual Agent to a live agent.|Admin|

**Note:** An admin can configure Rich Controls for Apple Messages. This enables setting up interactive controls for images, appointment pickers, and Apple Pay integration.

