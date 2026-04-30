---
title: Create an improvement request
description: Create an improvement request for improvement opportunities you identify in your environment. Once submitted, the improvement request is analyzed and implemented by the Improvement Manager and Improvement Coordinator.
locale: en-US
release: zurich
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Requesting improvements, Continual Improvement Management, IT Service Management]
---

# Create an improvement request

Create an improvement request for improvement opportunities you identify in your environment. Once submitted, the improvement request is analyzed and implemented by the Improvement Manager and Improvement Coordinator.

## Before you begin

Role required: sn\_cim.improvement\_requester

## Procedure

1.  Identify an opportunity for improvement.

    Any type of improvement identified in your company qualifies as the basis for an improvement request. For example, KPI performance, customer satisfaction, resources, processes, training, to name a few.

2.  Determine your improvement goal.

    The improvement goal is the expected result to be achieved from the improvement.

3.  Submit an improvement request.

    1.  Navigate to **Continual Improvement** &gt; **Create New**.

        A CIM phase is automatically created when you create the initiative, if the **sn\_cim.create\_default\_phase** system property is enabled. For more information, see [Properties installed with Continual Improvement Management](../reference/cim-components.md).

    2.  Fill in the short description and the business justification, and select **Submit**.

        The improvement request is created and set to **New** for the Improvement Manager to accept or reject based on alignment with strategic objectives.

4.  To track the status of your improvement request, navigate to **Continual Improvement** &gt; **My CIM Requests**.


## Create improvement request

In the process of reviewing KPI performance in the Performance Analytics application, the incident manager noticed the **Average time to resolve an incident** KPI scorecard was too high \(24 hours\).

As part of the improvement identification process, the incident manager analyzed the KPI performance by comparing it with values from other companies using the Benchmarks application, determined an improvement was needed, and set a target goal.

|Field|Value|
|-----|-----|
|Number|CIM0000135 \(set internally\)|
|Business service|IT Services|
|Business process|Incident Management|
|Short description|\(Required\) Improve average time to resolve an incident by 25%|
|Business justification|A comparison with global values from companies in the same industry using the Benchmarks application shows that average incident resolution time is lower than the industry average.|
|State|New|
|Priority|4 - Low \(default\)|

**Parent Topic:**[Requesting improvements](../concept/cim-improvement-request.md)

**Related topics**  


[Improvement field descriptions](../reference/cim-field-descriptions.md)

