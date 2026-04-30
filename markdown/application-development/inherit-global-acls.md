---
title: Configure a table in an application administration app to inherit global ACL rules
description: To avoid duplicating global access control rules \(ACLs\) in your applications, you can configure application file tables in application administration apps to inherit global ACLs when no ACL rules for the scoped application are found.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control rules in application administration apps, Application administration, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Configure a table in an application administration app to inherit global ACL rules

To avoid duplicating global access control rules \(ACLs\) in your applications, you can configure application file tables in application administration apps to inherit global ACLs when no ACL rules for the scoped application are found.

## Before you begin

Role required: admin role for the application

## Procedure

1.  Enter `sys_scoped_admin_acl_inheritance.list` in the navigation filter.

    The Application Administration ACL Inheritance table \[sys\_scoped\_admin\_acl\_inheritance\] opens.

2.  Click **New**.

3.  In the **Table** field, select an application file table \(a table that extends the Application File \[sys\_metadata\] table\) from the application administration app.

    Only the administrator for the application administration app can add/remove/read records owned by the application administration app in this configuration table.

4.  Click **Submit**.

    If no ACL rules from the application administration app are found, tables added to this list inherit global ACL rules.


