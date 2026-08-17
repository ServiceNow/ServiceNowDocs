---
title: Confirm category prediction system properties
description: Confirm the system properties that control product and spend category prediction, including the confidence score threshold and whether fallback logic is enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/confirm-category-prediction-properties.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-06-23"
reading_time_minutes: 1
keywords: [system properties, confidence score threshold, category prediction, fallback logic]
breadcrumb: [Activate the Spend categorization agent, Configure ServiceNow Otto for SPO, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Confirm category prediction system properties

Confirm the system properties that control product and spend category prediction, including the confidence score threshold and whether fallback logic is enabled.

## Before you begin

The Product category predictor and Spend category predictor skills are active.

Role required: admin.

## About this task

|Property|Description|
|--------|-----------|
|**sn\_spend\_gen\_ai.spend\_category\_confidence\_score\_threshold**|Sets the confidence score threshold for product category or spend category prediction. Accepts a number from 0 through 100. The default value is 80.|
|**sn\_spend\_gen\_ai.enable\_category\_fallback\_logic**|Enables fallback logic for product and spend category prediction. When the value is set to true, the agent suggests a category when the primary prediction doesn't meet the confidence threshold. This property is set to true by default.|

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the **sn\_spend\_gen\_ai.spend\_category\_confidence\_score\_threshold** property.

3.  Confirm that the value is a number from 0 through 100.

    The default value is 80. A higher value applies predictions only when confidence is higher, which reduces the number of automatic updates.

4.  Search for the **sn\_spend\_gen\_ai.enable\_category\_fallback\_logic** property.

5.  Confirm that the value is set to true.

    A value of true enables fallback logic and is the default. When fallback logic is enabled, the agent suggests a category if the primary prediction doesn't meet the confidence threshold.

6.  If you change a value, save the property.

    The agent uses the updated property the next time it predicts a category.


## Result

The confidence score threshold and fallback logic settings are confirmed, and the agent applies them when it predicts product and spend categories.

**Parent Topic:**[Activate the Spend categorization agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-spend-categorization-agent.md)

