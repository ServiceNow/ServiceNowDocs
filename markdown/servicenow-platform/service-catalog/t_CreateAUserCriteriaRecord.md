---
title: Create a user criteria record in Service Catalog
description: Create a user criteria record to define conditions that are evaluated against user records.When creating user criteria for your system, consider the following recommendations.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Set security for items and categories, Service Catalog security, Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a user criteria record in Service Catalog

Create a user criteria record to define conditions that are evaluated against user records.

## Before you begin

Role required: admin, catalog\_admin

## About this task

You can apply several user criteria records to a single catalog item or category. In this situation, users match only one of these criteria records to have access.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **User Criteria** and create a record.

2.  Fill in the fields on the form, as appropriate.

<table id="table_ojq_r1g_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the criteria record.

</td></tr><tr><td>

Users

</td><td>

The individual user records to match.

</td></tr><tr><td>

Groups

</td><td>

The group records to match.

</td></tr><tr><td>

Roles

</td><td>

The roles to match. **Note:**

-   The evaluation of a role is cached in the session, so any change in the role requires you to logout and login, similar to roles in ACL \(Access Control List\).
-   User Criteria is not applicable for elevated privilege roles.


</td></tr><tr><td>

Advanced

</td><td>

A check box to display or hide the **Script** field.

</td></tr><tr><td>

Script

</td><td>

A [script](t_ContrlAccessByCDGUOrLoc.md#) to define any additional criteria, and return **true** or **false**. This field is available only if **Advanced** is selected. **Note:**

-   The script is evaluated in the scope that the user criteria is created in.
-   The evaluation of the script is cached in the session, so any change in the evaluation requires you to logout and login, similar to roles in ACL.
-   Do not use gs.getUser\(\) or other session APIs since they cause conflict when used in diagnostic tools. Use the pre-defined *user\_id* variable available in the script to get the user id of the user being used to evaluate the script.
-   Because scripts are evaluated dynamically, including scripts in user criteria records can decrease performance.
-   Because answer is a pre-reserved keyword, do not use a function with its name as answer, that is, answer\(\).


</td></tr><tr><td>

Active

</td><td>

A check box to activate or deactivate this criteria record.

</td></tr><tr><td>

Companies

</td><td>

The companies to match.

</td></tr><tr><td>

Locations

</td><td>

The locations to match.

</td></tr><tr><td>

Departments

</td><td>

The departments to match.

</td></tr><tr><td>

Match All

</td><td>

A check box to determine whether all elements from each populated criteria field must match. If selected, only users who match all criteria are given access. If cleared, the user must meet one or more of the set criteria to be given access. By default, this check box is cleared so that any condition met provides a match.

 For example, consider a user criteria record for the following:

-   Locations A or B
-   Company C or D
With **Match All** selected, only users meeting all these conditions are matched. For example, a user with a location A and a company C.

 With **Match All** cleared, users meeting any of these conditions are matched. For example, a user with a location B.

**Note:** If you select **Match All**, ensure that you do not create contradictory conditions which can never be met. For example, if all users in location A work for company G, then the conditions in this example can never be met.

</td></tr></tbody>
</table>
**Parent Topic:**[Set security for items and categories](../concept/c_ServiceCatalogAccessControls.md)

## Implementing user criteria

When creating user criteria for your system, consider the following recommendations.

-   Design Criteria for Reuse:

    Ensure that you design user criteria for maximum reuse. Create user criteria records with common sets of conditions matching your organization requirements. Allow them to be shared across as many items and categories as possible, rather than creating multiple similar criteria records for individual items and categories.

-   Naming conventions: Give each user criteria record a meaningful name, to help you determine the function for that record. For example,
    -   Users in company Cloud Dimensions AND in Madrid
    -   Users in company Cloud Dimensions OR in Madrid
    -   Users belonging to the Group Development, IT, or Sales
    -   Users with role itil, asset\_manager, or catalog\_admin
-   Test user criteria on a development or test instance, and then transfer the records from the user criteria tables and catalog records to your production instance using [update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

