---
title: Creation restrictions across application scopes
description: The system restricts the creation of some configuration records when the current application scope does not match the application scope of the configuration record's target table.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Creation restrictions across application scopes

The system restricts the creation of some configuration records when the current application scope does not match the application scope of the configuration record's target table.

Configuration record creation restrictions prevent one application from making unwanted changes to another application's data tables. These restrictions only apply when you create a configuration record whose target table belongs to another application. Configuration records that belong to the same application scope do not have these restrictions.

The system always enforces the following creation restrictions when a developer adds a configuration record belonging to another application scope.

<table id="table_hnk_slc_br"><thead><tr><th>

Configuration record type

</th><th>

Creation restrictions when target table is in another application scope

</th></tr></thead><tbody><tr><td>

Access controls

</td><td>

-   You can only create field-level access controls with a role-based requirement.
-   You cannot create table-level access controls for a table in another application scope.
-   You cannot create field-level access controls that apply to all fields.
-   You cannot create access controls that use conditions.
-   You cannot create access controls that use a script-based condition.

</td></tr><tr><td>

Business rules

</td><td>

-   You can create a rule where **When** is async with any of the following options:
    -   Insert, Update, and Delete database operations. You cannot select Query.
    -   **Set field values** actions and scripts \(the **Script** field\).
-   You can create a rule where **When** is before with any of the following options:
    -   Insert, Update, and Delete database operations. You cannot select Query.
    -   **Set field values** actions only. You cannot write scripts and you cannot abort the database transaction.

</td></tr><tr><td>

Calculated fields

</td><td>

You cannot create calculated fields for tables in another application scope.

</td></tr><tr><td>

Data policies

</td><td>

-   You cannot create data policy rules for fields in another application scope.
-   You cannot make a field mandatory.

</td></tr><tr><td>

Field styles

</td><td>

You cannot create field styles for fields in another application scope.

</td></tr><tr><td>

Form sections

</td><td>

-   You cannot modify existing form sections created in another application scope.
-   You can create new form sections.

</td></tr><tr><td>

Record producers

</td><td>

You must have create access to the application table to create records from a record producer.

</td></tr><tr><td>

UI policies

</td><td>

-   You cannot create UI policy rules for fields in another application scope.
-   You cannot make a field mandatory.

</td></tr><tr><td>

UI script

</td><td>

You cannot create a global UI script from a scoped application.

</td></tr><tr><td>

Views

</td><td>

-   You can create new views.
-   You cannot modify existing views created in another application scope.

</td></tr></tbody>
</table>