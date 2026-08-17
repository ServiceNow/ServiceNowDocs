---
title: Confirm spend category similarity solutions
description: Confirm that the machine learning similarity solutions and retrieval configuration used to predict spend categories are trained and active, so the Spend categorization agent can return spend category predictions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/confirm-spend-category-solutions.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-06-23"
reading_time_minutes: 2
keywords: [spend category prediction, similarity solution, retrieval-augmented generation, machine learning solution, Spend Category by PRL, Spend Category by POL]
breadcrumb: [Activate the Spend categorization agent, Configure ServiceNow Otto for SPO, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Confirm spend category similarity solutions

Confirm that the machine learning similarity solutions and retrieval configuration used to predict spend categories are trained and active, so the Spend categorization agent can return spend category predictions.

## Before you begin

The classification solutions for product category prediction are confirmed and active.

Role required: ml\_admin or admin.

## About this task

Spend category prediction relies on machine learning similarity solutions and a retrieval configuration that draw on product-to-spend category taxonomy mappings and similar past purchase lines. The agent predicts the spend category after the product category. Confirm these solutions before activating the related skills or the agent.

The following similarity solutions support spend category prediction:

-   **Spend Category by PRL**: Predicts the appropriate Spend Category for purchase request lines by finding spend categories from similar purchase lines and taxonomy mappings.
-   **Spend Category by POL**: Predicts the appropriate Spend Category for purchase order lines by finding spend categories from similar purchase lines and taxonomy mappings.

## Procedure

1.  Open the machine learning solutions list by navigating to **All** &gt; **Predictive Intelligence** &gt; **Solutions**.

2.  Locate **Spend Category by PRL**.

    This solution finds spend categories from similar purchase request lines and taxonomy mappings rather than from a fixed set of classes.

3.  Confirm that the solution status indicates a completed, trained version.

    A trained solution is available to generate predictions. If no trained version exists, train the solution before you continue.

4.  Locate **Spend Category by POL** and confirm it is trained and active.

    This solution performs the same spend category prediction for purchase order lines.

5.  Confirm that the AI Search configuration for spend category prediction is published.

    The AI Search configuration provides the semantic retrieval that supports spend category prediction.

6.  Review the prediction results or test output for each solution to confirm they are ready.

    The solutions return spend category predictions with confidence scores, which confirms they are ready for use by the agent.


## Result

The similarity solutions \(**Spend Category by PRL** and **Spend Category by POL**\) and retrieval configuration for spend categories are active and ready to support predictions from the Spend categorization agent.

**Parent Topic:**[Activate the Spend categorization agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-spend-categorization-agent.md)

