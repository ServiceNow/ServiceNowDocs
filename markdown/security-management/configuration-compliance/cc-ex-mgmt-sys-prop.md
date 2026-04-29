---
title: Specify the duration of an exception requested for a remediation task
description: Use system properties to limit the duration for which an exception is requested for a remediation task. Remediation of the remediation task is deferred for the specified period.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Specify the duration of an exception requested for a remediation task

Use system properties to limit the duration for which an exception is requested for a remediation task. Remediation of the remediation task is deferred for the specified period.

## Before you begin

Role required: sn\_vulc.admin

## About this task

The `sn_vulc.exception_max_request_days` property is used to specify the maximum number of days for which an exception for a remediation task can be requested. The default value is 365 days.

**Note:** You can use the `sn_vulc.exception_approval_required` property to disable the exception approval work flow for the remediation task if it is not required. By default, this property is enabled and its value is `true`.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  On the System Properties page, search for `sn_vulc.exception_max_request_days`.

3.  Click on the property name to open the System Property record.

4.  To be able to edit this record, ensure that Configuration Compliance is selected as the current application.

5.  Enter a positive **Value** and click **Update**.

    The record is updated and saved.


