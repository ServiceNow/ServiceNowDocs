---
title: Request a procurement item using SPO MCP Server
description: Submit a procurement request for catalog and off-catalog items through an MCP client connected to SPO MCP Server in ServiceNow Otto for Sourcing and Procurement Operations \(SPO\). The MCP client guides you through discovery questions, displays product recommendations, and routes you to Shopping Hub or Employee Center to complete your request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/conversational-intake-using-spo-mcp-server.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 2
keywords: [Conversational intake, SPO MCP Server, MCP Client]
breadcrumb: [Use SPO MCP Server, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Request a procurement item using SPO MCP Server

Submit a procurement request for catalog and off-catalog items through an MCP client connected to SPO MCP Server in ServiceNow Otto for Sourcing and Procurement Operations \(SPO\). The MCP client guides you through discovery questions, displays product recommendations, and routes you to Shopping Hub or Employee Center to complete your request.

## Before you begin

Before you begin, confirm the following:

-   SPO MCP Server must be activated and connected to your MCP client.
-   You must have access to an MCP client such as Claude.

Role required: sn\_spend\_gen\_ai.now\_assist\_requester

## About this task

Use conversational intake to streamline procurement requests. You can ask procurement questions and submit purchase requests without leaving the MCP client chat. Conversational intake:

-   Handles how-to and knowledge base \(KB\) article questions about procurement processes.
-   Routes non-purchasing requests to create a procurement request \(PR\) or service catalog request \(SR\).
-   Presents discovery questions to identify the supplier and amount needed for purchase requests.
-   Validates selections against knowledge base articles and approval rules.
-   Routes you to pre-filled on-catalog or off-catalog request forms.

## Procedure

1.  Open your MCP client, such as Claude, that is connected to your ServiceNow instance using the SPO MCP Server.

    For more information on how to configure SPO MCP Server, see [Activate SPO MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-spo-mcp-server.md).

2.  Enter your procurement request into the chat.

    For example, enter `I want to purchase a tripod from ServiceNow`.

    The Initialize Procurement Session tool retrieves your user profile information, policies, approval rules, and product categories relevant to your request.

3.  Answer the discovery questions that appear in the chat.

    Discovery questions may include:

    -   What is the quantity you need?
    -   What is the purchase reason?
    -   What is your budget?
    Respond conversationally or select from the options provided.

4.  Review the product recommendations displayed in the chat.

    Each recommendation includes a description of why it matches your requirements.

5.  Select a product from the recommendations.

    You can type the number corresponding to your choice. For example, `1` for the first item, or describe which product you prefer.

    The Describe Intake Requirements tool generates a pre-filled link to either Shopping Hub \(for catalog items\) or Employee Center \(for off-catalog items\).

6.  Select the generated link to open Shopping Hub or Employee Center.

    The link pre-fills details that you provided in the chat, such as quantity, purchase reason, and product category.

    Shopping Hub or Employee Center opens with your procurement form partially completed.

7.  Complete any remaining required fields in Shopping Hub or Employee Center.

    Review all fields on the form. Fill in any information that was not automatically populated, such as:

    -   Request details
    -   Additional comments or specifications
    -   Any fields marked as required by your organization
8.  Select **Submit** to submit your request.

    Your request is submitted to your organization's procurement queue.


## Result

Your procurement request is submitted. You can track the request status in Employee Center or through your organization's procurement system.

