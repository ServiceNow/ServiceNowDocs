---
title: Advanced ACL configuration
description: In addition to creating new ACLs or modifying existing ones, you can configure other aspects of ACL functionality.
locale: en-US
release: zurich
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access Control List Rules, Access Management]
---

# Advanced ACL configuration

In addition to creating new ACLs or modifying existing ones, you can configure other aspects of ACL functionality.

## Deny ACL rules

Deny-Unless

## Query ACL rules

|Task|Description|
|----|-----------|
|[Apply ACL script conditions to reference fields](../reference/r_ContScriptCondAppRefFld.md)|Enable a property to allow script conditions to apply to reference fields if you want to control access to the data that a reference field displays on a form or in a list. There might be an impact to the performance of your instance if you enable this.|
|[Apply ACLs to AJAXGlideRecord \(client-side Glide record\)](../../security/reference/r_ApplyACLsToAJAXGlideRecord.md)|Apply ACLs to GlideAjax API calls so that the system queries only the data that the currently connected user has rights to access.|
|[Evaluate the admin override at the access level](../task/t_EvalAdmOverrideAccLevel.md)|Force ACL evaluation for admin overrides at the access level. By default, users with the admin role automatically pass the permissions check for this ACL rule when the Admin Overrides option is selected on the [ACL rules form](../task/t_CreateAnACLRule.md).|
|[Use ACL debugging and troubleshooting tools](c_AccessControlRulesDebug.md)|Use tools like the ACL watcher, field level debugging, and access ACL rule output messages to help you troubleshoot and debug ACLs.|

