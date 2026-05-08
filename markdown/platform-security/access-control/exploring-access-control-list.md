---
title: Explore Access Control Lists
description: Explore Access Control Lists \(ACLs\).
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Access Control List Rules, Access Management]
---

# Explore Access Control Lists

Explore Access Control Lists \(ACLs\).

All access control list rules specify:

-   The decision type, rule type and operation which defines the ACL
-   The object being secured
-   The conditions required to access the object

## Components of ACL

The decision type defines whether users are allowed to access the object if conditions are met or denies access the object unless conditions are met.

|Decision type|Description|
|-------------|-----------|
|Deny-Unless|Restrict access to resource by explicitly denying access unless conditions are passed. See [acl-denial-behavior.md\#section\_qnd\_snl\_zbc](acl-denial-behavior.md#section_qnd_snl_zbc) for more information.|
|Allow-If|Allow access to resource if conditions are passed.|

The object is the target to which access needs to be controlled. Each object consists of a type and name that uniquely identifies a particular table, field, or record. With the Applies-to field users have granular control over which specific records this ACL will apply to.

For example, all these entries specify an object:

<table id="table_mlr_5q3_yv"><thead><tr><th>

Type

</th><th>

Name

</th><th>

Object secured

</th></tr></thead><tbody><tr><td>

record

</td><td>

\[incident\].\[--None--\]

</td><td>

The Incident table.

</td></tr><tr><td>

record

</td><td>

\[incident\].\[active\]

</td><td>

The Active field in the Incident table.

</td></tr><tr><td>

record

</td><td>

\[incident\]Applies-To: Priority = P1

</td><td>

Only Priority 1 incidents in the incident table.

</td></tr><tr><td>

REST\_Endpoint

</td><td>

user\_role\_inheritance

</td><td>

The record for the user\_role\_inheritance Scripted REST API.

</td></tr></tbody>
</table>Each operation describes a valid action the system can take on the specified object. Some objects, such as records, support multiple operations, while other objects, such as a REST\_Endpoint, only support one operation.

For example, all these entries specify an operation:

|Type|Name|Operation|Operation secured|
|----|----|---------|-----------------|
|record|\[incident\].\[-- None --\]|create|Creating records in the Incident table.|
|record|\[incident\].\[active\]|write|Updating the Active field in the Incident table.|
|REST\_Endpoint|user\_role\_inheritance|execute|Running the user\_role\_inheritance scripted REST API.|

The conditions specify when someone can access the named object and operation. Security administrators can specify condition requirements by adding:

-   One or more user roles to the **Requires role** list.
-   One or more security attributes need to be evaluated to be true.
-   One or more data conditions.
-   A script that evaluates to true or false or sets the `answer` variable to true or false.

To gain access to an object and operation, a user must pass all conditions listed in an access control. For example, this access control restricts access to view operations on the incident table.

![ACL on an incident record.](../image/access-control-record-write-incident2.png)

To update a record in the incident table, a user must have the listed roles and the record must meet the condition.

|Condition type|Requirement|Description|
|--------------|-----------|-----------|
|Requires role|**Requires role**:itil|Only allow users with the itil role to update incidents.|
|Security Attributes|UserIsAuthenticated|Only authenticated users to update incidents.|
|Data Condition|\[Incident state\] \[is not\] \[Closed\]|Only allow updates to active incident records.|

## Applies-to behavior

The Applies-to field determines whether an ACL applies to records, whereas data condition evaluates an ACL that's already applied. Applies-to specifies whether the ACL affects a specific record; if it's empty, the ACL applies to all records. Applies-to can be used for granular ACL enforcement whereas "Data Condition" is an evaluation criteria.

**Note:** Applies-to is case sensitive.

## Deny by default behavior

By default the ACL engine completely denies access if an ACL is empty or invalid. Empty ACLs are defined as ACLs without one or more of these components:

-   Defined role
-   Security attribute
-   Data condition
-   Script

Invalid ACLs are defined as:

-   ACLs with roles that do not exist \(e.g. have no row in the database\)
-   ACLs with Security Attributes that do not exist \(e.g. have no row in the database\)
-   ACLs with a script that contains "answer=true" or "true"

If the system detects the user creating an ACL it will prompt the user to select a role or an existing security attribute.

![System prompting user to select.](../../security/image/empty-acl-example.png)

## ACL evaluation process

An ACL rule only grants a user access to an object if the user meets all conditions required by the matching ACL rule.

-   The condition must evaluate to true.
-   The script must evaluate to true or return an answer variable with the value of true.
-   The user must have one of the roles in the required roles list. If the list is empty, this condition evaluates to true.
-   \[Record ACL rules only\] The matching table-level and field-level ACL rules must both evaluate to true.

![ACL evaluate conditions](../image/AclEvaluatePermissions2.png "ACL evaluate conditions")

Whenever a session requests data, the system searches for access control rules that match the requested object and operation. If there’s a matching access control rule, then the system evaluates if the user has the conditions required to access the object and operation. If an access control rule specifies more than one condition, then the user must meet all conditions to gain access to the object and operation. Failing any one condition check prevents the user from accessing the matching object and operation.

If a user does not meet the conditions of the first matching rule, the system evaluates the conditions of the next matching access control rule as specified by the access control processing order. If the user fails to meet the conditions of any matching access control rule, the system denies access to the requested object and operation.

**Note:** If there are no matching access control rules for the requested object and operation, then the system grants the user access to it. In practice, it is rare for the system to find no matching rules because the system has a set of default access control rules that protect all record operations.

The effects of being denied access to an object depend on the ACL rule that the user failed. For example, failing a read operation ACL rule prevents the user from seeing the object. Depending on the object secured, the ACL rule hides a field on a form, hides rows from a list, or prevents a user from accessing a UI page. The following table contains a complete list of results of failing an ACL rule for a given operation and object type.

## Pre and post query ACL checks

Your instance checks ACL rules both before and after a user makes a query. Because different information is available before and after a query, results can be different.

-   **Pre-query ACL check**

    Before your instance runs a database query, it checks the ACL rules for each field in the queried table to determine which fields a user may access. This check only looks at the user's roles, and checks to see if these roles allow access to fields. Because this check runs before the query, the ACL doesn't have access to the records on the table, so it can’t take that data into account. Scripts and conditions that rely on knowing the contents of a record aren’t evaluated.

    If the user doesn't have read access at this point, the value for the field isn’t shown to the user.

-   **Post-query ACL check**

    After the query, your instance checks each record returned by the query. During this check, there’s context for the ACL, so the role, condition, and script portions of the ACL are evaluated. If the user doesn't have read access at this point, the value for the field isn’t shown to the user, however the user sees the field label if their roles allow access to the field.


<table id="table_evh_h12_2r"><thead><tr><th>

Operation

</th><th>

Results of failing an ACL rule on object

</th></tr></thead><tbody><tr><td>

execute

</td><td>

User can’t execute scripts on a record or UI page.

</td></tr><tr><td>

create

</td><td>

User can’t see the **New** UI action from forms. The user also cannot insert records into a table using API protocols such as web services.A **create** ACL with a condition requiring that a field contain a specific value may evaluate as false. Fields on new records are considered empty until the record is saved.

</td></tr><tr><td>

read

</td><td>

User can’t see the object in forms or lists. The user also can’t retrieve records using API protocols such as web services.

</td></tr><tr><td>

write

</td><td>

User sees a read-only field in forms and lists, and the user can’t update records using API protocols such as web services.

</td></tr><tr><td>

delete

</td><td>

User cannot see the **Delete** UI action from forms. The user also can’t remove records from a table using API protocols such as web services.

</td></tr><tr><td>

edit\_task\_relations

</td><td>

User cannot define relationships between task tables.

</td></tr><tr><td>

edit\_ci\_relations

</td><td>

User cannot define relationships between Configuration Item \[cmdb\_ci\] tables.

</td></tr><tr><td>

save\_as\_template

</td><td>

Used to control the fields that should be saved when a template is created.

</td></tr><tr><td>

add\_to\_list

</td><td>

User can’t view or personalize specific columns in the list mechanic.

</td></tr><tr><td>

list\_edit

</td><td>

User can’t update records \(rows\) from a list.

</td></tr><tr><td>

report\_on

</td><td>

User can’t create a report on the ACL table. For more information, see Restrict report creation with an ACL rule.

</td></tr><tr><td>

report\_view

</td><td>

User can’t view the content of a report on the ACL table or on the ACL field. For more information, see Reporting.

</td></tr><tr><td>

personalize\_choices

</td><td>

User can’t right-click a list field and select **Configure Choices**.

</td></tr></tbody>
</table>## ACL matching requirements for objects

<table id="table_bcz_vb2_2r"><thead><tr><th>

Object Type

</th><th>

Matching ACL Rules Required to Access Object

</th><th>

Existing wild-card ACL Rules

</th></tr></thead><tbody><tr><td>

Client-callable script includes

</td><td rowspan="2">

Users must meet the conditions of two ACL rules:1.  All wild-card ACL rules for the object \(if any ACL rule exists for the operation\).
2.  The first ACL rule that matches the object's name \(if any ACL rule exists for the operation\).

</td><td rowspan="2">

By default, there are no wild-card \(\*\) rules for these object types. If you create a wild-card ACL rule for one of these objects, then the ACL rule applies to all objects of this type.

</td></tr><tr><td>

Processors

</td></tr><tr><td>

UI pages

</td><td rowspan="2">

Users must meet the conditions of two ACL rules:1.  The first ACL rule that matches the record's field \(if any ACL rule exists for the operation\).
2.  The first ACL rule that matches the record's table \(if any ACL rule exists for the operation\).

</td><td rowspan="2">

By default, there are wild-card table rules \(\*\) for the create, read, write, and delete operations and wild-card field rules \(\*.\*\) for the personalize\_choices, create, and save\_as\_template operations. When you create a table, create ACL rules for the table unless you want to use the provided wild-card ACL rules.

</td></tr><tr><td>

Record

</td></tr></tbody>
</table>**Note:** The Security manager default behavior \(glide.sm.default\_mode\) property determines whether users can access objects that only match against wild-card table ACL rules. When this property is set to Deny access, only administrators can access objects that match the wild-card table ACL rules.

**Note:** The wild-card field ACL rule \(\*.\*\) for the create operation reuses the same conditions as the write operation. This means that the create conditions are the same as the write conditions unless you define an explicit create operation ACL rule.

## Multiple ACL rules at the same point in the processing order

If two or more rules match at the same point in the processing order, the user must pass any one of the ACL rules conditions to access the object. For example, if you create two field ACL rules for **incident.number**, then a user who passes one rule has access to the number field regardless of whether the user failed any other field ACL rule at the same point in the processing order.

## Required role

Normal admin users can view and debug access control rules. However, to create or update existing access control rules, administrators must elevate privileges to the security\_admin role. See [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md) for instructions.

## ACL rules in scoped applications

You can create ACL rules for objects in the same scope as the ACL rule. You can also create ACL rules for tables with at least one field that is in the same scope as the ACL rule.

For tables that are in a different scope than the ACL rule record, the types of rules are limited.

-   You can create an ACL rule for any table, UI page, or other object that is in the same scope as the ACL rule.
-   You can create an ACL for a field that is in the same scope as the ACL rule.
    -   If the table is in the same scope, you can use a script to evaluate conditions.
    -   If the table is in a different scope, you can’t use a script to evaluate conditions.
-   You can’t create or modify ACL rules for objects that are in a different scope than the application you’ve selected in the application picker, including adding a role to an ACL in a different scope.
-   You can create wild-card table rules \(\*\) only in the global scope.
-   You can create wild-card field rules \(\*\) only for tables in the same scope as the ACL rule.

