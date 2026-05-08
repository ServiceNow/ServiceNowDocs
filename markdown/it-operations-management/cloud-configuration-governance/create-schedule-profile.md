---
title: Create a schedule profile
description: You map a schedule profile to an instance schedule. The schedule profile applies to all newly-provisioned resources that use the profile. For example, a schedule profile can specify the days of the week and times of day when a stack should start and stop.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resource Profiles, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a schedule profile

You map a schedule profile to an instance schedule. The schedule profile applies to all newly-provisioned resources that use the profile. For example, a schedule profile can specify the days of the week and times of day when a stack should start and stop.

## Before you begin

Role required: sn\_cmp.cloud\_admin

You must have a cloud account with datacenters. You must run Discovery on the service accounts to populate the datacenters.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Resource Profiles**.

2.  In the **Profiles** list, select **Schedule Profile**.

3.  Click **New**, enter a unique and descriptive **Name** and **Description**, fill in the form, and then click **Submit**.

<table id="table_n3n_zvt_ddb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schedule

</td><td>

Select an existing schedule or define a custom schedule. A schedule is a rule that includes or excludes specified time periods for actions. To define a schedule, use the **System Scheduler** module. See Define a schedule.

</td></tr><tr><td>

Multiplier

</td><td>

Auto-populated value between `0` and `1`: The fraction of time that a stack with this schedule is expected to be powered on.

</td></tr></tbody>
</table>
**Parent Topic:**[Resource Profiles](../concept/cloud-resource-profiles.md)

**Related topics**  


[Discover all datacenters in a service account on-demand](../../cloud-management-v2-setup/task/disco-datacntrs-in-srv-acct.md)

