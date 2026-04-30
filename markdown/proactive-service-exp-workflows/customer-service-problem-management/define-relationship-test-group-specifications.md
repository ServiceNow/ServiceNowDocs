---
title: Associate a test group with a specifications or product model
description: Establish a relationship between test groups and their respective specifications or product model to determine the tests that must be executed for a given inventory. This relationship confirms that the appropriate tests are identified and executed based on the defined specifications. Without this association, the system can’t accurately assign the necessary tests for each inventory item.
locale: en-US
release: yokohama
product: Customer Service Problem Management
classification: customer-service-problem-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up a test group, Configuring Customer Service Problem Management, Customer Service Problem Management]
---

# Associate a test group with a specifications or product model

Establish a relationship between test groups and their respective specifications or product model to determine the tests that must be executed for a given inventory. This relationship confirms that the appropriate tests are identified and executed based on the defined specifications. Without this association, the system can’t accurately assign the necessary tests for each inventory item.

## Before you begin

Role required: sn\_st\_mgmt.test\_def\_creator

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select the test group that you want to open.

    Only the published test groups are displayed in the list.

3.  In the Specification or product model to Test Group Relationship related list, define a relationship by selecting **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Specification|Name of the specification.|
    |Product model|Name of the inventory.|
    |Test Group|Auto-populated name of the test group for which you’re specifying a relationship.|

5.  Select **Submit**.


**Parent Topic:**[Setting up a test group](../concept/setting-test-group.md)

