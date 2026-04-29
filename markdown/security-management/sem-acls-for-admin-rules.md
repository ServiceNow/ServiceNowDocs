---
title: Access control lists \(ACLs\) for administration rules
description: You can either view or modify the administration rules based on the roles assigned to you.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Access control lists \(ACLs\) for administration rules

You can either view or modify the administration rules based on the roles assigned to you.

## New roles for administration rules

The following two new roles have been introduced to manage administration rules within the Security Exposure Management Workspace:

-   sn\_sec\_wf.read\_admin\_rules: Enables you to view all the administration rules.
-   sn\_sec\_wf.manage\_admin\_rules: Enables you to perform all CRUD \(Create, Read, Update, Delete\) operations on administration rules.

## Personas with read access to administration rules

The following personas can read administration rules:

-   sn\_vul.vulnerability\_analyst
-   sn\_vul\_container.vulnerability\_analyst
-   sn\_vulc.auditor
-   sn\_vulc.vulnerability\_analyst

## Personas with create, update, and delete permissions

The following personas can create, update, and delete admin rules, provided they have access to the corresponding findings table:

|Persona|Accessible Findings table|
|-------|-------------------------|
|sn\_vul.app\_sec\_manager|Application Vulnerable Item|
|sn\_vul. vulnerability\_admin|Vulnerable Item|
|sn\_vulc.admin|Test Result|
|sn\_vul\_container.vulnerability\_admin|Container Vulnerable Item|
|sn\_vul\_cmn.usem\_admin|Vulnerable Item, Application Vulnerable Item, Test Result, Container Vulnerable Item|

**Note:** You can only modify the rules if you have create, update, and delete permissions and access to the corresponding findings table.

Additional considerations for other rule types regarding create, update, and delete access:

-   **Lookup and Exclusion rules**: Access to create, update, or delete these rules is determined by the persona's permissions for the rule table itself, as they don’t have an associated findings table.
-   **Auto-delete rules**: Only users with the admin role can create, update, or delete these rules.
-   **Classification rules**: Personas can manage these rules if they have access to the specific table defined within the classification group.
-   **Rollup Calculator rules**: Personas who have access to the corresponding target table can manage these rules.

