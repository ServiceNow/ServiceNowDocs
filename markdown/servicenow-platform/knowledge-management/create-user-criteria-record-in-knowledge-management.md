---
title: Create user criteria for controlling access to knowledge bases and articles
description: Control access to knowledge bases and articles by creating user criteria.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Managing access to knowledge bases and knowledge articles, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create user criteria for controlling access to knowledge bases and articles

Control access to knowledge bases and articles by creating user criteria.

## Before you begin

Role required: user\_criteria\_admin

**Note:** To create a user criteria record from the Knowledge module, you must have the user\_criteria\_admin role in addition to the knowledge role. For more information about access, see [Managing access to knowledge bases and knowledge articles](../concept/user-access-knowledge.md).

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **User Criteria**.

2.  Click **New**.

3.  On the User Criteria form, fill in the fields.

<table id="table_ojq_r1g_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the user criteria.

</td></tr><tr><td>

Users

</td><td>

Users that must match the user criteria.

</td></tr><tr><td>

Groups

</td><td>

Groups that must match the user criteria.

</td></tr><tr><td>

Roles

</td><td>

Roles to match the user criteria. **Note:**

-   Because the evaluation of a role is cached in the session, any change in the role requires you to log in again.
-   User criteria are not applicable for elevated privilege roles.


</td></tr><tr><td>

Advanced

</td><td>

Option to display or hide the advanced option that includes the **Script** field on the User Criteria form.

</td></tr><tr><td>

Script

</td><td>

Script to define any additional user criteria that returns true or false. This field is available when the **Advanced** option is selected on the User Criteria form. **Note:**

-   A script is evaluated in the scope that the user criteria are created in.
-   The evaluation of a script is cached in the session, so any change in the evaluation requires you to log in again. If a scripted user criterion is defined for a knowledge base, user access to knowledge bases is evaluated once per session. If the script results in changes after a session cache is built, the result takes effect in the next session.
-   Don’t use gs.getUser\(\) or other session APIs because they cause conflicts when used in diagnostic tools. Use the predefined *user\_id* variable available in the script to get the user ID of the user being used to evaluate the script.
-   Scripts are evaluated dynamically. Therefore, including scripts in a user criteria can impact performance.


</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate the user criteria.

</td></tr><tr><td>

Companies

</td><td>

Companies that the user record must match.

</td></tr><tr><td>

Locations

</td><td>

Locations that the user record must match.

</td></tr><tr><td>

Departments

</td><td>

Departments that the user record must match.

</td></tr><tr><td>

Match All

</td><td>

Option to determine whether all elements from each populated user criteria field must match. If selected, only users who match all user criteria are given access. If cleared, the user must meet one or more of the set user criteria to be given access. By default, this check box is cleared so that any condition met provides a match.

 For example, consider a user criteria record for the following:

-   Locations A or B
-   Company C or D
With **Match All** selected, only users that meet all of these conditions are matched. For example, a user with a location A and a company C.

 If **Match All** isn’t selected, users meeting any of these conditions are matched. For example, a user with a location B.

**Note:** If you select **Match All**, ensure that you don't create contradictory conditions that can never be met. For example, if all users in location A work for company G, the conditions in this example can never be met.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Related topics**  


[Control access at the knowledge base level through user criteria](t_SelectUserCriteria.md)

[Control access at the knowledge article level through user criteria](t_SelectUCArticle.md)

