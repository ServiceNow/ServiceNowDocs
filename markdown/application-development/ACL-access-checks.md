---
title: Access control rules in application administration apps
description: By default, when application administration is enabled for a scoped application, ACL rules for the scoped application are applied. If no ACL rules for the scoped application are found, global ACL rules can apply.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Application administration, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Access control rules in application administration apps

By default, when application administration is enabled for a scoped application, ACL rules for the scoped application are applied. If no ACL rules for the scoped application are found, global ACL rules can apply.

This behavior applies to configuration records created in tables that extend the Application File \[sys\_metadata\] table only. You can also change the default behavior.

When no access control \(ACL\) rules for an application administration app are defined, global ACL rules can apply to the configuration records of the application administration apps. See [Application files](c_ApplicationFiles.md) for more information.

**Note:** Not all applications utilize global ACL rules. If you are unable to perform an action as expected, verify that the application allows global ACL rules. If it does not, you may need to create specific ACL rules for some applications.

To allow a table in an application administration app to inherit global ACL rules, check that the system property is true and follow the instructions detailed in [Configure a table in an application administration app to inherit global ACL rules](../task/inherit-global-acls.md).

-   `glide.security.scoped_administration.honor_global_acl` system property: If no scoped ACL rules are defined, application administration apps can inherit global ACL rules. By default, this property is enabled for new and upgraded instances.
-   Application Administration ACL Inheritances \[sys\_scoped\_admin\_acl\_inheritance\] table: If no ACL rules for the application administration app are found, tables added to this list inherit global ACL rules. Only the administrator for the application administration app can add, remove, read the records owned by the application administration app in this configuration table.

