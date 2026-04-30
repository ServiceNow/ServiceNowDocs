---
title: Explore Scripting Governance Tool
description: The Scripting Governance Tool \(SGT\) provides a single, centralised control for managing scripting access across your ServiceNow AI Platform.
locale: en-US
release: zurich
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-04-06"
reading_time_minutes: 5
keywords: [Scripting Governance Tool, SGT, scripting, Conditional Script Writer]
breadcrumb: [Scripting Governance Tool, Access Management]
---

# Explore Scripting Governance Tool

The Scripting Governance Tool \(SGT\) provides a single, centralised control for managing scripting access across your ServiceNow AI Platform.

The Zurich release introduces a feature that gives administrators centralised control over who can edit script fields on the ServiceNow AI Platform. The feature adds a new permission layer built on the **Conditional Script Writer** group and its child role, `snc_required_script_writer_permission`. Users must be members of this group to edit any script field, regardless of their existing ACL-based access. This permission layer is enforced through data-type ACLs and maintained by scheduled jobs and system properties.

To manage this feature, ServiceNow AI Platform provides the **Scripting Governance Tool \(SGT\)** — a dashboard where administrators can see which users have scripting access, scan the instance for users who have edited script fields, and directly add or revoke scripting access from users.

## Why it matters

Scripting can read and write data across tables, bypass business logic, and alter platform behaviour at a fundamental level making scripting access one of the most important permissions to govern on any instance.

Before Zurich, scripting access was controlled solely by ACLs on individual script fields. To determine which users could edit scripts, administrators had to check each ACL individually. There was no single place to view or manage scripting access across the instance.

Scripting governance feature addresses it by adding a mandatory second layer of access control on top of existing ACL-based permissions. Satisfying a field-level ACL alone is no longer sufficient to edit a script field. Now, security administrators can manage scripting access centrally by adding or removing users from the **Conditional Script Writer** group.

## The two-layer access model

Scripting governance feature enforces a two-layer access model. Both layers must pass independently before a user can edit any script field. Passing one layer alone is not sufficient.

-   **Layer 1 — Existing field-level ACL**

    The user must pass the existing ACL on the scripting field \(out-of-the-box or custom\). This check is unchanged from pre-Zurich behaviour.

-   **Layer 2 — SGT role check**

    The user must also hold the `snc_required_script_writer_permission` role, which is granted through membership in the **Conditional Script Writer** group.


**Important:**

A user who could edit script fields before the Zurich upgrade — because their roles satisfied the field-level ACL — will be blocked after the upgrade unless they also satisfy Layer 2. The `snc_required_script_writer_permission` role does not grant new scripting access on its own. It only unlocks access for users who already pass Layer 1.

The following table summarises access outcomes under the two-layer model:

|Passes field-level ACL \(Layer 1\)?|Holds `snc_required_script_writer_permission` \(Layer 2\)?|Can edit script field?|
|-----------------------------------|----------------------------------------------------------|----------------------|
|Yes|Yes|✅ Yes|
|Yes|No|❌ No|
|No|Yes|❌ No|
|No|No|❌ No|

## Data type ACLs

Scripting governance feature introduces 9 data type ACLs to enforce Layer 2. These are **deny unless** ACLs that require the `snc_required_script_writer_permission` role for the following data types:

-   **Data type**

    -   script
    -   script\_client
    -   script\_plain
    -   script\_server
    -   email\_script
    -   html\_script
    -   html\_template
    -   xml
    -   condition\_string
    **Note:** The admin role does not have scripting access by default. Admin users are subject to the same two-layer check and cannot edit script fields unless they are members of the **Conditional Script Writer** group or explicitly hold the `snc_required_script_writer_permission` role.To know more, see [Datatype ACL](../../contextual-security/concept/datatype-acl.md).


## Scheduled jobs and properties

As part of the scripting governance feature, the **Conditional Script Writer** group is introduced, which has the `snc_required_script_writer_permission` role as a child role. When the Zurich upgrade completes, a one-time scheduled job runs to auto-populate all eligible users to this group ensuring no one loses scripting access after the upgrade. Once that job completes, a recurring weekly job is created to keep the group membership up to date. Both jobs and their eligibility criteria are described as follows:

-   **Add users to Conditional Script Writer group**

    A job that runs once immediately after the Zurich upgrade completes. It adds all users who meet the eligibility criteria to the **Conditional Script Writer** group, ensuring no user loses scripting access after the upgrade. After the job completes, the platform disables it.

    The job uses the property `glide.security.scripting_role.provisioning_job_running`, which is set to true while the job is running and false after it completes. When the job finishes, it creates the property `glide.security.scripting_role.auto_provisioning` and sets it to **true**.

-   **Update users in Conditional Script Writer group**

    A weekly job that adds new users who meet the eligibility criteria to the group and removes users who no longer meet the eligibility criteria. It is controlled by the `glide.security.scripting_role.auto_provisioning` property:

    |Value|Behaviour|
    |-----|---------|
    |true \(default\)|The weekly job runs on schedule and adds qualifying users to the group automatically.|
    |false|The job does not run. Users are only added to the group manually by an administrator.|

    To disable automatic provisioning, set `glide.security.scripting_role.auto_provisioning` to **false** in System Properties.

    **Note:** The `glide.security.scripting_role.auto_provisioning` property is created at runtime and has a different **sys\_id** on every instance. Always reference it by a property name.


## Eligibility criteria

Both scheduled jobs use the same criteria to determine which users are added to the **Conditional Script Writer** group:

|Explicit Role plugin|User type|Requirement|Added to group?|
|--------------------|---------|-----------|---------------|
|Enabled|External|—|No|
|Enabled|Internal|Must have snc\_internal and at least one additional role|Yes|
|Disabled|Any user|Must have at least one role|Yes|

**Note:** The **snc\_external** role and the `snc_required_script_writer_permission` role are conflicting roles. ServiceNow AI Platform does not allow both role to the same user. External users cannot have scripting access.

## Scripting Governance Tool

The **Scripting Governance Tool** is a dashboard that helps administrators manage scripting access on the ServiceNow platform. It provides visibility into users who are members of the **Conditional Script Writer** group — giving a clear picture of how many users can script on your instance.

You can also view which groups contain the scripting role and which roles contain it as a child role. There are two ways to manage scripting access through the tool:

-   **Manual configuration**: Manually add or remove users from the **Conditional Script Writer** group to control who has scripting access.
-   **Scan for users who have scripted**: Scan your instance to find users who have scripted within a specific time frame. The scan queries the audit logs and identifies any user who has performed write or update to a table having script field.

![Scripting Governance Tool dashboard](../image/scripting-governance-dashboard.png)

**Note:** It is recommended to manage scripting access exclusively through the **Conditional Script Writer** group. Adding the `snc_required_script_writer_permission` role as a child role to other roles or groups reduces your ability to centrally control who can script on your instance.

