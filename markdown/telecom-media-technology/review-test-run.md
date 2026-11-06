---
title: Review a test run
description: Check the state and result of a test run, the test definition and test group run that it belongs to, and the test measures that it captured.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/review-test-run.html
release: australia
topic_type: task
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [test run, test run result]
breadcrumb: [Use, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Review a test run

Check the state and result of a test run, the test definition and test group run that it belongs to, and the test measures that it captured.

## Before you begin

Role required: sn\_st\_mgmt.test\_viewer

## About this task

Test runs are normally created and updated by an external system. See [Test run in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-run-stm.md).

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Runs** &gt; **All**.

    To see only some test runs, open one of the filtered lists under **Test Runs**, such as **In progress**, **Completed**, or **Scheduled**. The **Scheduled** list shows test runs in the Acknowledged state.

2.  Select the test run that you want to open.

3.  Check the **State** and **Result** fields.

    For the values, see [States and choice values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-states-choices.md).

4.  Check the test definition and the test group run that the test run belongs to.

5.  In the Test Measures related list, review the test measures that the test run captured.

    Each test measure shows its value and a summary of the rule violations that it raised. To read a test measure in detail, see [Review the test measures of a test run](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/review-test-measures.md).


## What to do next

If a test measure raised violations, review them. See [Review threshold rule violations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/review-threshold-rule-violations.md).

