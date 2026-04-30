---
title: Permission evaluation
description: Permission evaluation criteria when using the Access analyzer.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Access Analyzer, Identity]
---

# Permission evaluation

Permission evaluation criteria when using the Access analyzer.

## Evaluation hierarchy

Permission for the selected user, group, or role is evaluated in the following hierarchy:

-   Business rule: A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried.
-   Access Handler: An internal system check using hidden source code on the platform.
-   Data Filtration: Data filter is a form of access control designed to work along with the existing Access Control rules \(ACLs\) on your instance. Data filter support only read operation.
-   Access control list \(ACL\): Rules for access control lists \(ACLs\) restrict access to data by requiring users to pass a set of requirements before they can interact with it. Within an ACL, the following hierarchy is evaluated:
    -   Role
    -   Security Attribute
    -   Condition
    -   Script

You can analyze access and permissions for the selected user, role, or group using the Access Analyzer. The permissions are evaluated based on the following rule types:

-   **Table Level Evaluation**: Role and security attribute ACLs are used for Table level evaluation.
-   **Record or Field level Evaluation**: Role, security attribute, condition, and script level ACLs are used for Record or Field level evaluation.
-   **UI page**: Support Only ready operations. Only read level ACLs are evaluated.
-   **REST Endpoint**: Support only execute operation. Only execute level ACL are evaluated.

Details about the important fields in the Access Results are as follows:

-   Presence of a script
-   Access result legend
-   Evaluation process
-   IAccessHandlers
-   Data filters
-   Access control list rules

## Presence of a script

Alert Icon in any status indicates the presence of a script in the ACL. Review highlighted ACLs to understand the final access. To know more about how these controls are evaluated and review the logic to determine the access, see [Access Analyzer Debug logs](access-analyzer-logs.md).

## Legend in Access Analyzer

When Analyzing the access and permissions, legends are displayed as part of the evaluation process. Following are the legends:

-   \[Passed\] Access granted
-   \[Blocked\] Access denied
-   \[Skipped\] Did not evaluate
-   \[Undefined\] No rule found

## Evaluation process

Evaluation process is carried out by impersonating a user and determining the access control list \(ACL\) permission on the resource. Permission rules enable access to the specified resource if the following checks are evaluated to true:

-   IAccessHandlers must evaluate to “Passed”, or is empty or undefined
-   Data filters must evaluate to “Passed”, or is empty or undefined
-   Access control rules \(ACLs\) evaluate to “Passed”

## IAccessHandlers

An internal system check using hidden source code on the platform. IAccessHandler can grant or deny access to a resource without evaluating ACLs. If IAccessHandler is ignored, then the ACLs are evaluated.

You can’t change the IAccessHandler checks. For example, an IAccessHandler implementation is used for access checks on application resources such as read access.

## Data filter

Data filter is a form of access control designed to work along with the existing Access Control rules \(ACLs\) on your instance.

## Access control list rules

Rules for access control lists \(ACLs\) restrict access to data by requiring users to pass a set of requirements before they can interact with it.

