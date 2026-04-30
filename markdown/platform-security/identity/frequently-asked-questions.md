---
title: Frequently Asked Questions
description: Frequently asked questions while using the Access analyzer.
locale: en-US
release: xanadu
product: Identity
classification: identity
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Access Analyzer, Identity]
---

# Frequently Asked Questions

Frequently asked questions while using the Access analyzer.

## Evaluate Access

The following are some of the frequently asked questions while using the Evaluate Access feature in the Access Analyzer:

<table id="table_nrd_cpb_1yb"><thead><tr><th>

Questions

</th><th>

Explanation

</th></tr></thead><tbody><tr><td>

How to read the evaluation results displayed by the Access Analyzer?

</td><td>

Each row represents an individual access control list \(ACL\). The sequence \(\#\) in the results the order in which ACLs are evaluated. The status shows whether overall access is granted \(passed\) or denied \(blocked\).

</td></tr><tr><td>

How are ACLs Evaluated?

</td><td>

At a table level, ACLs are evaluated only for roles and security attributes, conditions and scripts aren’t evaluated.

 Roles are evaluated first. If Roles are blocked, conditions and scripts are skipped. For more information, see [Configure an ACL rule](../../../administer/contextual-security/task/t_CreateAnACLRule.md).

</td></tr><tr><td>

What are the legends in Access Analyzer?

</td><td>

When Analyzing the access and permissions, legends are displayed as part of the evaluation process. The following are the legends:

 -   \[Passed\] Access granted
-   \[Blocked\] Access denied
-   \[Skipped\] Didn’t evaluate
-   \[Undefined\] No rule found

</td></tr><tr><td>

What is the Alert icon in the Access results mean?

</td><td>

Alert Icon in any status indicates the presence of a script in the ACL. Review highlighted ACLs to understand the final access. To know more about how these controls are evaluated and review the logic to determine the access, see [Access Analyzer Debug logs](access-analyzer-logs.md).

</td></tr><tr><td>

What is **IAccesshandler**?

</td><td>

An internal system check using hidden source code on the platform. It’s a system security check that you can’t modify. **IAccessHandler** can grant or deny access to a resource without evaluating ACLs.

 If this **IAccessHandler** is ignored, then the ACLs are evaluated. You can’t modify the **IAccessHandler** checks in any way. For example, an **IAccessHandler** implementation is used for access checks on application resources such as read-only access.

</td></tr><tr><td>

What are data filters?

</td><td>

Data filters are a form of access control designed to work along with the existing Access Control rules \(ACLs\) on your instance.

</td></tr><tr><td>

What is an ACL rule?

</td><td>

Rules for access control lists \(ACLs\) restrict access to data by requiring users to pass a set of requirements before they can interact with it.

</td></tr></tbody>
</table>Time limited role assignments found for the user due to which the results may be impacted. You can review the time-limited roles assigned for the user here.

## Compare user records

The following are some of the frequently asked questions while using the Compare user record feature in the Access Analyzer:

|Questions|Explanation|
|---------|-----------|
|How to read the results on the Details tab?|The Details tab displays the metadata associated to the user 1 and user 2|
|How to grant a role to a user?|From the Users tab, you can check the role that must be granted for the user and assign that role.|
|How to add a user to a group?|From the Groups tab, you can check the group the user must be added and add the user to the group.|
|What is Show difference only?|When you enable the Show differences only check box, only the roles or group that are different between the user 1 and user 2 is displayed.|

## Compare user access

The following are some of the frequently asked questions while using the Compare user access feature in the Access Analyzer:

<table id="table_sj1_5w2_nzb"><thead><tr><th>

Questions

</th><th>

Explanation

</th></tr></thead><tbody><tr><td>

How to read the results on the access control comparison page?

</td><td>

The access control comparison page displays the evaluation states for different ACL operations.

</td></tr><tr><td>

What are the different evaluation states?

</td><td>

When comparing access controls between the users, following are the different evaluation states:

 -   Passed
-   Blocked

</td></tr><tr><td>

What is show differences only?

</td><td>

When you enable the Show differences only check-box, only the operation evaluation state that are different between the user 1 and user 2 is displayed.

</td></tr><tr><td>

How the ACL operation is evaluated?

</td><td>

Access control list \(ACL\) is the rule for access control lists \(ACLs\) that restrict access to data by requiring users to pass a set of requirements before they can interact with it. Within an ACL, the following hierarchy is evaluated:

 -   Role
-   Security Attribute
-   Condition
-   Script

</td></tr><tr><td>

How to read the results on the showing role hierarchy page?

</td><td>

The showing role hierarchy page displays the role that is assigned for user 1 and user 2. You can understand the role that is required for the user for a particular ACL operation.

</td></tr><tr><td>

How can I see the details of the user?

</td><td>

You can select the **User \(node\)** &gt; **More actions** &gt; **View user** details to know more about the user.

</td></tr><tr><td>

How can I see the details of the role?

</td><td>

You can select the **Role \(node\)** &gt; **More actions** &gt; **View role** details to know more about the role.

</td></tr><tr><td>

How can I see the details of the resources the role can access?

</td><td>

You can select the **Role \(node\)** &gt; **More actions** &gt; **View all resources that the role has access** to know the resources the role can access.

</td></tr><tr><td>

How can I see the details of the group?

</td><td>

You can select the **Group \(node\)** &gt; **More actions** &gt; **View group** details to know more about the group.

</td></tr></tbody>
</table>