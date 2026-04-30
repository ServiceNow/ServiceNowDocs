---
title: Set up accrual codes
description: Complete the one time set up of loading accrual codes from the Ultimate Kronos Group application into a ServiceNow application. Accrual codes help in pulling accrual leave balances of employees from the Ultimate Kronos Group application into a ServiceNow application.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, HR Service Delivery with Ultimate Kronos Group, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Set up accrual codes

Complete the one time set up of loading accrual codes from the Ultimate Kronos Group application into a ServiceNow application. Accrual codes help in pulling accrual leave balances of employees from the Ultimate Kronos Group application into a ServiceNow application.

## Before you begin

Role required: sn\_hr\_ukg.admin

## About this task

When an employee posts a question in virtual chat in Employee Center, the [NLU model](nlu-ukg-model.md) selects an utterance from the question, checks for its mention in vocabulary sources, identifies its accrual code and ID. A flow uses the ID to pull the requested information from the Ultimate Kronos Group application and display in virtual chat in Employee Center.

For example, an employee wants to view the accrual balance for annual leave. The NLU model selects annual leave as the utterance. It identifies **Annual Leave** as the accrual code whose ID in Ultimate Kronos Group is **1531**. The flow uses the ID **1531** to pull the requested information from the Ultimate Kronos Group application.

## Procedure

1.  If you have made any modifications to accrual periods in Ultimate Kronos Group:

    1.  Navigate to **HR UKG Integrations** &gt; **Accrual codes** and click **Refresh Accrual codes.**
    2.  Navigate to **NLU Workbench** &gt; **Vocabulary sources**, and synchronization **@AccrualCode**.
    3.  Navigate to**NLU Workbench** &gt; **Models**, select the **UKG Topics Model**, and click **Train**.

