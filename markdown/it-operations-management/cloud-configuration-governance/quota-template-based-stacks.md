---
title: Provisioning stacks based on quota limits
description: The system calculates the quota allocated to you and the user groups to which you belong when you provision stacks. If quota limits are exceeded, the system either displays an error message or triggers a policy-based approval.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Launch a stack, Cloud User Portal, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Provisioning stacks based on quota limits

The system calculates the quota allocated to you and the user groups to which you belong when you provision stacks. If quota limits are exceeded, the system either displays an error message or triggers a policy-based approval.

To view quota limits, navigate to the Overview page. For more information, see [Viewing resource quota limits](resource-quota.md).

## Quota calculation for template-based stacks

The Stack Count is a default base system quota limit available beginning with the Zurich release. It applies to all template-based stacks in the service catalog.

If your Cloud Provisioning and Governance administrator has set a Stack Count quota for you or your user group, the system calculates the stack number when you provision a template-based stack. After provisioning, the system increases the Stack Count quota by a value of 1 for each provisioned stack.

## Stack provisioning after exceeding quota limits

If the quota limit set for you or your user group has been exceeded, the system either displays an error message or triggers an assigned policy when you attempt to provision a stack.

-   If the system displays an error message indicating that the quota limit has been exceeded, you cannot provision the stack. If you think the quota limit should be increased, contact your Cloud Provisioning and Governance administrator.
-   If a policy is defined in the system for exceeding the quota limit, that policy is triggered. Based on the policy, the system raises an approval request or notification for increasing the quota limit. The request follows a predefined subflow in the system for approval. If the request is approved, the system deploys the stack.

![Policy triggered for provisioning a stack.](../image/policy-approval.png "Policy triggered for provisioning a stack after exceeding the quota limit")

