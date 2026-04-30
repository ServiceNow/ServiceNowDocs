---
title: Access Analyzer Debug logs
description: Debug logs display the details of the select access result operation.
locale: en-US
release: xanadu
product: Identity
classification: identity
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Frequently Asked Questions, Access Analyzer, Identity]
---

# Access Analyzer Debug logs

Debug logs display the details of the select access result operation.

## Fields in Debug logs

The Debug logs in the Access Analyzer displays information about the selected operation to understand the permissions, business rules, and ACLs associated with the operation.

![Fields in the Debug log](../images/access-analyzer-logs-details.png)

Following are the fields and their description in the Debug logs:

|Fields|Description|
|------|-----------|
|Name|The details about the business rule or ACL. You can select the business rule of ACL for more information.|
|Applies to|The details about the application of ACL at a field, record, or table level.|
|Status|Status of the ACL for the associated role and permission.|
|Requires ACL|The role that is required for accessing the field, record, or table.|
|Role|The details about the role being Blocked, Passed, Skipped for the Access Control.|
|Security Attribute|The details about the security attribute being Blocked, Passed, Skipped for the Access Control.|
|Condition|The detail about the condition being Blocked, Passed, Skipped for the Access Control.|
|Script|The details about the script being Blocked, Passed, Skipped for the Access Control.|
|Customized|The details about the customized ACL if any for the Access Control.|
|Application|Status of the Application. Global or Store.|

## Evaluation hierarchy

Permission for the selected user, group, or role is evaluated in the following hierarchy:

-   Business rule: A business rule is a server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried.
-   Access Handler: An internal system check using hidden source code on the platform.
-   Data Filtration: A data filter is a form of access control designed to work along with the existing Access Control rules \(ACLs\) on your instance. Data filters support only read operation.
-   Access control list \(ACL\): Rules for access control lists \(ACLs\) restrict access to data by requiring users to pass a set of requirements before they can interact with it. Within an ACL, the following hierarchy is evaluated:
    -   Role
    -   Security Attribute
    -   Condition
    -   Script

## Access control list evaluation

ACLs for the operations are evaluated in the sequence as follows:

-   Role
-   Security Attribute
-   Condition
-   Script

## Presence of a script

Alert Icon in any status indicates the presence of a script in the ACL. Review highlighted ACLs to understand the final access.

**Note:** During an Access analyzer query, business rules are executed first and then the access control list.

## Sequence of execution

The sequence of access result execution in different scenarios is as follows:

-   **Presence of an inherited or wildcard ACL**: During the sequence of execution the inherited ACLs are evaluated first and then wildcard ACL.
-   **One ACL is passed the others are skipped**: During execution and evaluation of permission if one ACL is passed the other ACL execution and evaluation is skipped. Because the overall permission for the selected operation requires one ACL to access a field, record, or table for an identity.
-   **Field level ACL and table level ACLs execution**: During execution field level ACLs are executed first followed by table level ACL to provide more granular results when analyzing the access for an identity.
-   **Evaluation in the presence of scripted ACL**: When there’s a presence of a script, the overall access for the operation is passed with an Alert icon to indicate the script in the ACL.

