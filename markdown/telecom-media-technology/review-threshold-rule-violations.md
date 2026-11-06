---
title: Review threshold rule violations
description: Check which threshold rule a test measure broke, how severe the violation is, and the values that it was compared against.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/review-threshold-rule-violations.html
release: australia
topic_type: task
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [threshold rule violation, severity]
breadcrumb: [Use, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Review threshold rule violations

Check which threshold rule a test measure broke, how severe the violation is, and the values that it was compared against.

## Before you begin

Role required: sn\_st\_mgmt.test\_viewer

## About this task

The system records a threshold rule violation when a test measure breaks a threshold rule. Violations are normally sent by an external system. See [Recording test results and violations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/how-test-results-are-recorded.md).

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Runs** &gt; **All**.

2.  Open the test run.

3.  In the Test Measures related list, select the test measure that you want to see the violations.

4.  In the Threshold Rule Violations related list, select the violation that you want to open.

5.  Check the severity of the violation: High, Medium, or Low.

6.  Check the tolerance period, the number of allowed crossings, and the comparison values.

7.  Check the linked test measure and threshold rule.

    The threshold rule link might be empty on a violation that an external system created.

8.  In the Applied Consequences related list, review the consequences that the system applied.


## What to do next

To review an applied consequence, see [Review applied consequences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/review-applied-consequences.md).

**Related topics**  


[Recording test results and violations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/how-test-results-are-recorded.md)

