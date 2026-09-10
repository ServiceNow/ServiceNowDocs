---
title: Set up usage tracking by user and department
description: Add user email and department information to the User table so that the AI Control Tower can break down usage and cost by user and by department.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Set up usage tracking by user and department

Add user email and department information to the User table so that the AI Control Tower can break down usage and cost by user and by department.

## Before you begin

Role required: sn\_ai\_governance\_ai\_steward

## About this task

Usage by user and department is available for ServiceNow and the Anthropic service. The usage by user and department widget shows the cost breakdown by user and by department. For ServiceNow, the AI Control Tower reads user consumption and maps each user to a department through the User table. For the Anthropic service, it maps the usage email address to a User record, and then reads the user name and department from that record.

## Procedure

1.  Navigate to **Insights** &gt; **Value** and review the usage by user and department widget.

2.  For a user who has no record in the User \[sys\_user\] table, create the user record with the email address.

3.  For a user with a missing department, add the department in the User \[sys\_user\] table.

    When email or department information is missing, you will see a message. The message indicates that information may be unavailable for some users and prompts you to update the email and department details in the User table.

4.  Run the sync to pick up the new records.

    The sync job runs every four hours and picks up newly created records.


## Result

The usage by user and department widget shows usage and cost broken down by user and by department.

