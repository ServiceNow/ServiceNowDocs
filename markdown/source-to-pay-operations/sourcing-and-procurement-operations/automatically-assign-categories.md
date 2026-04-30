---
title: Automatically assign categories during SR and PR creation
description: AI-driven category prediction automatically assigns product and spend categories when service requests, purchase requisitions, or purchase orders are created or updated, ensuring consistent classification at the line level.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore Now Assist for Sourcing and Procurement Operations \(SPO\), Now Assist for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Automatically assign categories during SR and PR creation

AI-driven category prediction automatically assigns product and spend categories when service requests, purchase requisitions, or purchase orders are created or updated, ensuring consistent classification at the line level.

## Key benefits

When working with service requests \(SRs\), purchase requisitions \(PRs\), purchase orders \(POs\), or invoices, you must classify line-level items into product and spend categories. The Spend categorization agent enables this process by generating and validating AI-driven predictions for line-level items. The **Product category** and **Spend category** fields are updated only when they are empty. This process ensures accurate reporting, consistent procurement processes, and efficient downstream automation while reducing manual effort.

View the Spend categorization agent by navigating to **All** &gt; **** &gt; **AI Agent Studio** &gt; **** &gt; **Create and manage** &gt; **Spend categorization agent**.

## Classification solutions used for predictions

For predicting product category on PRs and SRs, the following classification solutions have been added:

-   Product Category Classification For PRL
-   Product Category Classification For POL

Classification solutions identify the most appropriate Product Category using product related information.

You can access the classification definitions by navigating to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

## Similarity solutions used for predictions

For predicting spend category on PRs and SRs, the following similarity solutions have been added:

-   Spend Category by PRL
-   Spend Category by POL

Similarity solutions compare line item details with previously categorized data to suggest the best Spend Category.

You can access the similarity definitions by navigating to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

To use the solution definitions for both PRL and POL in your instance, open each definition and select **Update and Retrain**. This action ensures that the solution definitions are trained to meet your specific requirements. Any PR or SR with empty Product category and Spend category fields is updated using the latest model outputs.

**Note:** Users with the category\_manager\_admin and now\_assist\_admin roles can update the solution definitions.

![Product Category Classification solution definition interface with Update & Retrain button highlighted.](../image/prl-cat-sol-train.png)

Both solution types retrain automatically based on configured training frequency. By default, the solution definitions run automatically once every seven days.

## How to configure

The `sn_spend_genn_ai.spend_category_confidence_score_threshold` system property defines the confidence score threshold for predicting the Product category and Spend category fields. You can set a value between 0 and 100. The default value is 80.

## Product and spend category prediction logic

First, the Spend categorization agent predicts the product and spend categories for SR and PR records. It uses the prediction models and the system property confidence threshold value.

If the confidence score is below the threshold, the Spend categorization agent does not predict categories. In this case, the Product category predictor and Spend category predictor skills act as fallback logic.

-   **Product category predictor**: Suggests the most likely product category for a fulfiller \(sn\_shop.procurement\_specialist\) when the primary ML-based category prediction does not meet the confidence threshold.
-   **Spend category predictor**: Suggests the appropriate spend category for a fulfiller \(sn\_shop.procurement\_specialist\) when primary ML-based category prediction does not meet the confidence threshold.

These skills run and predict and update the **Product category** and **Spend category** fields on the PRLs for an SR or PR.

View these skills by navigating to **All** &gt; **Now Assist Admin** &gt; **Finance &amp; Supply Chain** &gt; **Sourcing and Procurement Operations**.

## How it works

When a new service request \(SR\) or purchase request \(PR\) is created using the **I need a product**, **I need a service**, or **I need to submit a quote** record producers, the Spend categorization agent is automatically triggered. The Spend categorization agent predicts and updates the product category and spend category on the purchase request lines \(PRLs\).

If the AI-predicted category differs from the category selected by the requester, the **Product category** and **Spend category** fields are updated only when the prediction confidence score exceeds 80%.

Visual indicators appear next to the **Product category** and **Spend category** fields in the Playbook view and the Purchase Line related lists, indicating that the fields were updated using AI predictions. In such cases, a corresponding comment is added to the activity stream, for example, "AI-suggested Spend category updated from X to Y."

![PRL form showing AI-suggested updates to Product and Spend category fields.](../image/prl-ai-banner.png)

You can manually select different values for either category field from the Product category and Spend category drop-down lists on the Purchase Line form.

![Purchase Line form showing Product category drop-down list with AI predictions highlighted.](../image/prl-ai-prediction.png)

Any user-selected overrides are captured and used to improve future model accuracy. When a different value is selected, a banner appears at the top of the form that informs you that an AI-predicted value was applied.

The prediction model also analyzes information in documents attached to the SR or PR, such as the product name and product description, to predict the product and spend categories.

-   **[Audit purchase lines automatically when predictive fields change](audit-prls-predictive-fields.md)**  
Automated audit compares existing categories with the latest AI prediction when key predictive fields are updated in a service request or purchase requisition, flagging inconsistencies without automatically updating category fields.
-   **[Predict categories for PRLs and POLs imported through integrations](predict-categories-integrations.md)**  
Automatically predict and assign product and spend categories for imported purchase requisition lines and purchase order lines using scheduled on-demand scripts.
-   **[Ensure consistent invoice spend categories during PO matching](invoice-po-spend-categories.md)**  
Maintain aligned spend categories when matching invoice lines with purchase order lines by applying the spend category from the PO line to the corresponding invoice line.

**Parent Topic:**[Explore Now Assist for Sourcing and Procurement Operations \(SPO\)](now-assist-spo-exploring.md)

**Related topics**  


[Supporting information for Now Assist for Sourcing and Procurement Operations \(SPO\)](now-assist-spo-supporting-info.md)

