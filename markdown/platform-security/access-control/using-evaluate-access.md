---
title: Using Evaluate access
description: Analyze identities on the ServiceNow AI Platform instance.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Access Analyzer, Access Analyzer, Access Management]
---

# Using Evaluate access

Analyze identities on the ServiceNow AI Platform instance.

## Before you begin

Role required: access\_analyzer\_admin

The following procedure describes the steps for accessing Evaluate access in the Access Analyzer and using its various features.

**Note:** Access Analyzer is a ServiceNow Store product.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

    The Analyze access and permissions homepage is displayed.

2.  Select the **Evaluate access** tab.

3.  Select your criteria as follows:

<table id="table_cpw_mgd_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Analyze by \*

</td><td>

Analyze access for a user, a role, or a group

</td></tr><tr><td>

Select user \*

</td><td>

Specify a user name to select from the list.

</td></tr><tr><td>

Rule type \*

</td><td>

Analyze access for the following:-   Table
-   UI page
-   REST Endpoint
-   Client callable script include
-   AI agent
-   Agentic workflow


</td></tr><tr><td>

Select table \*

</td><td>

Specify a table name to select from the list.

</td></tr><tr><td>

Select record

</td><td>

Specify a record name to select from the list.

</td></tr><tr><td>

Select field

</td><td>

Specify a field name to select from the list.

</td></tr></tbody>
</table>4.  Specify the description in the **Description** field.

5.  Select **Analyze permissions**.

    The access results for the user are displayed. Similarly you can analyze the permissions of a Group or Role for the following rule types:

    -   Table \(record\)
    -   Client callable scripts include
    -   REST endpoints
    The access results are displayed.

    ![Access results](../images/use-access-analyzer-results.png)

    The Access results table includes the following fields:

<table id="table_dqg_wxp_dyb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operation

</td><td>

The type of operation that the user, group, or role can perform for the selected table, record, or field.

</td></tr><tr><td>

Overall Access

</td><td>

Result of the overall access. The results are as follows:-   \[Passed\] Access granted
-   \[Blocked\] Access denied
-   \[Skipped\] Didn’t evaluate
-   \[Undefined\] No rule found


</td></tr><tr><td>

ACL

</td><td>

Whether an ACL is defined for the selected operation.

</td></tr><tr><td>

Access Handler

</td><td>

An internal system check using hidden source code on the platform. IAccessHandler can grant or deny access to a resource without evaluating ACLs. If IAccessHandler is ignored, then the ACLs are evaluated.

</td></tr><tr><td>

Data filtration

</td><td>

A data filter is a form of access control designed to work along with the existing Access Control rules \(ACLs\) on your instance.

</td></tr><tr><td>

Execution time

</td><td>

The time at which the access results were executed.

</td></tr><tr><td>

Insights

</td><td>

More information about the selected operation.

</td></tr><tr><td>

Execution ID

</td><td>

A unique ID for each access result execution.

</td></tr></tbody>
</table>6.  Select the Operation for more information about the ACL.

    For example, if you select **read**, the access control related to read is displayed.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the ACL.|
    |Decision Type|Decision type configured for the ACL. **Allow access** or **Deny access**.|
    |Applies to condition|Whether the ACL is applied to a condition.|
    |ACL Applies to|Details about the resource the ACL is applied.|
    |Status|Status of the ACL or Access result.|
    |Required ACL Roles|Details of the role that is required to access the resource.|
    |Role|Status of the role. Passed, Skipped, or Blocked.|

    ![ACL Details](../images/acl-details-for-user.png)


