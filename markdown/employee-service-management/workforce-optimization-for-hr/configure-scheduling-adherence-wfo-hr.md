---
title: Configure schedule adherence properties
description: Configure schedule adherence properties to calculate the adherence to improve the operational efficiency of your organization.
locale: en-US
release: zurich
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up Scheduling, Configure, Workforce Optimization overview, HR Service Delivery, Employee Service Management]
---

# Configure schedule adherence properties

Configure schedule adherence properties to calculate the adherence to improve the operational efficiency of your organization.

## Before you begin

Role required: sn\_hr\_wfo.admin

## About this task

The threshold settings for adherence and conformance indicate how many minutes early or late an agent can clock in or clock out to a scheduled work shift without being considered as non-adherent.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for HR** &gt; **Schedule Adherence** &gt; **Settings**

2.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Enable Schedule Adherence|Calculation and information about the agents' adherence to the schedules.|
    |Threshold for early checkin for planned shift \(in Minutes\)|Time set early check in. This time is the acceptable time for an agent to start the work shift before the actual shift time. The default value is 60 minutes. For example, if an agent's planned work shift is 8 a.m. to 5 p.m., and the agent clocks in at 7 a.m., the threshold time allows flexibility and the agent is not considered as a non-adherent agent.|
    |Threshold for adherence% of Time Worked Summary|Percentage set for a threshold in adherence. The agents who do not qualify to be above the defined threshold value \(70%\) are considered non-adherent agents.|
    |Lower threshold conformance % of Time Worked Summary|Lower threshold percentage set for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered as non-conformant agents. The default value is 80%.|
    |Upper threshold for conformance % of Time Worked Summary|Upper threshold percentage set for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered as non-conformant agents. The default value is 120%.|
    |Default threshold time for clock-out event generation \(in Minutes\)|Default threshold time to generate an automatic clock-out event if an agent fails to clock out. The default value is 60 minutes. For example, if an agent's planned work shift is 8 a.m. to 5 p.m. and the agent fails to clock out at 5 p.m., the system waits for 60 minutes as the threshold time and generates an automatic clock-out event.|

3.  Click **Save**.


**Parent Topic:**[Setting up Scheduling for Workforce Optimization for HR](setup-scheduling-wfo-hr.md)

