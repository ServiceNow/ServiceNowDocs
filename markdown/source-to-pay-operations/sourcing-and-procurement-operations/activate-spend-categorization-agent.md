---
title: Activate the Spend categorization agent
description: The Spend categorization agent predicts product and spend categories on purchase requisition lines. Complete the configuration tasks that activate the agent and its supporting prediction services in Now Assist for SPO.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/activate-spend-categorization-agent.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-06-23"
reading_time_minutes: 3
keywords: [Spend categorization agent, product category prediction, spend category prediction, Now Assist, AI agent activation]
breadcrumb: [Configure, Now Assist, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Activate the Spend categorization agent

The Spend categorization agent predicts product and spend categories on purchase requisition lines. Complete the configuration tasks that activate the agent and its supporting prediction services in Now Assist for SPO.

The Spend categorization agent uses AI to predict the product category and spend category for items on purchase requisition lines, reducing manual data entry and helping avoid misclassification. The agent predicts the product category first, followed by the spend category. Predictions draw on machine learning solutions, taxonomy mappings, and text extracted from related attachments.

## Why activation is needed

The Spend categorization agent and its supporting prediction capabilities are inactive when Now Assist for SPO is installed. Activation confirms that the underlying prediction solutions are ready, turns on the related Now Assist skills, sets the prediction system properties, and makes the agent available in the Now Assist panel.

## Activation tasks

Complete the following tasks in the order listed. Each task confirms or enables one part of the prediction chain that the agent depends on.

-   [Confirm product category classification solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/confirm-product-category-solutions.md): Confirm that the classification solution and AI Search configuration used to predict product categories are trained and active.
-   [Confirm spend category similarity solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/confirm-spend-category-solutions.md): Confirm that the similarity solution and retrieval configuration used to predict spend categories are trained and active.
-   [Activate Product and Spend category predictor skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-category-predictor-skills.md): Activate the Product category predictor and Spend category predictor skills in Now Assist Admin.
-   [Confirm category prediction system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/confirm-category-prediction-properties.md): Confirm the system properties that control category prediction, including the confidence score threshold.
-   [Enable Spend categorization agent in Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/enable-agent-na-panel.md): Enable the Spend categorization agent so that users can run it from the Now Assist panel.

-   **[Confirm product category classification solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/confirm-product-category-solutions.md)**  
Confirm that the classification solutions and AI Search configuration for product category prediction are trained and active before activating the Spend categorization agent.
-   **[Confirm spend category similarity solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/confirm-spend-category-solutions.md)**  
Confirm that the machine learning similarity solutions and retrieval configuration used to predict spend categories are trained and active, so the Spend categorization agent can return spend category predictions.
-   **[Activate Product and Spend category predictor skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-category-predictor-skills.md)**  
Activate the Product category predictor and Spend category predictor skills in Now Assist Admin to make both skills available to the Spend categorization agent.
-   **[Confirm category prediction system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/confirm-category-prediction-properties.md)**  
Confirm the system properties that control product and spend category prediction, including the confidence score threshold and whether fallback logic is enabled.
-   **[Enable Spend categorization agent in Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/enable-agent-na-panel.md)**  
Enable the Spend categorization agent in AI Agent Studio so users can run it from the Now Assist panel to validate and update product and spend categories on procurement records.

**Parent Topic:**[Configure Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-now-assist-for-spo.md)

**Related topics**  


[Customize a Now Assist for Sourcing and Procurement Operations \(SPO\) skill]()

[Skill inputs for Now Assist for Sourcing and Procurement Operations \(SPO\)]()

