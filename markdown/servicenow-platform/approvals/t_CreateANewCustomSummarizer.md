---
title: Create a new custom approval summarizer
description: After you add a new table that has approvals to an instance, you can add a custom activity formatter by creating a new UI macro and then add it to the appropriate form.
locale: en-US
release: australia
product: Approvals
classification: approvals
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Summarizers, Approval summarizer formatter, Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a new custom approval summarizer

After you add a new table that has approvals to an instance, you can add a custom activity formatter by creating a new UI macro and then add it to the appropriate form.

## Before you begin

Role required: admin

## About this task

approval\_summarizer can only be used on approval forms in the global scope.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Macros**

2.  Click **New**.

3.  Give the macro a name that follows the summarizer naming convention: `approval_summarizer_<tablename>`

4.  Complete the rest of the form and click **Submit**.

5.  Create a formatter and add it to a form and add it to the appropriate form.

    To learn more about activity formatters, see Activity formatter.


**Parent Topic:**[Summarizers](../concept/c_Summarizers.md)

