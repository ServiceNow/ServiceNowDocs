---
title: Set up the Importance and Impact Tolerance Rating Scale
description: Set up the Importance and Impact Tolerance Rating Scale in the Operational Resilience application so that you can define new parameters for your business services.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Completing general administrative tasks, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Set up the Importance and Impact Tolerance Rating Scale

Set up the Importance and Impact Tolerance Rating Scale in the Operational Resilience application so that you can define new parameters for your business services.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

Define new parameters such as importance, impact tolerance, impact tolerance icon and its color, minimum and maximum tolerance value, and the tolerance order for your business service. When the options in the sn\_grc\_choice table are set as **choice\_category=opres\_asmt\_rating** and **set=operational\_resilience**, the Operational Resilience application delivers the following default importance rating scales. This task is optional.

|Importance|Impact tolerance|Impact tolerance icon|Minimum-maximum score|Order|
|----------|----------------|---------------------|---------------------|-----|
|1—Most critical|1 Day|flag-fill|76—100|10|
|2— Somewhat critical|2 Days|triangle-exclamation-fill|51—75|20|
|3—Less critical|3 Days|binoculars-fill|26—50|30|
|4—Not critical|4 Days|circle-check-fill|0—25|40|

When a new questionnaire template is created, the application clones the default rating scale to it​.

A user with the sn\_oper\_res.admin role can change the rating scale for the individual templates.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Admin** &gt; **Importance and Impact Tolerance Rating Scale**.

    You see the default importance and impact tolerance rating scales as shown in the following example.

    ![Importance and Impact Tolerance Rating Scales module.](../image/importance-and-impact-rating-scale-module.png "Importance and Impact Tolerance Rating Scales module")

2.  Click **New**.

    You can define new parameters such as the importance, impact tolerance, impact tolerance icon and its color, minimum and maximum tolerance value, and the tolerance order for your business service.

3.  On the form, fill in the fields and click **Submit**.

    For a description of the field values on the Rating Scale New Record form, see [Rating Scale New Record form](../reference/importance-and-impact-rating-scale-reference.md).


