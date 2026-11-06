---
title: Review the test measures of a test run
description: Check the values that a test run captured and whether each value met the limits of its threshold rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/review-test-measures.html
release: australia
topic_type: task
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [test measure, metric]
breadcrumb: [Use, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Review the test measures of a test run

Check the values that a test run captured and whether each value met the limits of its threshold rules.

## Before you begin

Role required: sn\_st\_mgmt.test\_viewer

## About this task

A test measure is one value that a test captured during a test run. On each test measure, the application keeps a text summary that shows whether the measured value meets the limits stored on the violations of that measure. See [Recording test results and violations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/how-test-results-are-recorded.md).

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Runs** &gt; **All**.

2.  Open the test run.

3.  In the Test Measures related list, select the test measure that you want to open.

4.  Review the metric name, the metric description, the value, the unit of measure, and the accuracy.

5.  Check when and how the value was captured in the **Capture date time** and **Capture method** fields.

6.  Check the test measure definition that the test measure is based on, and the summary of rule violations.

    To see the limits that apply, open the test measure definition. See [Threshold Rule form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/threshold-rule-fields.md).


## What to do next

To review the violations that the test measure raised, see [Review threshold rule violations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/review-threshold-rule-violations.md).

