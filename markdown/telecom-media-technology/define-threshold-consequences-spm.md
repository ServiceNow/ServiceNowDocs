---
title: Define measure consequences for the threshold rules
description: Set actions or responses to trigger when the test measure results fall outside the predefined acceptable limits.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/define-threshold-consequences-spm.html
release: australia
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [measure consequence, prescribed action, repeat action]
breadcrumb: [Setting up test definitions, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Define measure consequences for the threshold rules

Set actions or responses to trigger when the test measure results fall outside the predefined acceptable limits.

## Before you begin

The test definition must be in the Draft state, and it must have at least one threshold rule. See [Define threshold rules for a test measure definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-threshold-rules.md).

Role required: sn\_st\_mgmt.test\_def\_creator

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Definitions** &gt; **All**.

2.  Select the test definition that you want to open.

3.  In the Threshold Rules related list, select the threshold rule that you want to define a consequence.

4.  In the Measure Consequences related list, select **New**.

5.  On the form, fill in the fields.

    For the field descriptions, see [Measure Consequence form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/measure-consequence-fields.md).

6.  Select **Submit**.


## Result

When a test measure breaks the threshold rule, the system can apply the consequence and record an applied consequence. See [Review applied consequences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/review-applied-consequences.md).

