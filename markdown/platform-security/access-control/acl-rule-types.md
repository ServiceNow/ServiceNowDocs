---
title: ACL rule types
description: Create ACL rules on different components of the system.
locale: en-US
release: zurich
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Explore Access Control Lists, Access Control List Rules, Access Management]
---

# ACL rule types

Create ACL rules on different components of the system.

## Record ACL rules

Record ACL rules consist of table and field names.

-   The table name is the table that you want to secure. If other tables extend from this table, then the table is considered a parent table. ACL rules for parent tables apply to any table that extends the parent table.
-   The field name is the field that you want to secure. Some fields are part of multiple tables because of table extension. ACL rules for fields in a parent table apply to any table that extends the parent table.

ACL rules can secure the following record operations:

<table id="table_scf_z22_2r"><thead><tr><th>

Operation

</th><th>

Description

</th></tr></thead><tbody><tr><td>

execute

</td><td>

Enables users to execute client callable script includes and REST endpoint execution.

</td></tr><tr><td>

query\_match

</td><td>

Enables users to submit match queries\("is", "is not", "is empty", etc\).

</td></tr><tr><td>

conditional\_table\_query\_range

</td><td>

Enables users to give partial ACL-access based on read ACLs. Created for the tables that have the read ACLs without Data condition and script.

</td></tr><tr><td>

query\_range

</td><td>

Enables users to submit range queries\("starts with", "ends with", "contains", etc\) and sorting is unrestricted.

</td></tr><tr><td>

create

</td><td>

Enables users to insert new records \(rows\) into a table.

</td></tr><tr><td>

read

</td><td>

Enables users to display records from a table.

</td></tr><tr><td>

write

</td><td>

Enables users to update records in a table.

</td></tr><tr><td>

delete

</td><td>

Enables users to remove records from a table or drop a table.

</td></tr><tr><td>

edit\_task\_relations

</td><td>

Enables users to extend the Task \[task\] table.

</td></tr><tr><td>

edit\_ci\_relations

</td><td>

Enables users to extend the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr><td>

save\_as\_template

</td><td>

Enables users to save a record as a template.

</td></tr><tr><td>

add\_to\_list

</td><td>

Prevents users from viewing or personalizing specific columns in the list mechanic.**Note:** Conditions and scripts are not supported.

</td></tr><tr><td>

list\_edit

</td><td>

Enables users to update records \(rows\) from a list.

</td></tr><tr><td>

report\_on

</td><td>

Enables users to report on tables.

</td></tr><tr><td>

report\_view

</td><td>

Enables users to report on field ACLs.

</td></tr><tr><td>

personalize\_choices

</td><td>

Enables users to configure the table or field.

</td></tr><tr><td>

data\_fabric

</td><td>

Allows a data fabric table to reference a local table.

</td></tr></tbody>
</table>Record ACL rules are processed in the following order:

-   Match the object against table ACL rules.
-   Match the object against field ACL rules.

This processing order ensures that users gain access to more specific objects before gaining access to more general objects. A user must pass both table and field ACL rules to access a record object.

-   If a user fails a table ACL rule, the user is denied access to all fields in the table, even if the user passes a field ACL rule.
-   If a user passes a table ACL rule, but fails a field ACL rule, the user cannot access the field described by the field ACL rule.

![ACL matching](../image/acl-matching.png "ACL matching")

## Processor ACL rules

Processor ACL rules specify the processor you want to secure. For a list of available processors, navigate to **System Definition** &gt; **Processors**.

By default, an ACL rule for the EmailClientProcessor is included to restrict the email client to users with the itil role.

Processor ACL rules honor the STAR \(\*\) rule if they cannot find a more specific ACL for those resources.

## Table ACL rules

The user must first pass the table ACL rule. Since the base system includes STAR \(\*\) table ACL rules that match every table, the user must always pass at least one table ACL rule. The base system provides additional table ACL rules to control access to specific tables.

Table ACL rules are processed in the following order:

1.  Match the table name. For example, incident.
2.  Match the parent table name. For example, task.
3.  Match any table name \(\*\). For example, \*.

If a user fails all table ACL rules, the user cannot access any fields in the table. If a user passes a table ACL rule, the system then evaluates the field ACL rules.

## Field ACL rules

After a user passes a table ACL rule, field ACL rules are processed in the following order:

1.  Match the table and field name. For example, incident.number.
2.  Match the parent table and field name. For example, task.number.
3.  Match any table \(\*\) and field name. For example, \*.number.
4.  Match the table and any field \(\*\). For example, incident.\*.
5.  Match the parent table and any field \(\*\). For example, task.\*.
6.  Match any table \(\*\) and any field \(\*\). For example, \*.\*.

A user must pass the table ACL rule to be granted access to the table's fields. For example, the user must first pass the table ACL rule for the incident table to access the **Number** field in the incident table.

The first successful field ACL evaluation stops ACL rule processing at the field level. When a user passes a field ACL rule, the system stops searching for other matching field ACL rules. For example, if a user passes the field ACL rule for incident.number, the system stops searching for other ACL rules that secure the **Number** field in the incident table.

Access to query information of inferred data is restricted for protected fields, therefore preventing return of predictive information.

## UI page ACL rules

UI page ACL rules specify the UI page to be secured. For a list of available UI pages, navigate to **System UI** &gt; **UI Pages**. When defining an ACL rule for a UI page, use the fully scoped page name. For example, **x\_myapp\_mypage**.

**Note:** You can use the STAR \(\*\) character in the **Name** field on **ui\_page** type ACLs to match any UI pages.

UI page ACL rules honor the STAR \(\*\) rule if they cannot find a more specific ACL for those resources. For example, if you have a UI page named `mysecretpage` but do not define an ACL for this UI page, the STAR \(\*\) rule for the UI page processor is used for access check.

ACL rules can secure the following UI page operation:

|Operation|Description|
|---------|-----------|
|read|Allows users to display the UI page.|

## Client-callable script include ACL rules

Script include ACL rules specify the client-callable script include to be secured. For a list of available script includes, navigate to **System Definition** &gt; **Script Includes**. You can personalize the list to show the Client callable column.

The base system does not include any ACL rules for client-callable script includes.

Client-callable script include ACL rules honor the STAR \(\*\) rule if they cannot find a more specific ACL for those resources.

