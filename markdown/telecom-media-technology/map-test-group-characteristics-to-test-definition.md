---
title: Map a test group characteristic to a test definition
description: Map a characteristic of a test group to a test definition so that the test definition inherits the characteristic from the group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/map-test-group-characteristics-to-test-definition.html
release: brazil
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [characteristic mapping, test group, test definition]
breadcrumb: [Test group characteristics, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Map a test group characteristic to a test definition

Map a characteristic of a test group to a test definition so that the test definition inherits the characteristic from the group.

## Before you begin

Define the characteristic for the test group. See [Define a characteristic for a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/define-characteristic-for-test-group.md).

Role required: sn\_st\_mgmt.test\_def\_creator

## About this task

You create each mapping yourself. The system doesn't create mappings automatically.

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Definitions** &gt; **All**.

2.  Select the test definition that you want to open.

3.  In the Specification or product model to Test Definition Relationship related list, define a relationship by selecting **New**.

4.  Select the test group that you want to open.

    Only the published test groups are displayed in the list.

5.  In the Test Characteristic Attribute Mapping related list, map a test characteristic by selecting **New**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Test definition|Test definition that inherits the characteristic. You can't change this value after you save the record.|
    |Source test characteristic|Characteristic of the test group that you want the test definition to inherit. The list shows only characteristics that belong to a test group. You can't change this value after you save the record.|
    |Target definition characteristic|Characteristic that belongs to the selected test definition and receives the inherited value. This field is optional. The list shows only characteristics of the selected test definition that no other mapping in the same test group already uses.|

    **Note:** You can create only one mapping for the same test definition and source characteristic. If you map a target characteristic that another mapping in the same test group already uses, the system doesn't save the record.

7.  Select **Submit**.


## Result

The test definition inherits the characteristic from the test group. To stop inheriting it, delete the mapping.

