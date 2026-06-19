---
title: Show ACL execution plan
description: Administrators can view how ACLs relate to each other by viewing an execution plan for any ACL in the instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/access-control/t\_ShowACLExecutionPlan.html
release: zurich
product: Access Control
classification: access-control
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACL configuration watcher, ACL debugging tools, Advanced ACL configuration, Access Control List Rules, Access Management]
---

# Show ACL execution plan

Administrators can view how ACLs relate to each other by viewing an execution plan for any ACL in the instance.

## Before you begin

Role required: security\_admin

## Procedure

1.  [Elevate to a privileged role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/t_ElevateToAPrivilegedRole.md).

2.  Navigate to **System Security** &gt; **Access Control \(ACL\)**.

3.  Open an ACL with the type **record**.

    \[Omitted image "acl-type-record.png"\] Alt text: ACL type equals "record."

4.  Click **Show ACL Execution Plan** in the Related Links section.

    The security rules window appears for the ACL. The example displays the execution plan for "vtb\_task".

    \[Omitted image "ACL\_execution\_plan.png"\] Alt text: An ACL execution plan

    |UI item|Description|
    |-------|-----------|
    |Title|The name of the ACL.|
    |Tab name|If the ACL is create, read, write, or delete.|
    |Row level|Row-level ACLs that run on this table.|
    |Field level|Field-level ACLs that run only on this field \(or column in the table\).|

5.  Click **Show all** to show all related ACLs, including those ACLs that are overridden and generic ACLs that apply to all records.

    Overridden ACLs have a line through the name, and generic ACLs have the wildcard character asterisk \(\*\) for the name.

6.  Show only the immediate ACLs related to the one you are viewing and hide the ACLs on tables from which the ACL table is extended and the generic wildcard \(\*\) ACLs by clicking **Show Effective**.


