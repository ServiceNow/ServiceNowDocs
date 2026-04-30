---
title: Related record access
description: Related record access enable consistent control over what records users are able to access between related tables.
locale: en-US
release: yokohama
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure an ACL rule, Access Control List Rules, Access Management]
---

# Related record access

Related record access enable consistent control over what records users are able to access between related tables.

Related record access enables you to configure access to related record, determining whether the related parent table's ACL should be enforced on data that is allowed access from the ACL. Consider the following use-case, a user has access to a record via ACL, then related record access enables the users' access to all other records related to it, via either reference or bidirectional relationship.

Review the related records of an ACL in the **Advanced Condition** &gt; **Controlled by references** field. See [Configure an ACL rule](../task/t_CreateAnACLRule.md) for more information on configuring ACLs.

**Warning:** Related record access does not support security data filters, or tables with name and document IDs.

