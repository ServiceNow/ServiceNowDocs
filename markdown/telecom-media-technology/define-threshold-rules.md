---
title: Define threshold rules for a test measure definition
description: Set the limits for a test measure definition that a captured value is checked against. When a value breaks a limit, the system records a threshold rule violation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/define-threshold-rules.html
release: australia
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [threshold rule, conformance target, severity, tolerance period]
breadcrumb: [Setting up test definitions, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Define threshold rules for a test measure definition

Set the limits for a test measure definition that a captured value is checked against. When a value breaks a limit, the system records a threshold rule violation.

## Before you begin

The test definition must be in the Draft state, and it must have at least one test measure definition. See [Define test measure definitions for a service test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-test-measure-spm.md).

Role required: sn\_st\_mgmt.test\_def\_creator

## About this task

Each threshold rule belongs to one test measure definition, so you create it from that test measure definition. A rule can compare the captured value against a single exact value, or against a lower limit, an upper limit, or both.

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Definitions** &gt; **All**.

2.  Select the test definition that you want to open.

3.  In the Test Measure Definitions related list, select the test measure definition that you want to define a rule for.

4.  In the Threshold Rules related list, select **New**.

5.  On the form, fill in the fields.

    For the field descriptions and the rules that govern which comparators and targets you can combine, see [Threshold Rule form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/threshold-rule-fields.md).

6.  7.  Select **Submit**.


## What to do next

Define the action to take when the rule is broken. See [Define measure consequences for the threshold rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-threshold-consequences-spm.md).

