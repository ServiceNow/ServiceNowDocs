---
title: ACL configuration watcher
description: The ACL configuration watcher lets you know what related ACLs exist on a table when you insert, update, or delete an ACL on the same table.
locale: en-US
release: yokohama
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ACL debugging tools, Advanced ACL configuration, Access Control List Rules, Access Management]
---

# ACL configuration watcher

The ACL configuration watcher lets you know what related ACLs exist on a table when you insert, update, or delete an ACL on the same table.

The ACL configuration watcher is an interceptor window that displays every time you make important changes on the Access Control \[sys\_security\_acl\] table. It displays a security rules summary window where you can view ACLs related to the one you are modifying. You cannot modify any ACLs from the security rules window. To make any modifications, close the watcher window and go to those ACLs.

The ACL configuration watcher does not appear in the following situations:

-   If you save or update an ACL record without actually making any changes.
-   If you make minor updates \(not an insert or delete\), such as updating scripts, conditions, and the admin-overrides option.
-   If the ACL record is not active.

## ACL Security Rules window

The configuration watcher shows the [ACL execution plan](../task/t_ShowACLExecutionPlan.md). The execution plan is displayed in the security rules pop-up window. You can view this kind of information:

|Item|Description|
|----|-----------|
|red highlight|An ACL that is deleted or deactivated.|
|blue highlight|An ACL that is modified.|
|green highlight|An ACL that is added or becomes active.|
|Masked|An ACL that was effective until you made a change.|
|Unmasked|An ACL that was just made effective when you made a change.|

![Configuration watcher](../image/config_watcher_example.png "Configuration watcher example")

