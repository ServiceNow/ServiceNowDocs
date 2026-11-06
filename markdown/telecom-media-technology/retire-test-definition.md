---
title: Retire test definitions
description: Retire published test definitions that you no longer use, so that new test runs can't reference them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/retire-test-definition.html
release: australia
topic_type: task
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [retire test definition, test definition state]
breadcrumb: [Setting up test definitions, Setting up test configuration records, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Retire test definitions

Retire published test definitions that you no longer use, so that new test runs can't reference them.

## Before you begin

The test definitions must be in the Published state.

Role required: sn\_st\_mgmt.test\_def\_manager

## About this task

A retired test definition can't be changed, and it can't return to an earlier state. See [Test definitions in Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/test-definition-stm.md). You can retire one test definition from its form, or several from the list.

## Procedure

1.  Navigate to **All** &gt; **Service Test Management** &gt; **Test Definitions** &gt; **All**.

2.  Retire the test definitions.

    -   To retire one test definition, open it, select **Retire**, and then confirm.
    -   To retire several test definitions, select the check box for each one. In the list actions, select **Retire**, and then confirm.

## Result

The state of each test definition changes from Published to Retired.

A test definition linked to a published test definition as a related test definition can't be retired. On the form, an error appears. From the list, the others are retired and a message lists the skipped definitions. In this case, remove the relationship first. See [Define the relationship between the test definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/define-test-spec-relationship.md).

## What to do next

To archive retired test definitions, see [Archive test definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/archive-test-definitions.md).

