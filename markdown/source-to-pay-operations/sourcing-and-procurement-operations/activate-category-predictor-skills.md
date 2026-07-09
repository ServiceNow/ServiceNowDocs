---
title: Activate Product and Spend category predictor skills
description: Activate the Product category predictor and Spend category predictor skills in Now Assist Admin to make both skills available to the Spend categorization agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/activate-category-predictor-skills.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-06-23"
reading_time_minutes: 1
keywords: [Now Assist skills, Product category predictor, Spend category predictor, Now Assist Admin]
breadcrumb: [Activate the Spend categorization agent, Configure, Now Assist, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Activate Product and Spend category predictor skills

Activate the Product category predictor and Spend category predictor skills in Now Assist Admin to make both skills available to the Spend categorization agent.

## Before you begin

Verify that the classification and similarity solutions for product and spend category prediction are active.

Role required: admin.

## About this task

The Spend categorization agent uses two Now Assist skills in the Category Prediction skill family. Each skill suggests a category for a fulfiller when the primary machine learning \(ML\) prediction doesn't meet the confidence threshold. Both skills are inactive by default.

|Skill|Description|
|-----|-----------|
|Product category predictor|Suggests the most likely product category for a fulfiller when the primary prediction doesn't meet the confidence threshold.|
|Spend category predictor|Suggests the appropriate spend category for a fulfiller when the primary prediction doesn't meet the confidence threshold.|

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin**.

2.  Open the Now Assist for Sourcing and Procurement Operations experience that contains the Category Prediction skills.

3.  In the Finance and Supply Chain workflow group, select **Sourcing and Procurement Operations** to view the skills for the Now Assist for SPO features.

4.  Select the **Product category predictor** skill.

    Verify the skill is in the Category Prediction skill family.

5.  Set the skill to active.

    The Product category predictor skill is available to the agent.

6.  Return to the skills list and select the **Spend category predictor** skill.

7.  Set the skill to active.

    The Spend category predictor skill is available to the agent.


## Result

Both Category Prediction skills are active and available to the Spend categorization agent.

**Parent Topic:**[Activate the Spend categorization agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-spend-categorization-agent.md)

