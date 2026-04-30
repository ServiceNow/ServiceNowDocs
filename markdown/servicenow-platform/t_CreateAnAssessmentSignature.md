---
title: Create an assessment signature
description: A signature on an assessment questionnaire contains assertions that can communicate directions, a legal statement, or any text that you want the recipient to consider.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Metric types and assessable records, Create an assessment metric for a category, Assessment metrics, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an assessment signature

A signature on an assessment questionnaire contains assertions that can communicate directions, a legal statement, or any text that you want the recipient to consider.

## Before you begin

Role required: assessment\_admin or admin

## About this task

You can require the recipient to select a check box or provide a full signature to acknowledge acceptance of the assertion before submitting the form. You can display assertions without requiring a signature. An assessment property called **Require authentication for user signature** allows you to require users to provide their user name and password when an assessment asks for a full name signature.

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Metric Definition** &gt; **Signatures**.

    All signatures in the system appear in this list.

2.  Click **New**.

3.  Complete and submit the form using the fields in the table.

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive name for this signature|
    |Signature type|Type of signature required. The selections are **Checkbox**, **Full name**, or **Assertion only**. If **Assertion only** is selected, no signature is required to submit the questionnaire. By default, the system requires user authentication for a full name entry.|
    |Assertion|Text to present to recipients that requires acknowledgement.|


**Parent Topic:**[Metric types and assessable records](../concept/c_MetricTypesAndAssessableRecords.md)

