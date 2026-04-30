---
title: Activate an HR flow
description: HR flows help automate task and case creation.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [HR flows and triggers, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Activate an HR flow

HR flows help automate task and case creation.

## Before you begin

Role required: admin

## About this task

There are three HR flows installed with the Human Resources: Core application.

-   New Hire on Boarding Case Trigger HR Profile
-   New Hire on Boarding Case Trigger Job
-   Case Trigger Custom Condition

Activation is immediate. These flows create an HR case adding an entry in the HR Lifecycle Events Case \[sn\_hr\_le\_case\] table. If multiple flows are active at the same time, there is a high probability of creating duplicate records and cases.

**Note:** Only one of these flows should be active at any given time for a particular lifecycle event.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Open the flow you want to activate.

3.  Click the **Activate** button.


**Parent Topic:**[HR flows and triggers](../concept/hr-flows-and-triggers.md)

