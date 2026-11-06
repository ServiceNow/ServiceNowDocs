---
title: Associate a test group to a specifications or product model
description: Establish a relationship between test groups and their respective specifications or product model to determine the tests that must be executed for a given inventory. This relationship confirms that the appropriate tests are identified and executed based on the defined specifications. Without this association, the system can’t accurately assign the necessary tests for each inventory item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/define-relationship-test-group-specifications.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [specification to test group relationship, associate test group, product model]
breadcrumb: [Setting up a test group, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Associate a test group to a specifications or product model

Establish a relationship between test groups and their respective specifications or product model to determine the tests that must be executed for a given inventory. This relationship confirms that the appropriate tests are identified and executed based on the defined specifications. Without this association, the system can’t accurately assign the necessary tests for each inventory item.

## Before you begin

The test group must be in the Published state. See [Publish a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/publish-test-groups.md).

To relate the test group to a specification, the Product Model plugin \(com.sn\_prd\_pm\) must be active. You can only relate the test group to a product model without this plugin. For more information, [Plugins installed with Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-requirements.md).

Role required: sn\_st\_mgmt.test\_def\_creator

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select the test group that you want to open.

    If the test group isn't published, the system shows the error "Test group state must be in Published state."

3.  In the Specification To Test Group Relationships related list, select **New**.

4.  On the form, fill in the fields.

    For more information about the fields, see [Specification to Test Group Relationship form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/spec-to-test-group-relationship-fields.md).

5.  Select **Submit**.


## Result

A specification or product model is associated with the test group.

## What to do next

To apply the test group only to the product inventory records that meet certain conditions, define conditions for the relationship. This requires the Product Inventory plugin and a relationship that uses a specification. For more details, see [Define conditions for a test group relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-conditions-for-test-group-relationship.md).

