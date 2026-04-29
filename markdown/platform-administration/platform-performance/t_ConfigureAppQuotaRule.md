---
title: Configure an application quota rule
description: Configure an application quota rule to limit the number of events or jobs that can run in an application's scope within a specified time.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application quotas, Configure, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Configure an application quota rule

Configure an application quota rule to limit the number of events or jobs that can run in an application's scope within a specified time.

## Before you begin

Role required: admin

## About this task

You must be in the application scope of the application for which you want to create a rule.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Application Quota Rules**.

2.  Select **New**.

3.  On the Application Quota Rule form, fill in the fields.

    For a description of the field values, see [Application quota rule form](../reference/application-quota-rule-form.md).

4.  Set a condition to specify when the application quota rule should take effect.

    The application quota rule condition builder displays conditions that are only applicable to transactions. For a description of the condition builder options, see [Application quota condition builder](../reference/application-quota-condition-builder.md).

5.  Select **Submit**.


**Parent Topic:**[Maintaining and monitoring the ServiceNow AI Platform](../../general/concept/maintain-monitor-now-platform.md)

