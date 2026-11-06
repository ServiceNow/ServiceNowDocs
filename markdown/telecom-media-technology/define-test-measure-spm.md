---
title: Define test measure definitions for a service test
description: Define the values that a test captures, such as the metric, the unit, and how often the value is captured.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/define-test-measure-spm.html
release: australia
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [test measure definition, metric name, capture frequency]
breadcrumb: [Setting up test definitions, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Define test measure definitions for a service test

Define the values that a test captures, such as the metric, the unit, and how often the value is captured.

## Before you begin

The test definition must be in the Draft state.

Role required: sn\_st\_mgmt.test\_def\_creator

## About this task

Test measure definitions are optional. You can publish a test definition that has no test measure definitions.

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Definitions** &gt; **All**.

2.  Select the draft test definition that you want to open.

3.  In the Test Measure Definitions related list, select **New**.

4.  On the form, fill in the fields.

    For the field descriptions, see [Test Measure Definition form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-measure-definition-fields.md).

5.  Select **Submit**.


## What to do next

Set the limits that the captured value is checked against. Open the test measure definition that you created, and define a threshold rule from its Threshold Rules related list. See [Define threshold rules for a test measure definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-threshold-rules.md).

