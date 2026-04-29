---
title: Viewing resource quota limits
description: View quota limits to see how many resources you have consumed and how many you can provision based on quota limits set for you and your user group.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Launch a stack, Cloud User Portal, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Viewing resource quota limits

View quota limits to see how many resources you have consumed and how many you can provision based on quota limits set for you and your user group.

## Allocated and consumed quota limits

To see the quota you have consumed for provisioning resources compared to the maximum quota limit allocated to you, navigate to the Overview page. The following predefined resource types in the system might have quota limits set for you and the user groups to which you belong:

-   Stack Count
-   VM Count
-   vCPUs Count
-   Storage Volume Size
-   Network Count

**Note:** The Stack Count is a default base system quota limit available beginning with the Australia release. It is displayed on the Overview page if your Cloud Provisioning and Governance administrator has set a Stack Count quota for you or your user group.

The Quota section on the Overview page displays the quota limits in a graph.

-   Green indicates that sufficient resources are available.
-   Red indicates that insufficient resources are available.
-   If quota limits have been exceeded, the system might either display an error message or trigger a policy-based approval when you attempt to provision a stack. For more information, see [Provisioning stacks based on quota limits](quota-template-based-stacks.md).

The quota limit that is displayed on the Quota section is an aggregate from all of the user groups to which you belong. To view quota limits separately for you and each of your user groups, click **View All**. The Quota Details pop-up window is displayed.

![Quota details for user and user groups.](../image/quota-details.png "Quota Details pop-up window")

The Quota Details pop-up window indicates your consumed quota compared to your allocated quota limit for each resource type. For example, 0/5 for a resource type means that zero has been consumed and five is the allocated quota limit.

The quota limit for a resource type appears as either a sum or count. For example, the Storage Volume Size is shown as a sum in GB and the VM Count is shown as a number.

You can also view quota limits when launching stacks. For more information, see [Launch a stack](../task/cloudmgt-launch-stack.md).

