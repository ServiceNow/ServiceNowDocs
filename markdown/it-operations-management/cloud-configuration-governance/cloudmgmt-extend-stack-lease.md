---
title: Modify the lease for a stack
description: When a stack reaches the end of its lease, the system notifies the stack owner and deprovisions the stack. You can modify the lease for a stack before it approaches its end date.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business hour scheduling, Cloud User Portal, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Modify the lease for a stack

When a stack reaches the end of its lease, the system notifies the stack owner and deprovisions the stack. You can modify the lease for a stack before it approaches its end date.

## Before you begin

Role required: sn\_cmp.cloud\_service\_user

## About this task

A lease end date is assigned to all provisioned stacks. A built-in policy titled **Lease End ServiceNow** with an **on Lease end** policy trigger has rules defining notifications and operations that are performed before, at, and after the end date of the lease. Lease dates can be modified for active stacks. The system sends a notification to the stack owner one day prior to the end of the lease. On the day the lease ends, the system stops the stack and sends another notification. Seven days after the lease has ended, the stack is terminated and a final notification is sent to the stack owner. You can modify the actions taken and the timings of these actions by modifying the **Lease End ServiceNow** policy. You can modify the default lease duration for all new stacks, going forward, by modifying the associated action script in the **Scheduling Defaults** built-in policy.

## Procedure

1.  Navigate to **All** &gt; **Overview** &gt; **View Activities**, then select **Lease Operations**.

    A list of stacks with upcoming lease-related operations is displayed.

2.  Click the **Select Action** list associated with the stack and then select **Modify Lease**.

    The **Modify Lease** option is also available from the stack details list in **Manage Stacks**.

3.  Set a new date and time for the lease to expire and then click **OK**.


