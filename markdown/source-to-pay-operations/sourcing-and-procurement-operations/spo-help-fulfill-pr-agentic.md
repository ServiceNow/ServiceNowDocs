---
title: Conversational intake for sourcing and procurement agentic workflow
description: The Conversational intake for sourcing and procurement agentic workflow addresses your procurement needs by providing product recommendations, guided checkout, off-catalog processes, and detailed product information. It also answers questions and tracks related records.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-12-01"
reading_time_minutes: 5
keywords: [AI agents, agentic AI]
breadcrumb: [Use agentic workflows, Now Assist for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Conversational intake for sourcing and procurement agentic workflow

The Conversational intake for sourcing and procurement agentic workflow addresses your procurement needs by providing product recommendations, guided checkout, off-catalog processes, and detailed product information. It also answers questions and tracks related records.

## Conversational intake for sourcing and procurement agentic workflow overview

The Conversational intake for sourcing and procurement agentic workflow handles and resolves procurement-related inquiries, which include the product information, purchase intent, sourcing new items, or tracking purchasing records.

## Accessing the Conversational intake for sourcing and procurement agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Conversational intake for sourcing and procurement**.

## Available AI agents in the Conversational intake for sourcing and procurement agentic workflow

The following table lists the agents that are used in the Conversational intake for sourcing and procurement agentic workflow.

**Important:** In the Define availability screen for the AI agent, make sure that the Status toggle is enabled to activate the AI agent.

<table id="table_bpl_31s_y2c"><thead><tr><th>

AI agent

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Procurement request tracking AI agent

</td><td>

Handles tracking-related queries throughout the procurement lifecycle. Identifies and responds to requests for tracking, status checks, updates, or follow-ups on procurement records, such as sourcing requests, purchase requisitions, purchase orders, and procurement cases.Understands the query context to retrieve the relevant record, even when a record number isn’t provided, and displays a direct link to the record.

</td></tr><tr><td>

Procurement product recommendation AI agent

</td><td>

Handles procurement-related intents by identifying explicit or implicit requests to buy or source products or services. It recommends up to three product or service options based on minimal user input and guides users through the appropriate procurement flow. You can request for multiple items in one request.After presenting recommendations, it checks user interest and triggers either a sourcing or purchasing plan based on internal rules. Upon user confirmation, it creates the relevant record and displays the plan.

You can add an attachment in PDF, PNG, JPEG, Word, XLSX, or ZIP format \(up to 10 GB\) when submitting your request to include any additional information.

</td></tr><tr><td>

Procurement inquiry analysis AI agent

</td><td>

Retrieves and displays relevant knowledge articles to address sourcing and procurement queries. If no relevant articles are found, or if intent is unclear, redirects you to a live agent.

</td></tr></tbody>
</table>The AI agent decision log displays the AI agents that are working on a request. You can watch their interactions, decisions, and thought processes as they happen in real time.

## Tools mapped to the Track request AI agent

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Scripts|Autonomous|Get records data|Searches the Knowledge Graph for procurement records that match a generated query, returning relevant links and details.|
|Scripts|Autonomous|Record summary|Summarizes the provided information, ensuring that the summary captures the key details and intent of an inquiry.|

## Tools mapped to the Procurement product recommendation AI agent

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Scripts|Autonomous|Supplier recommendation tool|Recommends suitable suppliers using the Supplier Recommendation Skill.|
|Scripts|Autonomous|Recommendation|Generates a list of products based on the product name, additional details, and supplier preferences.|
|Scripts|Autonomous|Show more results|Displays additional product recommendations for a selected item.|
|Scripts|Autonomous|Channel rule engine|Suggests a checkout channel based on user input.|
|Scripts|Autonomous|Create purchasing plan|Creates or updates the purchasing plan from user-provided details and returns it in formatted HTML.|
|Scripts|Autonomous|Create sourcing plan|Creates or updates the sourcing plan from user-provided details and returns it in formatted HTML.|
|Scripts|Autonomous|Procurement attachment tool|Supports attachment uploads for purchase and sourcing requests.|
|Scripts|Autonomous|Create purchasing record|Creates purchasing records from the finalized plan \(with optional attachments\) and returns a submission summary.|
|Scripts|Autonomous|Create sourcing record|Creates sourcing requests from the finalized plan \(with optional attachments\) and returns a submission summary.|
|Scripts|Autonomous|Create a document task|Creates a document task that gathers delivery period and purchase reason information.|
|Scripts|Autonomous|Created record from document|Creates records once the document task is submitted.|
|Conversational topics|Autonomous|Quote or Sow attachment|Supports adding a quote or SOW document by passing the uniquely generated document conversation ID \(documentConversationId\) as input to the tool.|

## Tools mapped to the Procurement inquiry analysis AI agent

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Scripts|Autonomous|Get relevant knowledge article|Retrieves and displays relevant knowledge articles for sourcing and procurement queries.|
|Scripts|Autonomous|Connect to live agent|Escalates to a live SPO agent upon user request.|
|Scripts|Autonomous|Redirect to Employee Center|Politely deflects unsupported requests and directs users to Employee Center resources.|

**Parent Topic:**[Using agentic workflows in Now Assist for Sourcing and Procurement Operations](agentic-ai-now-assist-spo.md)

**Related topics**  


[Enable AI agents for the Conversational intake for sourcing and procurement agentic workflow in the Now Assist panel](../task/activate-fulfill-pr-agentic-workflow.md)

[Enable AI agents for the Conversational intake for sourcing and procurement agentic workflow in Virtual Agent](../task/activate-fulfill-pr-agentic-workflow-va.md)

[Submit a purchase request using the Now Assist AI agent](../task/request-product-ai-agents.md)

[Update the product category or spend category in the Now Assist panel](../task/update-product-spend-category.md)

