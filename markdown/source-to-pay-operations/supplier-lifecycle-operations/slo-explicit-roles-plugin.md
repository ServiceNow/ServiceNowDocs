---
title: Explicit Roles in Supplier Case Management
description: You can grant access to your instance to both internal and external users. However, it is important to differentiate their access levels for added security. To achieve this, every user must have at least one role, allowing the instance to distinguish between internal and external users.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Explicit Roles in Supplier Case Management

You can grant access to your instance to both internal and external users. However, it is important to differentiate their access levels for added security. To achieve this, every user must have at least one role, allowing the instance to distinguish between internal and external users.

As of the Paris release, no user can simultaneously have the explicit roles snc\_internal and snc\_external. The ServiceNow AI Platform applies this mutual exclusion everywhere in the system and writes error messages to the logs for each conflict.

Groups and role containment structures also cannot include both roles, as this would result in any group member or user assigned to such a group or role automatically holding both roles. The ServiceNow AI Platform aborts any operation that would create such a scenario.

You must install the Explicit Roles \[com.glide.explicit\_roles\] plugin while installing Supplier Case Management. Supplier Case Management is dependent on the Explicit Roles \[com.glide.explicit\_roles\] plugin.

For more information about ServiceNow AI Platform explicit roles, see [Explicit Roles](https://www.servicenow.com/docs/access?context=explicit-roles&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Parent Topic:**[Install Supplier Case Management](../task/install-supp-mgmt.md)

**Related topics**  


[Components installed with Supplier Case Management](../reference/installed-with-supp-mgmt.md)

[Application plugin installation sequence in Supplier Case Management](../reference/slm-plugin-list.md)

[Configure properties for Supplier Case Management](../reference/config-prop-supp-mgmt.md)

