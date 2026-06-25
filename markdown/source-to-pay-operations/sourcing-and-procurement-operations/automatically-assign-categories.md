---
title: Automatically assign categories during SR and PR creation
description: AI-driven category prediction automatically assigns product and spend categories when sourcing requests, purchase requisitions, or purchase orders are created or updated, ensuring consistent classification at the line level.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/automatically-assign-categories.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, Now Assist for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Automatically assign categories during SR and PR creation

AI-driven category prediction automatically assigns product and spend categories when sourcing requests, purchase requisitions, or purchase orders are created or updated, ensuring consistent classification at the line level.

## Key benefits

When working with sourcing requests \(SRs\), purchase requisitions \(PRs\), purchase orders \(POs\), or invoices, you must classify line-level items into product and spend categories. The Spend categorization agent enables this process by generating and validating AI-driven predictions for line-level items. The **Product category** and **Spend category** fields are updated only when they are empty. This process ensures accurate reporting, consistent procurement processes, and efficient downstream automation while reducing manual effort.

View the Spend categorization agent by navigating to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Spend categorization agent**.

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

\[Omitted image "prl-cat-sol-train.png"\] Alt text: Product Category Classification solution definition interface with Update &amp; Retrain button highlighted.

Both solution types retrain automatically based on configured training frequency. By default, the solution definitions run automatically once every seven days.

## Semantic search used for predictions

When ML classification or similarity solutions return no results, the Spend categorization agent uses retrieval-augmented generation \(RAG\) semantic search as a second-tier mechanism to predict product and spend categories. RAG semantic search matches line item details against the following indexes:

-   purchaseLineForProductClassification
-   supplierProducts
-   purchaseLineForSpendClassification
-   purchaseOrderLineForProductClassification
-   purchaseOrderLineForSpendClassification

## LLM predictor skills used for predictions

When both ML classification or similarity solutions and RAG semantic search return no results, the Spend categorization agent invokes LLM-based predictor skills as the third and final tier. These skills use large language model reasoning to suggest categories for a fulfiller \(`sn_shop.procurement_specialist`\).

-   **Product category predictor**: Suggests the most likely product category when both ML classification and RAG semantic search return no results.
-   **Spend category predictor**: Suggests the appropriate spend category when both ML similarity and RAG semantic search return no results.

These skills predict and update the **Product category** and **Spend category** fields on the PRLs for an SR or PR.

View these skills by navigating to **All** &gt; **Now Assist Admin** &gt; **Finance &amp; Supply Chain** &gt; **Sourcing and Procurement Operations**.

## How to configure

The following system properties control category prediction behavior:

|Property|Description|Default value|
|--------|-----------|-------------|
|`sn_spend_gen_ai.spend_category_confidence_score_threshold`|Defines the confidence score threshold for predicting the Product category and Spend category fields. Set a value between 0 and 100.|80|
|`sn_spend_gen_ai.enable_category_fallback_logic`|Enables LLM-based fallback \(Product category predictor and Spend category predictor skills\) for product and spend category prediction when both ML and RAG semantic search return no results. Configurable by users with the `sn_shop.procurement_administrator` role.|true|

## Product and spend category prediction logic

The Spend categorization agent uses a three-tier fallback chain to predict product and spend categories for SR and PR records.

|Tier|Mechanism|Condition to advance to next tier|
|----|---------|---------------------------------|
|1|ML Classification and Similarity|Returns no result|
|2|RAG Semantic Search|Returns no result and `sn_spend_gen_ai.enable_category_fallback_logic` is set to `true`|
|3|Product category predictor and Spend category predictor skills|None|

**Note:** When a product category is already populated on a purchase request line \(PRL\), spend category candidates are filtered based on the spend-category-to-product-category mappings in the Spend Categories table. For more information, see [Map spend categories to product categories manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/map-spend-product-categories.md).

If one spend category is mapped, it is auto-selected without further ML or RAG input. If multiple spend categories are mapped, ML and RAG results are filtered to that mapped set only. If no mapping exists, the full result set is used.

## How it works

When a new sourcing request \(SR\) or purchase request \(PR\) is created using the **I need a product**, **I need a service**, or **I need to submit a quote** record producers, the Spend categorization agent is automatically triggered. The Spend categorization agent predicts and updates the product category and spend category on the purchase request lines \(PRLs\).

If the AI-predicted category differs from the category selected by the requester, the **Product category** and **Spend category** fields are updated only when the prediction confidence score exceeds 80%.

Visual indicators appear next to the **Product category** and **Spend category** fields in the Playbook view and the Purchase Line related lists, indicating that the fields were updated using AI predictions. In such cases, a corresponding comment is added to the activity stream, for example, "AI-suggested Spend category updated from X to Y."

\[Omitted image "prl-ai-banner.png"\] Alt text: PRL form showing AI-suggested updates to Product and Spend category fields.

You can manually select different values for either category field from the Product category and Spend category drop-down lists on the Purchase Line form.

\[Omitted image "prl-ai-prediction.png"\] Alt text: Purchase Line form showing Product category drop-down list with AI predictions highlighted.

Any user-selected overrides are captured and used to improve future model accuracy. When a different value is selected, a banner appears at the top of the form that informs you that an AI-predicted value was applied.

The prediction model also analyzes information in documents attached to the SR or PR, such as the product name and product description, to predict the product and spend categories.

-   **[Audit purchase lines automatically when predictive fields change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/audit-prls-predictive-fields.md)**  
Automated audit compares existing categories with the latest AI prediction when key predictive fields are updated in a service request or purchase requisition, flagging inconsistencies without automatically updating category fields.
-   **[Predict categories for PRLs and POLs imported through integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/predict-categories-integrations.md)**  
Automatically predict and assign product and spend categories for imported purchase requisition lines and purchase order lines using scheduled on-demand scripts.
-   **[Ensure consistent invoice spend categories during PO matching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/invoice-po-spend-categories.md)**  
Maintain aligned spend categories when matching invoice lines with purchase order lines by applying the spend category from the PO line to the corresponding invoice line.

**Parent Topic:**[Explore Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-exploring.md)

**Related topics**  


[Supporting information for Now Assist for Sourcing and Procurement Operations \(SPO\)]()

