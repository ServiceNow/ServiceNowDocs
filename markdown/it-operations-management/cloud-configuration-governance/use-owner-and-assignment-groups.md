---
title: Use owner and assignment groups
description: You must set up and use the user groups in Cloud Provisioning and Governance as a part of the day-2 task.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Additional Cloud Provisioning and Governance setup on day 2, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Use owner and assignment groups

You must set up and use the user groups in Cloud Provisioning and Governance as a part of the day-2 task.

## Before you begin

Role required: admin

## About this task

Owner group- This is used in quota management. During any stack provision, the user must select the "User group" on the order form. A quota check is performed based on the user group selected on the form, and this user group is later added as the stack 'Owner group' in the sn\_cmp\_stack table. Quota checks can be defined at the user group level. For more details, see [Quotas and resource order controls](../../cloud-management-v2/concept/quotas.md).

**Note:** If the stack is deleted or the owner group field changes for the stack, the quota is recalculated. The quota is recalculated in the business rule: Recalc Consumed Quota on Stack Update.

Assign group- The discovery schedule runs bring the resources created from other instances into your instance. These resources are unmanaged. Similarly, the 'Fill in tag assignments' scheduled job creates unmanaged stacks. To manage these stacks and resources, you can assign a change group to them.

Assign a change group to an unmanaged stack or resource, to make it visible in the **Cloud User Portal**, enabling you to perform day 2 operations on this resource.

## Procedure

1.  Navigate to **Cloud User Portal**.

2.  Click **View Stacks** and navigate to **Discovered Stacks** for unmanaged stacks.

3.  Click **View Resources** and navigate to **Virtual Machines**for unmanaged resources.

4.  Change the view to **My Groups**.

5.  Select any of the virtual machines and perform day 2 operation.


**Parent Topic:**[Additional Cloud Provisioning and Governance setup on day 2](cloud-mgt-general-setup-day-2.md)

