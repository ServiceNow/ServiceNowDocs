---
title: Map test definitions to a test group
description: Map test definitions to a draft test group and set the order in which they run.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/add-test-definitions-to-test-group.html
release: australia
topic_type: task
last_updated: "2026-10-13"
reading_time_minutes: 2
keywords: [test group to definition mapping, add test definition, test group order]
breadcrumb: [Setting up a test group, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Map test definitions to a test group

Map test definitions to a draft test group and set the order in which they run.

## Before you begin

The test group must be in the Draft state.

Role required: sn\_st\_mgmt.test\_def\_creator

## About this task

A manual test group needs at least one test definition before you can publish it. After the test group is published, you can't change its mappings.

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select the draft test group that you want to open.

3.  In the Test Group To Definition Mapping related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Test definition|Test definition to add to the test group. Select a definition that is in the Draft or Published state.|
    |Order|Order in which the test definition runs within the test group. Required.|
    |Active|Option that includes the test definition when the test group runs. Selected by default.|

    **Note:** You can map a test definition to a test group only once. If you map it again, the system shows an error.

5.  Select **Submit**.


## What to do next

To enable the test definitions to inherit characteristics from the test group, define the group characteristics before you publish the test group. You can't add or change group characteristics after the test group is published. This requires the Product Model plugin. For more information, see [Define a characteristic for a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-characteristic-for-test-group.md).

Map the group characteristics to the test definitions. You can do this while each test definition is in the Draft state. For more information, see [Map a test group characteristic to a test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/map-test-group-characteristics-to-test-definition.md).

To define test decomposition rules for a test definition in the test group, see [Define a test decomposition rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-test-decomposition-rule.md).

When the test group is ready, publish it. See [Publish a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/publish-test-groups.md).

**Related topics**  


[Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md)

[Test groups in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-stm.md)

