---
title: Discover datacenters only for new cloud accounts
description: If you have multiple cloud accounts and datacenters in AWS and Azure, you can discover datacenters for new cloud accounts only, instead of refreshing the entire list.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Discover datacenters only for new cloud accounts

If you have multiple cloud accounts and datacenters in AWS and Azure, you can discover datacenters for new cloud accounts only, instead of refreshing the entire list.

## Before you begin

-   Verify that you're using at least Zurich Patch 2.
-   Verify that the **glide.discovery.cdu.auto\_refresh\_sub\_accounts\_and\_ldcs** system property is set to true. For more information, see [Create Discovery schedules for cloud resources](../../discovery/concept/discovery-manager.md#).

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the **Name** column, search for `cloud.discovery.refresh_datacenter_for_new_member_account`.

3.  Select the **cloud.discovery.refresh\_datacenter\_for\_new\_member\_account** property.

4.  In the **Value** field, enter **true**.

5.  Select **Update**.


## What to do next

Either execute discovery immediately or wait until the predefined schedule triggers the discovery. For more information, see [Create a discovery schedule in Cloud Discovery Workspace](../../discovery/task/cloud-operations-disco-create-schedule.md).

**Parent Topic:**[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

**Previous topic:**[Activate a disabled pattern](activate-disabled-pattern.md)

**Next topic:**[Improved query performance with direct field population in CI tables](../concept/query-service-account-ldc-fields.md)

**Related topics**  


[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

[Microsoft Azure Cloud discovery using patterns](../reference/azure-cloud-discovery-patterns.md)

