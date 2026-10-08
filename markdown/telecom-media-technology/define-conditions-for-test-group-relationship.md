---
title: Define conditions for a test group relationship
description: Add conditions to the relationship between a specification and a test group so that the test group applies only to product inventory records that meet the conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/define-conditions-for-test-group-relationship.html
release: brazil
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [conditions, specification, product inventory]
breadcrumb: [Test group characteristics, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Define conditions for a test group relationship

Add conditions to the relationship between a specification and a test group so that the test group applies only to product inventory records that meet the conditions.

## Before you begin

Create the relationship between the test group and the specification. See [Associate a test group with a specifications or product model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/define-relationship-test-group-specifications.md).

The Product Inventory plugin \(com.sn\_prd\_invt\) must be active.

Role required: sn\_st\_mgmt.test\_def\_creator

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select the test group that you want to open.

3.  In the Specification or product model to Test Group Relationship related list, open the relationship that you want to add conditions to, or select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Specification|Select the specification. The fields for the conditions appear only after you select a specification. You can't set conditions when you select a product model.|
    |Product inventory table|Select the table whose records the conditions apply to. The list shows the Product Inventory table and its child tables.|
    |Conditions|Define the conditions. When you select a specification, the system adds a condition for that specification. The system keeps the other conditions that you define.|

5.  Select **Submit**.


## Result

The test group applies to a product inventory record only when the record has the specification and meets the conditions. Relationships without conditions continue to apply as before.

The system saves a relationship only if you provide either a specification or a product model. Conditions can't be set together with a product model.

