---
title: Map a role level to the employee profile
description: Mapping a role level to the employee is a critical step that links the job architecture data with the employee data in your organization, which enables you to track the skills of the employee.
locale: en-US
release: australia
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Skills Foundation, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Map a role level to the employee profile

Mapping a role level to the employee is a critical step that links the job architecture data with the employee data in your organization, which enables you to track the skills of the employee.

## About this task

The standard method to assign a role level is to create a Proactive Prompts configuration that is triggered when the job architecture tables are loaded and checks whether employees have one or more relevant role levels based on employee profiles and job profiles.

-   If an employee has more than one role level, a prompt with a list of relevant roles is sent to the employee. The employee selects suitable role levels from the list that are then added to the employee's profile.
-   If an employee has a single relevant role, a scheduled job triggered in set intervals that checks for employees who do not have a primary role assigned automatically attaches the primary role to the employee profile.

This procedure describes how to run this scheduled job on demand.

## Before you begin

Role required: sn\_skills\_int.job\_arch\_admin, sn\_skills\_int.admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and select the **Attach unique role levels to employees** scheduled job.

3.  Select **Execute Now** button to run the job.


## Result

The primary role of employees with a single role level are updated automatically in their profiles.

