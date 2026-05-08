---
title: Enable pa\_dashboard records in scoped applications
description: When application administration is enabled for a scoped application, access control list \(ACL\) rules for the scoped application are applied. To allow your scope to use the ACLs defined on the \[pa\_dashboards\] table but out of your scoped app, inherit the \[pa\_dashboards\] ACLs.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Share a responsive dashboard, Working with responsive dashboards, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Enable pa\_dashboard records in scoped applications

When application administration is enabled for a scoped application, access control list \(ACL\) rules for the scoped application are applied. To allow your scope to use the ACLs defined on the \[pa\_dashboards\] table but out of your scoped app, inherit the \[pa\_dashboards\] ACLs.

## Before you begin

Role required: admin.

Scope required: the scope of your application.

## Procedure

1.  Set the system property **glide.security.scoped\_administration.honor\_global\_acl** to true.

    Often this property is already set to true, so additional update is not necessary. For more information, see Add a system property.

2.  Switch the scope to the scope that the dashboard is created in.

    The user should be that scope's application administrator.

3.  Navigate to sys\_scoped\_admin\_acl\_inheritance\_list.do.

4.  Create a record for the PA Dashboards \[pa\_dashboards\] table and select **Submit**.

5.  Create a record for each of these tables:

    -   Portal Page \[sys\_portal\_page\]
    -   Tabs \[pa\_tabs\]
    -   Dashboard Permissions \[pa\_dashboards\_permissions\]
6.  If multiple reports have the same issue, create a record for each of these tables:

    -   Reports \[sys\_report\]
    -   Report Users and Groups \[sys\_report\_users\_groups\]

