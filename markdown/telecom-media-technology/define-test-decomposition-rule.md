---
title: Define a test decomposition rule
description: Add a test decomposition rule to the mapping between a test group and a test definition to specify the characteristic and characteristic option that the rule uses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/define-test-decomposition-rule.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [test decomposition rule, test group]
breadcrumb: [Setting up a test group, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Define a test decomposition rule

Add a test decomposition rule to the mapping between a test group and a test definition to specify the characteristic and characteristic option that the rule uses.

## Before you begin

The Product Model plugin \(com.sn\_prd\_pm\) must be active. See [Plugins installed with Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-requirements.md).

Define at least one characteristic for the test group. For ore information, see [Define a characteristic for a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-characteristic-for-test-group.md).

Map the test definition to the test group. A test decomposition rule belongs to that mapping. For more information, see [Map test definitions to a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/add-test-definitions-to-test-group.md).

Role required: sn\_st\_mgmt.test\_def\_creator

## About this task

A test decomposition rule belongs to the mapping between a test group and a test definition, so you create it from that mapping.

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select the test group that you want to open.

3.  In the Test Group To Definition Mapping related list, open the mapping for the test definition.

4.  In the Test Decomposition Rules related list, select **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Test Group Definition|Mapping between the test group and the test definition that the rule belongs to.|
    |Characteristic|Characteristic that the rule uses. The list shows only characteristics that belong to the test group. You must select a characteristic.|
    |Characteristic option|Option for the selected characteristic. The list shows only the options that you defined for that characteristic on the test group.|

6.  Select **Submit**.


## Result

The rule is added to the mapping. The system doesn't save a rule that has no test group definition or characteristic.

## What to do next

If the test group is in the Draft state, publish it when it is ready. See [Publish a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/publish-test-groups.md).

