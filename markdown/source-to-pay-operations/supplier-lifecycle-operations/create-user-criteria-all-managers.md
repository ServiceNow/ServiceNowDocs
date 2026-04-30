---
title: Create custom user criteria for all managers
description: You can create custom user criteria for all managers for configuring the assessment reassignment criteria.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-03"
reading_time_minutes: 2
breadcrumb: [Configure user criteria for reassigning assessments, Configure smart assessments, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create custom user criteria for all managers

You can create custom user criteria for all managers for configuring the assessment reassignment criteria.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **User Criteria**.

2.  Select **New**.

3.  On the User Criteria form, fill in the fields.

<table id="table_ojq_r1g_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the user criteria. For example, All supplier managers

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

Add the script to define the list of all supplier managers. This field is available when the **Advanced** option is selected on the User Criteria form. ```
<?xml version="1.0" encoding="UTF-8"?>
<unload unload_date="2026-02-24 08:43:14">
<user_criteria action="INSERT_OR_UPDATE">
<active>true</active>
<advanced>false</advanced>
<company/>
<department/>
<group/>
<location/>
<match_all>false</match_all>
<name>All supplier managers</name>
<role name="sn_slm.manager">da72c74043942110bb9e89e90db8f2ef</role>
<script><![CDATA[/** Scripted User Criteria is not cached, and evaluated everytime, so performance is dependent on the script.
* Populate `answer` with true/false or evaluate to true/false
* The script is evaluated in the scope the user criteria is defined
* Don't use `current` in the script or populate the variable
* Don't use `gs.getUser()` or  `gs.getUserID()`, 
* instead use `user_id` which contains the user sys_id against whom the evaluation is happening.
*/]]></script>
<short_description/>
<sys_class_name>user_criteria</sys_class_name>
<sys_created_by>maint</sys_created_by>
<sys_created_on>2026-02-24 08:43:10</sys_created_on>
<sys_domain>global</sys_domain>
<sys_domain_path>/</sys_domain_path>
<sys_id>0b4cfbbc50977250f8776d5de5c0693f</sys_id>
<sys_mod_count>0</sys_mod_count>
<sys_name>All supplier managers</sys_name>
<sys_package display_value="Global" source="global">global</sys_package>
<sys_policy/>
<sys_scope display_value="Global">global</sys_scope>
<sys_update_name>user_criteria_0b4cfbbc50977250f8776d5de5c0693f</sys_update_name>
<sys_updated_by>maint</sys_updated_by>
<sys_updated_on>2026-02-24 08:43:10</sys_updated_on>
<user/>
</user_criteria>
</unload>

```

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

**Note:** If you select **Match All**, verify that you don't create contradictory conditions that can never be met. For example, if all users in location A work for company G, the conditions in this example can never be met.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Configure user criteria for reassigning assessments](../concept/configure-user-criteria-for-reassigning-assessments.md)

