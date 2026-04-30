---
title: Enable security jump start plugin \(ACL Rules\) \[Updated in Security Center 1.3\]
description: Activate the Security Jump Start \(ACL Rules\) \(com.snc.system\_securitycom.snc.system\_security\) plugin to create several important ACLs that validate the Access Controls on some of the key system tables within the ServiceNow AI Platform.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable security jump start plugin \(ACL Rules\) \[Updated in Security Center 1.3\]

Activate the Security Jump Start \(ACL Rules\) \(com.snc.system\_security**com.snc.system\_security**\) plugin to create several important ACLs that validate the Access Controls on some of the key system tables within the ServiceNow AI Platform.

These rules provide a jump-start on securing many system tables, making it easier for an organization to get an instance into production. The Security Jump Start \(ACL Rules\) plugin is installed automatically on all new instances.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Plugin ID

</td><td>

**com.snc.system\_security**

</td></tr><tr><td>

Configuration type

</td><td>

System Definition &gt; Plugins

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

Activate the Security Jump Start \(ACL Rules\) plugin to achieve proper security compliance. It provides some basic ACLs that secure system tables in the first place instead of creating manually for each system table that comes with default provisioning of an instance. These ACLs are helpful when the newly created instance must quickly move into production.

</td></tr><tr><td>

Recommended value

</td><td>

Active

</td></tr><tr><td>

Default value

</td><td>

None. This is a plugin, not a Glide property, so there is no default value. The plugin is installed by default on zBoot \(resets\).

</td></tr><tr><td>

Security risk rating

</td><td>

8.1

</td></tr><tr><td>

Functional impact

</td><td>

There is significant functional impact if this plugin is installed without auditing of the existing ACLs on the instance. Customer outreach and definitions are required before the remediation can occur.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Access control should be enforced to lock down the unintended access to the instance. ACL jumpstart rules were created to provide a starting point on securing many system tables to make it easier for an organization to quickly get into production.

</td></tr><tr><td>

References

</td><td>

[Security jump start - ACL rules](../../roles/reference/r_SecurityJumpStartACLRules.md)

</td></tr></tbody>
</table>## Steps to configure

If this plugin is not activated on your instance, contact ServiceNow Support. Activating the plugin at this point might modify security access to tables already in use in a production environment. If an administrator is interested in the new ACL rules the plugin provides, you can manually create one or more of them in an existing instance if needed. This list of ACLs may be used as a guideline in that case.

**Parent Topic:**[Access control](sc-access-control.md)

