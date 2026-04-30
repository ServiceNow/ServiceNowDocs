---
title: Explicit Roles in Supplier Lifecycle Operations
description: You can grant access to your instance to both internal and external users. However, it is important to differentiate their access levels for added security. To achieve this, every user must have at least one role, allowing the instance to distinguish between internal and external users.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Explicit Roles in Supplier Lifecycle Operations

You can grant access to your instance to both internal and external users. However, it is important to differentiate their access levels for added security. To achieve this, every user must have at least one role, allowing the instance to distinguish between internal and external users.

As of the Paris release, no user can simultaneously have the explicit roles snc\_internal and snc\_external. The ServiceNow AI Platform applies this mutual exclusion everywhere in the system and writes error messages to the logs for each conflict.

Groups and role containment structures also cannot include both roles, as this would result in any group member or user assigned to such a group or role automatically holding both roles. The ServiceNow AI Platform aborts any operation that would create such a scenario.

You must install the Explicit Roles \[com.glide.explicit\_roles\] plugin while installing Supplier Lifecycle Operations. Supplier Lifecycle Operations is dependent on the Explicit Roles \[com.glide.explicit\_roles\] plugin.

For more information about ServiceNow AI Platform explicit roles, see [Explicit Roles](https://www.servicenow.com/docs/access?context=explicit-roles&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

**Parent Topic:**[Install Supplier Lifecycle Operations](../task/install-supp-mgmt.md)

