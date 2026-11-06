---
title: Review a test group run
description: Check the state of a test group run and the test runs that it produced.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/review-test-group-run.html
release: australia
topic_type: task
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [test group run, test group run state]
breadcrumb: [Use, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Review a test group run

Check the state of a test group run and the test runs that it produced.

## Before you begin

Role required: sn\_st\_mgmt.test\_viewer

## About this task

A test group run is one execution of a test group. It contains the test runs for the test definitions in the group. For more information, see [Test group run in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-run-initiation.md).

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Runs** &gt; **All**.

2.  In the filter, type **sn\_st\_mgmt\_test\_group\_run.list**.

3.  Open the test group run record.

4.  Check the **State** and the scheduled date.

    For the values, see [States and choice values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-states-choices.md).

5.  Check the test group that the test group run executes, and the linked diagnostic task.

6.  In the Test Runs related list, review the test runs that belong to the test group run.

    To review one, see [Review a test run](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/review-test-run.md).


## What to do next

With the Product Model plugin, the characteristics that appear on a test group run depend on how the test group characteristics are mapped. See [Test group run characteristics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-group-run-characteristics.md).

