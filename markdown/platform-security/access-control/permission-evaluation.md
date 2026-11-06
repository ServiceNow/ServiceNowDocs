---
title: Permission evaluation
description: The Access Analyzer uses permission evaluation criteria when you analyze access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/access-control/permission-evaluation.html
release: zurich
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Access analyzer, Access Management]
---

# Permission evaluation

The Access Analyzer uses permission evaluation criteria when you analyze access.

## Evaluation hierarchy

Permission for the selected user, group, or role is evaluated in the following hierarchy:

-   Business rule: A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried.
-   Access Handler: An internal system check using hidden source code on the platform.
-   Data Filtration: Data filter is a form of access control that works with the existing access control rules \(ACLs\) on your instance. Data filter supports only read operations.
-   Access control list \(ACL\): Rules for access control lists \(ACLs\) restrict access to data by requiring users to pass a set of requirements before they can interact with it. Within an ACL, the following hierarchy is evaluated:
    -   Role
    -   Security Attribute
    -   Condition
    -   Script

You can analyze access and permissions for the selected user, role, or group using the Access Analyzer. The permissions are evaluated based on the following rule types:

-   **Table Level Evaluation**: Role and security attribute ACLs are used for Table level evaluation.
-   **Record or Field level Evaluation**: Role, security attribute, condition, and script level ACLs are used for Record or Field level evaluation.
-   **UI page**: Supports only read operations. Only read-level ACLs are evaluated.
-   **REST Endpoint**: Supports only execute operations. Only execute-level ACLs are evaluated.

Details about the important fields in the Access Results are as follows:

-   Presence of a script
-   Access result legend
-   Evaluation process
-   IAccessHandlers
-   Data filters
-   Access control list rules

## Presence of a script

The alert icon in any status indicates the presence of a script in the ACL. Review highlighted ACLs to understand the final access. To learn more about how these controls are evaluated and review the logic to determine the access, see [Access Analyzer Debug logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/access-control/access-analyzer-logs.md).

## Legend in Access Analyzer

When analyzing the access and permissions, legends are displayed as part of the evaluation process. The following are the legends:

-   \[Passed\] Access granted
-   \[Blocked\] Access denied
-   \[Skipped\] Not evaluated
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

Data filter is a form of access control that works with the existing access control rules \(ACLs\) on your instance.

## Access control list rules

Rules for access control lists \(ACLs\) restrict access to data by requiring users to pass a set of requirements before they can interact with it.

