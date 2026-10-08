---
title: Define a test decomposition rule
description: Add a test decomposition rule to the mapping between a test group and a test definition to specify the characteristic and characteristic option that the rule uses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/define-test-decomposition-rule.html
release: brazil
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [test decomposition rule, test group]
breadcrumb: [Test group characteristics, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Define a test decomposition rule

Add a test decomposition rule to the mapping between a test group and a test definition to specify the characteristic and characteristic option that the rule uses.

## Before you begin

Define at least one characteristic for the test group. See [Define a characteristic for a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/define-characteristic-for-test-group.md).

Role required: sn\_st\_mgmt.test\_def\_creator

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select the test group that you want to open.

3.  Open the mapping between the test group and the test definition.

4.  In the Test Decomposition Rules related list, select **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Characteristic|Characteristic that the rule uses. The list shows only characteristics that belong to the test group. You must select a characteristic.|
    |Characteristic option|Option for the selected characteristic.|

6.  Select **Submit**.


## Result

The rule is added to the mapping. The system doesn't save a rule that has no test group definition or characteristic.

