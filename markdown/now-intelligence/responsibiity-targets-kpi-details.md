---
title: Responsibility for global indicator targets
description: A user can be responsible for targets on one or more Performance Analytics indicator/breakdown combinations \(KPIs\). Responsible users are expected to track progress towards the targets and can change the targets on their KPIs.After an admin creates a target, assign responsibility for reviewing and editing the target to a subject matter expert \(SME\) in the business area.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Targets and thresholds, KPI Details, Platform Analytics experience, Platform Analytics]
---

# Responsibility for global indicator targets

A user can be responsible for targets on one or more Performance Analytics indicator/breakdown combinations \(KPIs\). Responsible users are expected to track progress towards the targets and can change the targets on their KPIs.

Responsibility is separate from access control list \(ACL\)-based roles. A target admin role, such as pa\_target\_admin, allows a user to create and edit global targets on any unique indicator/breakdown element combination \(referred to here as a KPI\). Such a role is normally restricted to a few Performance Analytics experts. However, a business-area expert, such as a manager, is likely to know more about the appropriate target to set for a specific KPI. Conversely, a Performance Analytics expert is unlikely to be able to maintain appropriate targets for all the KPIs in their organization.

Here the concept of responsibility comes in. A user with any role can be responsible for managing a KPI's global targets, which everyone can see. They can create a new target or edit the target for any KPI they are responsible for. Responsible users can create or edit their targets either in KPI Details or the classic Analytics Hub. However, they have this right only for KPIs that they were explicitly made responsible for. Also, if ACLs prohibit a user from viewing a KPI, they cannot be responsible for that KPI.

Only users, not groups, can have responsibility. Responsible users can assign responsibility for their KPIs to other users or remove responsibility from other users or themselves. A user can be responsible for the targets of multiple KPIs, and a KPI can have multiple users responsible for its targets.

**Note:** Responsibility for targets is independent of any other responsibility for a KPI, such as responsibility for signals.

A user with a target admin role has to create the initial global target for a KPI. After they create that target, they can assign responsibility to any user with any role, if the user can view the KPI. The responsible users maintain the targets for that KPI thereafter. The expected workflow follows:

1.  A target admin creates an initial global target on a KPI. This target can be a meaningful value, or it can be a placeholder that a responsible user is expected to change.
2.  The target admin makes themselves or a different user responsible for targets on the KPI.
3.  At any point, the responsible users make other users responsible or remove responsibility from users.
4.  The responsible users replace or edit targets for which they are responsible.

**Note:** You can assign responsibility to targets only in KPI Details. You cannot assign responsibility from a KPI Targets component.

## Assign responsibility for targets

After an admin creates a target, assign responsibility for reviewing and editing the target to a subject matter expert \(SME\) in the business area.

### Before you begin

Role required: pa\_admin, pa\_target\_admin, pa\_power\_user, or admin.

### Procedure

1.  Open KPI Details in a Workspace.

2.  Either:

    -   Create a target, as described in [Create a target in KPI Details](../task/create-kpi-details-targets.md).
    -   Open an existing target, as described in [Edit targets in KPI Details](../task/edit-multiple-targets.md).
3.  Click the cogwheel to open the **Targets Configuration** page.

    ![Targets panel top showing config cogwheel.](../image/kpi-details-target-config-cogwheel.png)

    The **Targets configuration** view opens.

4.  Open the Responsibility tab.

    ![Selecting the Responsibility tab in Targets Configuration.](../image/kpi-details-targets-responsibility.png)

5.  Select one or more unique indicator/breakdown element combinations \(KPIs\).

6.  In the **Editing configuration items** panel, select one or more users to be responsible.

    You can select only one user at a time, but you can repeat the selection process as often as you want. Only users who can view all selected KPIs are available.

    ![Selecting responsible users.](../image/kpi-details-targets-select-resp-user.png)

7.  Click **Update**.


### Result

The users you selected appear in the **Responsible users** column for the KPIs you selected.

