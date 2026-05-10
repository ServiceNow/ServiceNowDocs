---
title: Explicit roles plugin
description: You can give both internal users and external users access to your instance. However, you might not want both types of users to have the same level of access. To provide added security, every user must have at least one role so that the instance can distinguish between internal and external users.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Supplier Collaboration Portal in APO, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Explicit roles plugin

You can give both internal users and external users access to your instance. However, you might not want both types of users to have the same level of access. To provide added security, every user must have at least one role so that the instance can distinguish between internal and external users.

As of the Paris release, no user can have both of the explicit roles \(snc\_internal and snc\_external\). Groups and role containment cannot include both roles, either, since that would cause any group member or user who is assigned to such a group or such a role to automatically have both roles. The ServiceNow AI Platform aborts any operation that would create such a scenario.

You must install the Explicit Roles \[com.glide.explicit\_roles\] plugin while installing Accounts Payable Operations. The Accounts Payable Operations plugin is dependent on the Explicit Roles \[com.glide.explicit\_roles\] plugin.

Before you install the Accounts Payable Operations plugin, you must perform comprehensive analysis of the Explicit Roles \[com.glide.explicit\_roles\] plugin configuration to avoid conflicts or adjustments; ensure seamless integration and operation of the plugins.

The installation of the Accounts Payable Operations plugin may cause access issues to the existing functionality that are controlled by the Explicit Roles \[com.glide.explicit\_roles\] plugin. You may have to manage or reconfigure certain roles and permissions managed by the Explicit Roles \[com.glide.explicit\_roles\] plugin for seamless integration and operation of existing functionalities. For more information on explicit roles, see [Explicit Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/explicit-roles.md).

**Parent Topic:**[Using Supplier Collaboration Portal in APO](using-supplier-collaboration-portal.md)

