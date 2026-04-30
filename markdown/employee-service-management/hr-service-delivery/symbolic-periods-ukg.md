---
title: Set up symbolic periods
description: By default, the symbolic periods of Ultimate Kronos Group application are set up when you activate the HR Service Delivery Integration with Ultimate Kronos Group application. Symbolic periods denote the time periods that are identifiable by the Ultimate Kronos Group application.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring HR Service Delivery with Ultimate Kronos Group, HR Service Delivery with Ultimate Kronos Group, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Set up symbolic periods

By default, the symbolic periods of Ultimate Kronos Group application are set up when you activate the HR Service Delivery Integration with Ultimate Kronos Group application. Symbolic periods denote the time periods that are identifiable by the Ultimate Kronos Group application.

## Before you begin

Role required: sn\_hr\_ukg.admin

## About this task

When an employee posts a question in virtual chat in Employee Center, an [NLU model](nlu-ukg-model.md) selects an utterance from the question, checks for its mention in vocabulary sources, identifies its symbolic code and ID. A flow uses the ID to pull the requested information from the Ultimate Kronos Group application and display in virtual chat in Employee Center.

## Procedure

1.  If you have made any modifications to the symbolic periods in Ultimate Kronos Group:

    1.  Navigate to **HR UKG Integrations** &gt; **Symbolic periods** and click**Refresh Symbolic Periods.**
    2.  Navigate to **NLU Workbench** &gt; **Vocabulary sources**, and synchronize **@UKGTimeKeepingSymbolicPeriod**.
    3.  Navigate to**NLU Workbench** &gt; **Models**, select **UKG Topics Model**, and click **Train**.

