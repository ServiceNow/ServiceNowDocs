---
title: Define conditions for a test group relationship
description: Add conditions to the relationship between a specification and a test group so that the test group applies only to product inventory records that meet the conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/define-conditions-for-test-group-relationship.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 2
keywords: [conditions, specification, product inventory]
breadcrumb: [Setting up a test group, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Define conditions for a test group relationship

Add conditions to the relationship between a specification and a test group so that the test group applies only to product inventory records that meet the conditions.

## Before you begin

The test group must be in the Published state. See [Publish a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/publish-test-groups.md).

Create the relationship between the test group and the specification. See [Associate a test group to a specifications or product model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-relationship-test-group-specifications.md).

The Product Model plugin \(com.sn\_prd\_pm\) must be active, because you set conditions for a specification. See [Plugins installed with Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-requirements.md).

The Product Inventory plugin \(com.sn\_prd\_invt\) must be active.

Role required: sn\_st\_mgmt.test\_def\_creator

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select the test group that you want to open.

3.  In the Specification To Test Group Relationships related list, open the relationship that you want to add conditions to, or select **New**.

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

## What to do next

To scope the test group to more than one set of conditions, create another relationship for the same specification with different conditions or a different product inventory table. The system treats relationships that differ by conditions or by product inventory table as different relationships.

