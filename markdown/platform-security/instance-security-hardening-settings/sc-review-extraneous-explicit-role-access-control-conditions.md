---
title: Review extraneous explicit role access control conditions \[Removed in Security Center 1.5\]
description: The Explicit Roles plugin is recommended to mandate that all users have either the snc\_internal role to access internal resources, or the snc\_external role to access external resources.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-14"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Review extraneous explicit role access control conditions \[Removed in Security Center 1.5\]

The Explicit Roles plugin is recommended to mandate that all users have either the snc\_internal role to access internal resources, or the snc\_external role to access external resources.

After the installation of this plugin, all existing users are assigned the snc\_internal role, and existing access control lists \(ACLs\) are populated with the role conditions. Due to automation logic or intervention by an instance admin, the snc\_internal or snc\_external roles may be incorrectly added to an ACL that already contains a more strict role requirement. Since ACL role evaluation will pass for any user containing any role mapped to an ACL, the addition of snc\_internal or snc\_external may be too broad for the intended purpose of an ACL. This could lead to data leakage if a low privileged user is granted access through the ACL.

For example, it would be unnecessary for both the snc\_internal and the admin roles to be mapped to the same ACL within a table. The ACL is meant to grant access to admins, in which case the snc\_internal role is a mistake. Or, the ACL is meant to grant access to all snc\_internal users which makes the admin role unnecessary. When the Explicit Roles plugin is installed, review the ACLs which contain a role condition for snc\_internal or snc\_external while also containing a condition for another role. If the roles are able to function for a specific use case, then the finding should be periodically reviewed.

**Important:** This hardening setting will be removed in the next Security Center v1.5 store patch release and future versions. An Instance Scan suite called "Explicit Roles ACL Config Check Suite" is available in the Washington release. We recommend that you review the findings of this new Instance Scan.

**Parent Topic:**[Access control](sc-access-control.md)

