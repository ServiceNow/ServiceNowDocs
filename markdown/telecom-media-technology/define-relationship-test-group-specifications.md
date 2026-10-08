---
title: Associate a test group with a specifications or product model
description: Establish a relationship between test groups and their respective specifications or product model to determine the tests that must be executed for a given inventory. This relationship confirms that the appropriate tests are identified and executed based on the defined specifications. Without this association, the system can’t accurately assign the necessary tests for each inventory item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/define-relationship-test-group-specifications.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Setting up a test group, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
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

<table id="table_gcm_vrp_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Specification

</td><td>

Name of the specification.**Note:** Provide either a specification or a product model. The system doesn't save a relationship that has both or neither.

</td></tr><tr><td>

Product model

</td><td>

Name of the inventory.**Note:** Provide either a specification or a product model. The system doesn't save a relationship that has both or neither.

</td></tr><tr><td>

Product inventory table

</td><td>

Table that contains the product inventory records that the conditions apply to. This field appears after you select a specification.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that a product inventory record must meet for the test group to apply. You can't set conditions when you select a product model. For details, see [Define conditions for a test group relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/define-conditions-for-test-group-relationship.md).

</td></tr><tr><td>

Test Group

</td><td>

Auto-populated name of the test group for which you’re specifying a relationship.

</td></tr></tbody>
</table>5.  Select **Submit**.


## What to do next

A specification or product model is associated with the test group. You can now publish the test group. For more details, see [Publish a test groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/publish-test-groups.md).

