---
title: Create a test group
description: Create a test group to group related service tests, such as speed and ping tests, to streamline diagnostics for specific service types or product models in Service Test Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/create-test-group.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Setting up a test group, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Create a test group

Create a test group to group related service tests, such as speed and ping tests, to streamline diagnostics for specific service types or product models in Service Test Management.

## Before you begin

To create an automated test group, create the flow that the test group runs. For more details, see [Create a flow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/create-flow.md) and [Service Test Management automation framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-automation-framework.md).

Create the test definitions that you want to add to the test group. A test definition must be in the Draft or Published state. For more details, see [Create a test definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/create-test-specification.md).

Role required: sn\_st\_mgmt.test\_def\_creator

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Groups** &gt; **All**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For more information about the fields, see [Service Test Group form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-fields.md).

4.  Select **Submit**.


## What to do next

For a manual test group, add the test definitions that the test group runs. For more details, see [Map test definitions to a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/add-test-definitions-to-test-group.md).

Publish the test group. For more details, see [Publish a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/publish-test-groups.md).

