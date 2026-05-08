---
title: Business hour scheduling
description: You can set up business hour scheduling on all virtual machines in a stack. Business hour scheduling can be set up on stacks at the time of provisioning or on existing stacks.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Cloud User Portal, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Business hour scheduling

You can set up business hour scheduling on all virtual machines in a stack. Business hour scheduling can be set up on stacks at the time of provisioning or on existing stacks.

Schedules can be set for when a stack should be started, stopped, and/or deprovisioned by defining parameters such as business hours, holidays, long weekends.

**Note:** For Google Deployment Manager \(GDM\) based template catalog, business hour scheduling and stack level operations are not supported.

The administrator can create schedule profiles in the **Cloud Admin Portal**. See [Resource Profiles](../../cloud-management-v2/concept/cloud-resource-profiles.md).

While provisioning a stack in the Cloud User Portal, use the **Schedule Profile** list to select a profile that has already been created by the administrator. Select a time zone in the **Schedule Time Zone** list which defaults to your system's time zone and indicates the time zone in which the schedule’s business hour time frames are enforced.

You can also define the lease end dates for a stack during provision. The lease end date for a stack can be modified at any time. See [Modify the lease for a stack](../task/cloudmgmt-extend-stack-lease.md).

Once you provision a stack with a schedule and/or lease dates, a series of operations \(start, stop, deprovision\) occur at the appropriate time set by you. You can skip a business schedule operation or cancel the business schedule operations associated with a stack. See [Modify business schedule operations for a stack](../task/cloudmgmt-modify-business-schedule.md).

