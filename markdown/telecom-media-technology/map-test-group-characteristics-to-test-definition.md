---
title: Map a test group characteristic to a test definition
description: Map a characteristic of a test group to a test definition so that the test definition inherits the characteristic from the group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/map-test-group-characteristics-to-test-definition.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 2
keywords: [characteristic mapping, test group, test definition]
breadcrumb: [Setting up a test group, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Map a test group characteristic to a test definition

Map a characteristic of a test group to a test definition so that the test definition inherits the characteristic from the group.

## Before you begin

The Product Model plugin \(com.sn\_prd\_pm\) must be active. See [Plugins installed with Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-requirements.md).

Define the characteristic for the test group. See [Define a characteristic for a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-characteristic-for-test-group.md).

Define the characteristic of the test definition that receives the inherited value. The test definition must be in the Draft state. See [Define a characteristic for the test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/add-characterisitc-for-test-specification.md).

Role required: sn\_st\_mgmt.test\_def\_creator

## About this task

You create each mapping yourself. The system doesn't create mappings automatically.

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Definitions** &gt; **All**.

2.  Select the draft test definition that you want to open.

3.  In the Test Characteristic Attribute Mapping related list, select **New**.

    The system fills in the **Test definition** field.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Test definition|Test definition that inherits the characteristic.|
    |Source group characteristic|Characteristic of the test group that you want the test definition to inherit. The list shows only characteristics that belong to a test group.|
    |Target definition characteristic|Characteristic that belongs to the selected test definition and receives the inherited value. The list shows only characteristics of the selected test definition that no other mapping in the same test group already uses.|

    **Note:** You can create only one mapping for the same test definition and source characteristic. If you map a target characteristic that another mapping in the same test group already uses, the system doesn't save the record.

5.  Select **Submit**.


## Result

The test definition inherits the characteristic from the test group. To stop inheriting it, delete the mapping.

## What to do next

To define test decomposition rules for a test definition in the test group, see [Define a test decomposition rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-test-decomposition-rule.md).

If the test group is in the Draft state, publish it when it is ready. See [Publish a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/publish-test-groups.md).

