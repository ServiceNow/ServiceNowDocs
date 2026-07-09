---
title: Confirm product category classification solutions
description: Confirm that the classification solutions and AI Search configuration for product category prediction are trained and active before activating the Spend categorization agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/confirm-product-category-solutions.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-06-23"
reading_time_minutes: 1
keywords: [product category prediction, classification solution, AI Search, machine learning solution, Product Category Classification For PRL, Product Category Classification For POL]
breadcrumb: [Activate the Spend categorization agent, Configure, Now Assist, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Confirm product category classification solutions

Confirm that the classification solutions and AI Search configuration for product category prediction are trained and active before activating the Spend categorization agent.

## Before you begin

Role required: ml\_admin or admin.

## About this task

Product category prediction relies on machine learning classification solutions and an AI Search configuration for purchase lines. The agent predicts the product category before the spend category, so confirm these solutions before activating the related skills or the agent.

The following classification solutions have been added for product category prediction:

-   **Product Category Classification For PRL** — identifies the most appropriate Product Category using product-related information for purchase request lines.
-   **Product Category Classification For POL** — identifies the most appropriate Product Category using product-related information for purchase order lines.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  Locate **Product Category Classification For PRL**.

    This solution classifies purchase request lines into a product category based on product-related attributes such as product name, supplier product, and supplier.

3.  Confirm that the solution status indicates a completed, trained version.

    A trained solution is available to generate predictions.

4.  Locate **Product Category Classification For POL** and confirm that it is also trained and active.

    This solution performs the same classification for purchase order lines.

5.  Confirm that the AI Search configuration for product category classification on purchase lines is published.

    The AI Search configuration provides the semantic index that supports product category prediction.

6.  Review the prediction results or test output to confirm the solutions are ready.

    The solutions return product category predictions with confidence scores, which confirms they are ready for use by the agent.


## Result

The classification solutions \(**Product Category Classification For PRL** and **Product Category Classification For POL**\) and AI Search configuration for product categories are active and ready to support predictions from the Spend categorization agent.

**Parent Topic:**[Activate the Spend categorization agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-spend-categorization-agent.md)

