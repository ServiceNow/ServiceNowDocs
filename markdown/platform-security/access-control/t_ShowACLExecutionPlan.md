---
title: Show ACL execution plan
description: Administrators can view how ACLs relate to each other by viewing an execution plan for any ACL in the instance.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACL configuration watcher, ACL debugging tools, Advanced ACL configuration, Access Control List Rules, Access Management]
---

# Show ACL execution plan

Administrators can view how ACLs relate to each other by viewing an execution plan for any ACL in the instance.

## Before you begin

Role required: security\_admin

## Procedure

1.  [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md).

2.  Navigate to **System Security** &gt; **Access Control \(ACL\)**.

3.  Open an ACL with the type **record**.

    ![ACL type equals "record."](../image/acl-type-record.png)

4.  Click **Show ACL Execution Plan** in the Related Links section.

    The security rules window appears for the ACL. The example displays the execution plan for "vtb\_task".

    ![An ACL execution plan](../image/ACL_execution_plan.png)

    |UI item|Description|
    |-------|-----------|
    |Title|The name of the ACL.|
    |Tab name|If the ACL is create, read, write, or delete.|
    |Row level|Row-level ACLs that run on this table.|
    |Field level|Field-level ACLs that run only on this field \(or column in the table\).|

5.  Click **Show all** to show all related ACLs, including those ACLs that are overridden and generic ACLs that apply to all records.

    Overridden ACLs have a line through the name, and generic ACLs have the wildcard character asterisk \(\*\) for the name.

6.  Show only the immediate ACLs related to the one you are viewing and hide the ACLs on tables from which the ACL table is extended and the generic wildcard \(\*\) ACLs by clicking **Show Effective**.


