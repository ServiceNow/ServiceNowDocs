---
title: Configure properties for schedule adherence and conformance
description: Configure schedule adherence properties to calculate the adherence and conformance of your agents so that you can improve the operational efficiency of your organization.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Schedule Adherence in Workforce Optimization for ITSM, Scheduling in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Configure properties for schedule adherence and conformance

Configure schedule adherence properties to calculate the adherence and conformance of your agents so that you can improve the operational efficiency of your organization.

## Before you begin

Role required: admin

## About this task

The threshold settings for adherence and conformance indicate how many minutes early or late an agent can clock in or clock out to a scheduled work shift without being considered as non-adherent.

## Procedure

1.  Navigate to **All** &gt; **Shift Planning** &gt; **Schedule Adherence** &gt; **Settings**

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Enable Schedule Adherence|Calculation and information about the agents' adherence to the schedules.|
    |Threshold for early checkin for planned shift \(in Minutes\)|Time that you can set for early check in. This time is the acceptable time for an agent to start the work shift before the actual shift time. The default value is 60 minutes. For example, if an agent's planned work shift is 8 a.m. to 5 p.m. and the agent clocks in at 7 a.m., the threshold time allows flexibility and the agent is not considered as a non-adherent agent.|
    |Threshold for adherence% of Time Worked Summary|Percentage that you can set for a threshold in adherence. The agents who do not qualify to be above the defined threshold value \(70%\) are considered non-adherent agents.|
    |Lower threshold conformance % of Time Worked Summary|Lower threshold percentage that you can set for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered as non-conformant agents. The default value is 80%.|
    |Upper threshold for conformance % of Time Worked Summary|Upper threshold percentage that you can set for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered as non-conformant agents. The default value is 120%.|
    |Default threshold time for clock-out event generation \(in Minutes\)|Default threshold time to generate an automatic clock-out event if an agent fails to clock out. The default value is 60 minutes. For example, if an agent's planned work shift is 8 a.m. to 5 p.m. and the agent fails to clock out at 5 p.m., the system waits for 60 minutes as the threshold time and generates an automatic clock-out event.|

3.  Click **Save**.


**Parent Topic:**[Schedule Adherence in Workforce Optimization for ITSM](../concept/schedule-adherence-configurable-itsm.md)

**Related topics**  


[Schedule Adherence in Workforce Optimization for ITSM](../concept/schedule-adherence-configurable-itsm.md)

