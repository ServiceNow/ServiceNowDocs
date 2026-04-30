---
title: Run scheduled job to publish stop words dictionary, search profiles, and index tables
description: After upgrading to the Zurich release and the Now Assist for Sales and Order Management plugin has been installed, run a scheduled job that publishes the stop word dictionary, search profiles, and index tables for using AI Search in the product catalog. AI Search.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-01-05"
reading_time_minutes: 1
breadcrumb: [AI Search for product catalog, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Run scheduled job to publish stop words dictionary, search profiles, and index tables

After upgrading to the Zurich release and the Now Assist for Sales and Order Management plugin has been installed, run a scheduled job that publishes the stop word dictionary, search profiles, and index tables for using AI Search in the product catalog. AI Search.

## Before you begin

Now Assist for Sales Force Automation \(SFA\) plugin must be installed.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.

2.  In the **Search** field, enter `Scheduled job to publish stop words dictionary, search profiles and index tables`.

3.  Select **Execute Now** to run the scheduled job.

4.  After the scheduled job completes, verify that the Semantic Ingestion State is set as indexed for the Product Offering Indexed Source and the Service Specification Indexed Source.

    1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

    2.  In the AI Search Indexed Sources list, select the following to verify the Semantic Ingestion State :

    -   Product Offering Indexed Source - In the Indexing History related list \(tab\), check that the Semantic Ingestion State displays **indexed**.

        ![Indexing History that shows the indexing of the Product Offering Indexed Source was completed](../image/ai-search-indexed-source-offering.png "Example of Product Offering Indexed Source with Semantic Ingestion State")

    -   Service Specification Indexed Source - In the Indexing History related list \(tab\), check that the Semantic Ingestion State displays **indexed**.

## What to do next

[Enable AI Search in product catalog](enable-ai-search-catalog.md).

