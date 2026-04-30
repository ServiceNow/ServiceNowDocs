---
title: Configure an ACL rule
description: Configure custom access control list \(ACL\) rules to secure access to new objects or to change the default security behavior.
locale: en-US
release: xanadu
product: Access Control
classification: access-control
topic_type: task
last_updated: "2025-10-03"
reading_time_minutes: 5
breadcrumb: [Access Control List Rules, Access Management]
---

# Configure an ACL rule

Configure custom access control list \(ACL\) rules to secure access to new objects or to change the default security behavior.

## Before you begin

Role required: security\_admin

## About this task

To create ACL rules, you must elevate privileges to the security\_admin role.

For tables that are in a different scope from the ACL rule record, the types of rules are limited. For Scope Master tables to derive scope and execute scoped ACLs, set the **glide.enforce\_security\_scope.&lt;scope\_name&gt;** property to **true**. This ensures ACLs in the global scope don’t match when there are scope-specific ACLs created on the relevant table. Examples are when securing data within shared application tables in the Global scope, such as sys\_attachment or sys\_question\_answer tables.

## Procedure

1.  [Elevated privilege roles](../../security/concept/c_ElevatedPrivilege.md) to the security\_admin role.

2.  Navigate to **System Security** &gt; **Access Control \(ACL\)**.

3.  Select **New**.

    **Tip:** When creating an ACL, it’s helpful to review the [Deny-Unless ACL](../concept/acl-denial-behavior.md).

4.  Complete the form.

<table id="table_uyy_41b_vx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select what kind of object this ACL rule secures. The type of object determines how the object is named and what operations are available. This field becomes read only after the ACL rule is created. If you want to change the type, you must delete the ACL and create one with the correct type.

</td></tr><tr><td>

Operation

</td><td>

Select the operation that this ACL rule secures. Each object type has its own list of operations. An ACL rule can only secure one operation. To secure multiple operations, create a separate ACL rule for each.If you’re creating a rule for a report\_view operation, see also [Report\_view access control](https://www.servicenow.com/docs/access?context=report-view-access-control&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Decision Type

</td><td>

Select the decision type of the ACL. **Allow If** allows access upon successful evaluation. **Deny Unless** denies access unless there’s successful evaluation.See [Deny-Unless ACL](../concept/acl-denial-behavior.md) for more information.

</td></tr><tr><td>

Admin overrides

</td><td>

Select this check box to have users with the admin role automatically pass the permissions check for this ACL rule. Admin users pass regardless of what script or role restrictions apply. However, the **nobody** role, which only ServiceNow personnel can assign, takes precedence over the admin override option. If an ACL is assigned the **nobody** role, admin users can’t access the resource even when **Admin overrides** is selected. See [Base system roles](https://www.servicenow.com/docs/access?context=r_BaseSystemRoles&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

 Clear this check box if administrators must meet the permissions defined in this ACL rule to gain access to the secured object. Since administrators always pass role checks \(see the description of the **Requires role** field\), use the condition builder or **Script** field to create a permissions check that administrators must pass.

</td></tr><tr><td>

Protection Policy

</td><td>

Select this to set the protection policy on the ACL

</td></tr><tr><td>

Name

</td><td>

Enter the name of the object being secured, either the record name or the table and field names. The more specific the name, the more specific the ACL rule. You can use the wildcard character asterisk \(\*\) in place of a record, table, or field name to select all objects that match a record type, all tables, or all fields. You can’t combine a wildcard character and a text search. For example, inc\* isn’t a valid ACL rule name, but incident.\* and \*.number are valid ACL rule names.**Note:** Select the blue triangle to manually enter the record name or the table and field names of the object being secured. Use this option to secure an object that doesn’t appear in the dropdown.

</td></tr><tr><td>

Description

</td><td>

Enter a description of the object or permissions that this ACL rule secures.

</td></tr><tr><td>

Applies To

</td><td>

Select **Add Filter Condition** to create a filter for the table selected in the **Name** field. The ACL applies only to the records matching this filter condition. For example, you could create an ACL for the incident table that applies only to incidents with the Critical priority.**Note:** You must select a table in the **Name** field to use this option. ACLs beginning with \* cannot use the **Applies To** filter.

</td></tr><tr><td>

Active

</td><td>

Select this check box to enforce this ACL rule.

</td></tr><tr><td>

Advanced

</td><td>

Select this check box to display the **Advanced Condition** fields. See step 6.

</td></tr></tbody>
</table>5.  To narrow the scope of the ACL fill in the **Conditions** fields as necessary.

<table id="id_ljx_cl3_ydc"><tbody><tr><td>

Requires role

</td><td>

Use this list to specify the roles a user must have to access the object. If you list multiple roles, a user with any one of the listed roles can access the object. The Requires role list appears as a related list.**Note:** Users with the admin role always pass this permissions check because the admin role automatically grants users all other roles.

</td></tr><tr><td>

Data Condition

</td><td>

Use this [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) to select the fields and values that must be true for users to access the object.**Note:** The Condition field is case-sensitive

</td></tr></tbody>
</table>6.  If the **Advanced** box is checked, fill in the **Advanced Conditions** fields as necessary.

<table id="id_cms_yl3_ydc"><tbody><tr><td>

Controlled by References

</td><td>

Enforces the ACL on related records. See  for more details.

</td></tr><tr><td>

Script

</td><td>

Enter a custom script describing the permissions required to access the object. The script can use the values of the current and previous [Global variables in business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=xanadu&pubname=xanadu-api-reference&section=c_UsingPredefinedGlobalVariables&ft:locale=en-US) as well as system properties. The script must generate a true or false response in one of two ways:-   return an answer variable set to a value of true or false
-   evaluate to true or false
 In either case, users only gain access to the object when the script evaluates to true and the user meets any conditions the ACL rule has. Both the conditions and the script must evaluate to true for a user to access the object.

If there’s script in the **Script** field. This script executes even if the field isn’t displayed on the form.

 **Note:** If the evaluated item is in a related list, **current** points to the item the related list is on, not to the current item the ACL is for. However, If the item you’re evaluating the ACL for isn’t in a related list, **current** points to the actual item.

</td></tr></tbody>
</table>    **Tip:** If there is script in the **Script** field. This script executes even if the field is not displayed on the form.

7.  Select and hold \(or right-click\) the form header and select **Save**.


