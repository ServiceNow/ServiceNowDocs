---
title: Access Analyzer Debug logs
description: Access Analyzer debug logs supply detailed information about the evaluation of access controls for a specific operation. These logs assist administrators and developers in troubleshooting access issues, optimizing security configurations, and ensuring that users have appropriate access to resources within the ServiceNow platform.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Frequently Asked Questions, Access Analyzer, Access Management]
---

# Access Analyzer Debug logs

Access Analyzer debug logs supply detailed information about the evaluation of access controls for a specific operation. These logs assist administrators and developers in troubleshooting access issues, optimizing security configurations, and ensuring that users have appropriate access to resources within the ServiceNow platform.

## Fields in Debug logs

For a given operation, the debug logs show a granular view of how ACLs, business rules, and other security attributes are evaluated.

![Fields in the Debug log](../images/access-analyzer-logs-details.png)

Following are the fields and their description in the Debug logs:

|Fields|Description|
|------|-----------|
|Name|Details about the business rule or ACL. You can select the business rule or ACL for more information.|
|Applies to|Indicates the level at which the ACL is applied, for example, `Field`, `Record`, or `Table`.|
|Status|The status of the ACL for the associated role and permission, for example, `Passed`, `Blocked`, or `Skipped`.|
|Required ACL roles|Specifies the roles necessary for access to the resource.|
|Role|Provides details about the status of roles in terms of access control, for example, `blocked`, `passed`, or `skipped`.|
|Security Attribute|The details about the security attribute evaluated as `Blocked`, `Passed`, or `Skipped` for the Access Control.|
|Condition|The details about the condition evaluated as `blocked`, `passed`, or `skipped` for the Access Control.|
|Script|The details about the script evaluated as `blocked`, `passed`, or `skipped` for the Access Control.|
|Customized|Indicates if any customized ACLs are included in the access control.|
|Application|Status of the Application. `Global` or `Store`.|

## Evaluation hierarchy

Permissions for the selected user, group, or role are evaluated in the following hierarchy:

1.  **Business rule**: A business rule is a server-side script that runs when a record is read, inserted, updated, or deleted, or when a table is queried.
2.  **Access Handler**: An internal system check using hidden source code on the platform.
3.  **Data Filtration**: A data filter is a form of access control designed to work along with the existing Access Control rules \(ACLs\) on your instance. Data filters support only read operations.
4.  **Access control list \(ACL\)**: Rules for access control lists \(ACLs\) restrict access to specific data by requiring users to pass a set of requirements before they can interact with it. Within an ACL, the following hierarchy is evaluated:
    1.  Role
    2.  Security Attribute
    3.  Condition
    4.  Script

## Access control list evaluation

ACLs for the operations are evaluated in the following order:

1.  Role
2.  Security Attribute
3.  Condition
4.  Script

## Presence of a script

Alert Icon in any status indicates the presence of a script in the ACL. Review highlighted ACLs to understand the final access.

**Note:** During an Access Analyzer query, business rules are executed first and then the access control list.

## Sequence of execution

The order of execution for determining access in different scenarios is as follows:

1.  **Presence of an inherited or wildcard ACL**: During the sequence of execution, the inherited ACLs are evaluated first and then wildcard ACLs.
2.  **If one ACL is passed, the others are skipped**: During execution and evaluation of permissions, if one ACL is passed, the other ACLs' execution and evaluations are skipped. They are skipped because overall permissions for the selected operation require only one ACL to access a field, record, or table for an identity.
3.  **Field level ACL and table level ACLs execution**: During execution, field level ACLs are executed first, followed by table level ACLs. This provides more granular results when analyzing access for an identity.
4.  **Evaluation in the presence of scripted ACL**: When a script is present, the overall access for the operation is passed with an Alert icon to indicate that there's a script in the ACL.

