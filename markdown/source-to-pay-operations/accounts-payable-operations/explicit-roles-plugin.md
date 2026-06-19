---
title: Explicit roles plugin
description: Explicit roles in Accounts Payable Operations control data access for internal and external users, ensuring each user sees only information appropriate for their role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/explicit-roles-plugin.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 1
keywords: [Accounts Payable Operations, APO, invoice automation, AP automation, finance automation]
breadcrumb: [Using Supplier Collaboration Portal in APO, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Explicit roles plugin

Explicit roles in Accounts Payable Operations control data access for internal and external users, ensuring each user sees only information appropriate for their role.

As of the Paris release, no user can have both of the explicit roles \(snc\_internal and snc\_external\).

Groups and role containment can't include both roles, since that would cause any group member or user assigned to such a group or a role to automatically have both roles.

The ServiceNow AI Platform aborts any operation that would create such a scenario.

You must install the Explicit Roles \[com.glide.explicit\_roles\] plugin while installing Accounts Payable Operations. The Accounts Payable Operations plugin is dependent on the Explicit Roles \[com.glide.explicit\_roles\] plugin.

Before you install the Accounts Payable Operations plugin, you must perform comprehensive analysis of the Explicit Roles \[com.glide.explicit\_roles\] plugin configuration to avoid conflicts or adjustments. This confirms seamless integration and operation of the plugins.

The installation of the Accounts Payable Operations plugin may cause access issues to the existing functionality that are controlled by the Explicit Roles \[com.glide.explicit\_roles\] plugin. You may have to manage or reconfigure certain roles and permissions managed by the Explicit Roles \[com.glide.explicit\_roles\] plugin for seamless integration and operation of existing functionalities. For more information on explicit roles, see .

Frequently asked questions.

Why does Explicit Roles plugin matter?

The Explicit Roles plugin \(com.glide.explicit\_roles\) is the first prerequisite that must be installed before any APO plugin. It enforces role-based access control at the explicit record level. If it is not installed or if its configuration is not analyzed before APO installation, access control for APO roles may not function as expected.

**Parent Topic:**[Using Supplier Collaboration Portal in APO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/using-supplier-collaboration-portal.md)

