---
title: Submit a purchase request by uploading a quote
description: Use the ServiceNow Otto chat interface in the Employee Center to describe your needs, upload a quote, and submit a purchase request. ServiceNow Otto processes the uploaded quote and creates a purchase requisition for your review. Review all extracted information before submitting, as AI-generated output may require correction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/agentic-ai-spo-quote.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-07-30"
reading_time_minutes: 1
keywords: [Procurement product recommendation AI agent, Agentic AI, AI agent]
breadcrumb: [Submit a purchase request, Use agentic workflows in ServiceNow Otto for SPO, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Submit a purchase request by uploading a quote

Use the ServiceNow Otto chat interface in the Employee Center to describe your needs, upload a quote, and submit a purchase request. ServiceNow Otto processes the uploaded quote and creates a purchase requisition for your review. Review all extracted information before submitting, as AI-generated output may require correction.

## Before you begin

Role required: sn\_spend\_gen\_ai.now\_assist\_requester

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** in your ServiceNow instance.

2.  Select the ServiceNow Otto chat icon \(\[Omitted image "agentic-ai-now-assist-icon.png"\] Alt text: ServiceNow Otto icon.\).

3.  In the chat interface, enter details about the product to purchase.

    ServiceNow Otto displays product recommendations through the Procurement request path recommendation.

4.  Select **Yes** to upload a quote.

    **Note:** If your quote contains more than 50 products, set the **glide.sc.multirow\_set.rows.size** system property to a value greater than the total number of products in the quote. If the **glide.sc.multirow\_set.rows.size** system property does not exist, add it and set the type to Integer.

    For more information on system properties, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

5.  Select **Click here to upload a file** to choose your quote from your device.

    Enter additional details, such as the reason for purchase, expected delivery date, and service period.

    **Note:** The file must be in PDF, PNG, or JPEG format and must not exceed 1 MB.

6.  Verify the quote file name.

    ServiceNow Otto processes the quote and extracts the details for review.

7.  Select the link to open the extracted quote it in a new tab.

8.  Verify that all information was extracted correctly.

    Review the extracted product details, quantities, and pricing before submitting. AI-generated extractions may contain errors.

9.  Select **Submit**.

10. Close the tab and return to the Employee Center.

    Select **Yes** to confirm you have submitted the extracted quote.


## Result

A purchase requisition is created and submitted for approval. Review the requisition details to verify the AI-extracted information is accurate before the approval process begins.

**Parent Topic:**[Submit a purchase request using the ServiceNow Otto AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/request-product-ai-agents.md)

