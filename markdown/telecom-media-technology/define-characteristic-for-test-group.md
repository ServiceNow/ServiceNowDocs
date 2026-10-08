---
title: Define a characteristic for a test group
description: Add a characteristic to a test group so that its test definitions can inherit the characteristic and the test group run can show it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/define-characteristic-for-test-group.html
release: brazil
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [test group, characteristic]
breadcrumb: [Test group characteristics, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Define a characteristic for a test group

Add a characteristic to a test group so that its test definitions can inherit the characteristic and the test group run can show it.

## Before you begin

Role required: sn\_st\_mgmt.test\_def\_creator, admin

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select the test group that you want to open.

3.  In the Test Characteristics related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Characteristic|Service or product characteristic that the tests in the group use. The list excludes characteristics that you already added to this test group.|
    |Characteristic option|Option for the selected characteristic.|
    |Test group|Auto-populated name of the test group for which you're defining the characteristic.|
    |Is Mandatory|Option to specify that the characteristic is required for the test.|

    **Note:** A characteristic belongs to either a test group or a test definition, not both. You can't change the owner after you save the record.

5.  Select **Submit**.


## Result

The characteristic is added to the test group. You can now map it to a test definition. See [Map a test group characteristic to a test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/map-test-group-characteristics-to-test-definition.md).

