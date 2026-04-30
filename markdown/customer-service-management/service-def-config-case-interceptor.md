---
title: Add a case type to the Case interceptor
description: In the Core UI, the Case interceptor lists the types of customer service cases that an agent can create. If you create a case type and you want that case type to appear in the Case interceptor, you need to add it to the Case interceptor configuration.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring service definitions, Service definitions, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Add a case type to the Case interceptor

In the Core UI, the Case interceptor lists the types of customer service cases that an agent can create. If you create a case type and you want that case type to appear in the Case interceptor, you need to add it to the Case interceptor configuration.

## Before you begin

Role required: sn\_csm\_case\_types.service\_definition\_admin or admin

## About this task

When an agent creates a case, they can select the case type from the Case interceptor.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Interceptors**.

2.  Select the Case interceptor from the Interceptors list.

3.  In the Answers related list, select **New**.

4.  Select **Simple questions to redirect the URL**.

5.  Fill in the fields on the Answer form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name for the case type. For example, Complaint.|
    |User Prompt|The description that the agent sees in the interceptor when they create a case.|
    |Target URL|The target URL of the form view that should open for the selected case type.|
    |Order|The order in which the case type appears in the interceptor.|

6.  Select **Submit**.


