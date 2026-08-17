---
title: Submit a purchase request using the ServiceNow Otto AI agent
description: Use the ServiceNow Otto AI‑powered chat experience in the Employee Center to submit a purchase request. The AI agent analyzes your requirements, displays suitable products or services, and guides you through confirming and submitting the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/request-product-ai-agents.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-07-30"
reading_time_minutes: 3
keywords: [Submit purchase request, Purchase request, Engagement layer]
breadcrumb: [Use agentic workflows in ServiceNow Otto for SPO, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Submit a purchase request using the ServiceNow Otto AI agent

Use the ServiceNow Otto AI‑powered chat experience in the Employee Center to submit a purchase request. The AI agent analyzes your requirements, displays suitable products or services, and guides you through confirming and submitting the request.

## Before you begin

Role required: sn\_spend\_gen\_ai.now\_assist\_requester

## Procedure

1.  In your ServiceNow instance, navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  In the Employee Center interface, select the ServiceNow Otto chat icon \(\[Omitted image "agentic-ai-now-assist-icon.png"\] Alt text: ServiceNow Otto icon.\).

3.  In the chat window, describe the product or service that you want to purchase.

    You can request more than one product or service in the same purchase request.

4.  When prompted, enter **No** to proceed without a quote or Statement of Work.

    ServiceNow Otto analyzes your input using the Procurement request path recommendation and displays up to three products or services.

5.  Select **Show** to view the products.

    ServiceNow Otto shows the top three products or services categorized as an excellent match or good match in the engagement layer.

6.  Select the product or service that you want to purchase.

7.  Select **Submit** to confirm details, such as quantity, supplier, total price, and delivery period.

8.  Select **Edit** to make changes and then enter **Submit**.

9.  When prompted to add attachments, select **Yes** to upload supporting files.

    You can add multiple attachments in PDF, PNG, JPEG, Word, XLSX, or ZIP format.

10. Select **No** to submit the purchase request without attachments.


## Result

The purchase request is successfully submitted through Employee Center using the ServiceNow Otto AI agent.

-   **[Upload a Statement of Work \(SOW\) to request a purchase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-upload-sow.md)**  
Use ServiceNow Otto’s AI-powered chat interface to upload a Statement of Work \(SOW\) and submit your purchase request through Employee Center.
-   **[Submit a purchase request by uploading a quote](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/agentic-ai-spo-quote.md)**  
Use the ServiceNow Otto chat interface in the Employee Center to describe your needs, upload a quote, and submit a purchase request. ServiceNow Otto processes the uploaded quote and creates a purchase requisition for your review. Review all extracted information before submitting, as AI-generated output may require correction.

**Parent Topic:**[Use agentic workflows in ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/agentic-ai-now-assist-spo.md)

**Related topics**  


[Conversational intake for sourcing and procurement agentic workflow]()

[Enable AI agents for the Conversational intake for sourcing and procurement agentic workflow in the ServiceNow Otto panel]()

[Enable AI agents for the Conversational intake for sourcing and procurement agentic workflow in Virtual Agent]()

[Update the product category or spend category in the ServiceNow Otto panel]()

[Email parser agent for Sourcing and Procurement Operations]()

