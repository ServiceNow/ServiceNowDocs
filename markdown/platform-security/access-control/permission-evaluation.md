---
title: Permission evaluation
description: Understand permission evaluation criteria when using Access Analyzer.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access Analyzer, Access Management]
---

# Permission evaluation

Understand permission evaluation criteria when using Access Analyzer.

## Evaluation hierarchy

Permission for the selected user, group, or role is evaluated in the following hierarchy:

-   Business rule: A business rule is a server-side script that runs when a record is displayed, inserted, updated, deleted, or when a table is queried.
-   Access Handler: An internal system check using hidden source code on the platform.
-   Data Filtration: Data filters are a form of access control designed to work with existing Access Control rules \(ACLs\) on your instance. Data filters support only read operations.
-   Access control list \(ACL\): Rules for access control lists \(ACLs\) restrict access to specified data by requiring users to pass a set of requirements before they can interact with it. Within an ACL, the following hierarchy is evaluated:
    -   Role
    -   Security Attribute
    -   Condition
    -   Script

You can analyze access and permissions for the selected user, role, or group using Access Analyzer. Permissions are evaluated based on the following rule types:

-   **Table Level Evaluation**: Role and security attribute ACLs are used for Table level evaluation.
-   **Record or Field level Evaluation**: Role, security attribute, condition, and script level ACLs are used for Record or Field level evaluation.
-   **UI page**: Supports only read operations. Only read level ACLs are evaluated.
-   **REST Endpoint**: Support only execute operation. Only execute level ACL are evaluated.

The **Access results** table includes:

-   Presence of a script \(alert icon\)
-   Access result legend
-   Evaluation process
-   IAccessHandlers
-   Data filters
-   Access control list rules

## Presence of a script

An Alert Icon next to any status indicates the presence of a script in the ACL. Review highlighted ACLs to understand the final access. To know more about how these controls are evaluated and review the logic used to determine access, see [Access Analyzer Debug logs](access-analyzer-logs.md).

## Status in Access Analyzer

When analyzing access and permissions, Access Analyzer shows the evaluation's result or status. Statuses include:

-   \[Passed\] Access granted
-   \[Blocked\] Access denied
-   \[Skipped\] Did not evaluate
-   \[Undefined\] No rule found

## Evaluation process

The evaluation process is carried out by impersonating a user and by determining the access control list \(ACL\) permissions on the resource. Permission rules enable access to the specified resource if the following checks are evaluated to true:

-   IAccessHandlers must evaluate to “Passed”, or is empty or undefined
-   Data filters must evaluate to “Passed”, or is empty or undefined
-   Access control rules \(ACLs\) evaluate to “Passed”

## IAccessHandlers

IAccessHandlers are an internal system check using hidden source code on the platform. IAccessHandler can grant or deny access to a resource without evaluating ACLs. If IAccessHandler is ignored, then the ACLs are evaluated.

You can’t change the IAccessHandler checks. For example, an IAccessHandler implementation is used for access checks on application resources such as read access.

## Data filters

Data filters are a form of access control designed to work along with the existing Access Control rules \(ACLs\) on your instance.

## Access control list rules

Rules for access control lists \(ACLs\) restrict access to specific data by requiring users to pass a set of requirements before they can interact with it.

