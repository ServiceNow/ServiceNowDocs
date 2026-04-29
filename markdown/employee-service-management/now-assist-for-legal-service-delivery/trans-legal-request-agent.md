---
title: Triage legal requests agentic workflow
description: Use the Triage legal requests agentic workflow to predict the appropriate legal category and to initiate a transfer after a confirmation from the legal fulfiller or group manager.
locale: en-US
release: australia
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Transfer AI Agents]
breadcrumb: [Agentic workflow, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Triage legal requests agentic workflow

Use the Triage legal requests agentic workflow to predict the appropriate legal category and to initiate a transfer after a confirmation from the legal fulfiller or group manager.

## Triage legal requests agentic workflow overview

**Important:**

-   To run the Triage legal requests agentic workflow, ensure that you have completed all the configurations. For more information, see [Configure Triage legal requests agentic workflow](conf-transfer-legal-request-agent.md).
-   If your generative AI service provider is not Now LLM Service, ensure that the API connections and credentials are configured. For more information, see [Configuring API credentials for generative AI capabilities](https://www.servicenow.com/docs/access?context=configuring-api-credentials-for-generative-ai-capabilities&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
-   
The agentic workflow is triggered under the following conditions:

-   A general legal request is submitted and an assignment rule is configured for it.
-   The **Assigned to** field is updated for a general legal request.

The agentic workflow conversation can be seen in the Now Assist panel by the legal fulfiller or group manager with the now\_assist\_panel\_user role.

## Accessing the Triage legal requests agentic workflow from the AI Agent studio

You can access the agentic workflow from AI Agent Studio when you have the sn\_aia.admin role.

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Triage Legal Requests**.

## AI agents used in the Triage legal requests agentic workflow

|Name|Description|
|----|-----------|
|Record management AI agent|Obtains the request details from the provided description.|
|Record field value prediction AI agent|Checks for similar records and predicts the legal category.|
|Transfer legal request AI agent|Is the supervised agent. The AI agent predicts the appropriate legal category, and initiates a transfer after a confirmation from the legal fulfiller.|

## Using Triage legal requests agentic workflow

The agentic workflow conversation can be seen in the Now Assist panel by the legal fulfiller or group manager with the now\_assist\_panel\_user role.

1.  Open the Now Assist panel by selecting the Now Assist icon ![Now assist icon](../../../common/image/icon-ai-sparkle.png)
2.  In the Now Assist chat panel, select the legal request under the active chat.
3.  See the agentic workflow conversation and the predicted legal category:
    -   If you choose to transfer the general legal request, enter `Yes` and select the send icon \(![Send icon.](../image/send-chat-icon.png)\) in the panel. When it's transferred, the original request is canceled and a new request is created with the predicted legal category. The agentic conversation is closed after the transfer of the legal request.
    -   If you choose not to transfer the general legal request, enter `No` and select the send icon \(![Send icon.](../image/send-chat-icon.png)\) in the panel. The general legal request isn’t transferred and the agentic conversation is closed.

**Parent Topic:**[Using agentic workflow in Now Assist for Legal Service Delivery \(LSD\)](../concept/agentic-ai-now-assist-lsd.md)

