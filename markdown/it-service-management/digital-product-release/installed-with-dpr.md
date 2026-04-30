---
title: Components installed with Digital Product Release
description: Several types of components are installed with activation of the Digital Product Release app, including tables and user roles.
locale: en-US
release: xanadu
product: Digital Product Release
classification: digital-product-release
topic_type: reference
last_updated: "2025-07-22"
reading_time_minutes: 4
breadcrumb: [Digital Product Release reference, Digital Product Release, IT Service Management]
---

# Components installed with Digital Product Release

Several types of components are installed with activation of the Digital Product Release app, including tables and user roles.

## Roles installed

<table id="table_ekr_sp5_lyb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Product Enhancement Read

 \[sn\_dpr\_model.product\_enhancement\_read\]

</td><td>

Reads product enhancements in a product or service.

</td><td>

None

</td></tr><tr><td>

Product Feature Create

 \[sn\_dpr\_model.product\_feature\_create\]

</td><td>

Creates product features in a product or service.

</td><td>

None

</td></tr><tr><td>

Product Feature Delete

 \[sn\_dpr\_model.product\_feature\_delete\]

</td><td>

Deletes product features in a product or service.

</td><td>

None

</td></tr><tr><td>

Product Feature Read

 \[sn\_dpr\_model.product\_feature\_read\]

</td><td>

Reads product features in a product or service. Can’t create or modify a product feature.

</td><td>

None

</td></tr><tr><td>

Product Feature Write

 \[sn\_dpr\_model.product\_feature\_write\]

</td><td>

Updates product features in a product or service.

</td><td>

None

</td></tr><tr><td>

Digital Product Manager

 \[sn\_dpr\_model.product\_manager\]

</td><td>

Manages digital products and services.

</td><td>

-   asset
-   pd\_operator
-   model\_manager
-   sn\_devops.app\_owner
-   sn\_change\_write
-   sn\_dpr\_model.product\_feature\_create
-   sn\_dpr\_model.product\_feature\_delete
-   sn\_dpr\_model.product\_feature\_read
-   sn\_dpr\_model.product\_feature\_write
-   sn\_dpr\_workspace.workspace\_user
-   sn\_gf.goal\_user\_read
-   sn\_pace.code\_reader
-   sn\_pace.execution\_reader
-   sn\_pace.mapping\_admin
-   sn\_pace.policy\_reader
-   task\_editor
-   template\_read\_global

</td></tr><tr><td>

Digital Product Release Admin

 \[sn\_dpr\_model.release\_admin\]

</td><td>

Defines the release process and monitors the release.

</td><td>

-   pd\_operator
-   sn\_change\_write
-   sn\_devops.tool\_owner
-   sn\_devops.viewer
-   sn\_dpr\_model.product\_feature\_read
-   sn\_dpr\_workspace.workspace\_user
-   sn\_gf.goal\_user\_read
-   sn\_incident\_read
-   sn\_pace.admin
-   sn\_pace.mapping\_admin
-   sn\_problem\_read
-   sn\_request\_read
-   task\_editor
-   template\_editor\_global

</td></tr><tr><td>

Digital Product Release Coordinator

 \[sn\_dpr\_model.release\_coordinator\]

</td><td>

Helps product teams in their responsibilities.

</td><td>

-   pd\_operator
-   sn\_change\_write
-   sn\_devops.viewer
-   sn\_dpr\_model.product\_feature\_read
-   sn\_dpr\_workspace.workspace\_user
-   sn\_gf.goal\_user\_read
-   sn\_incident\_read
-   sn\_pace.code\_reader
-   sn\_pace.execution\_reader
-   sn\_pace.mapping\_admin
-   sn\_pace.policy\_reader
-   sn\_problem\_read
-   sn\_request\_read
-   task\_editor
-   template\_read\_global

</td></tr><tr><td>

Digital Product Release User

 \[sn\_dpr\_model.release\_user\]

</td><td>

Accesses Digital Product Release Workspace to view release details and update and approve release tasks. Can’t create or modify releases.

</td><td>

-   sn\_change\_read
-   sn\_devops.viewer
-   sn\_dpr\_model.product\_feature\_read
-   sn\_dpr\_workspace.workspace\_user
-   sn\_gf.goal\_user\_read
-   sn\_incident\_read
-   sn\_pace.policy\_reader
-   sn\_problem\_read
-   sn\_request\_read
-   task\_editor

</td></tr><tr><td>

Digital Product Release Workspace User

 \[sn\_dpr\_workspace.workspace\_user\]

</td><td>

Accesses Digital Product Release Workspace.

</td><td>

cmdb\_read

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_gkr_sp5_lyb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Clean 6 month old unused release target

</td><td>

Deletes release target records older than six months and unused.

 Runs: Daily

</td></tr><tr><td>

DPR Execute policies for all active release phases

</td><td>

Runs policies that are mapped to phases that are currently in progress for all releases.

 Runs: Daily

</td></tr><tr><td>

Release phase state transition

</td><td>

Manages the state of phases for ongoing releases.

 This job checks all in-progress releases and their phases. If a phase is in progress and its planned end date is today, and its policy status is compliant, it will be marked as completed and the next phase will begin.

 Runs: Every hour

</td></tr><tr><td>

Release state transition

</td><td>

Manages the states of Pending or In progress releases.

 -   If a release is in the Pending state and its planned start date is today, its state is updated to In progress.
-   If a release is in the In progress state and all its phases are completed, its state is updated to Review.

 Runs: Every hour

</td></tr></tbody>
</table>## Tables installed

<table id="table_ikr_sp5_lyb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approval Definition

 \[sn\_dpr\_model\_approval\_definition\]

</td><td>

Approval definitions that are used to direct approval requests for release tasks to a user or user group.

</td></tr><tr><td>

Key Date

 \[sn\_dpr\_model\_release\_key\_date\]

</td><td>

Release key dates that define milestones, key events, deadlines, and important dates for single or recurring releases.

</td></tr><tr><td>

Policy

 \[sn\_dpr\_pace\_policy\_mapping\]

</td><td>

Policies mapped to a release. Extends the Policy Mapping table \[sn\_pace\_policy\_mapping\] from PaCE.

</td></tr><tr><td>

Product Enhancement

 \[sn\_dpr\_model\_product\_enhancement\]

</td><td>

Product enhancements of a product feature.

 Use these product enhancements to release a product feature in phases across multiple versions.

</td></tr><tr><td>

Product Feature

 \[sn\_dpr\_model\_product\_feature\]

</td><td>

A product feature is a function or capability that adds value to a product or service for the customer.

 You can break down a product feature into product enhancements to release it in phases across multiple versions.

</td></tr><tr><td>

Related Tasks

 \[sn\_dpr\_model\_release\_related\_task\_m2m\]

</td><td>

Mapping between records from the Task table \(task\) and release records in the Release table \(sn\_dpr\_model\_release\).

</td></tr><tr><td>

Release

 \[sn\_dpr\_model\_release\]

</td><td>

A product or service release is the process of releasing a new version of a product or service. It involves several phases, tasks, policies, and approvals.

</td></tr><tr><td>

Release Artifact

 \[sn\_dpr\_model\_release\_artifact\]

</td><td>

Artifacts in a release for a product.

</td></tr><tr><td>

Release Association

 \[sn\_dpr\_release\_association\]

</td><td>

Relationships between a release and the associated release template.

</td></tr><tr><td>

Release Bundle

 \[sn\_dpr\_model\_release\_bundle\]

</td><td>

Release bundles are groupings of releases that can be tracked concurrently.

</td></tr><tr><td>

Release Bundle M2M

 \[sn\_dpr\_model\_release\_bundle\_m2m\]

</td><td>

Relationships of releases that are grouped into various release bundles.

</td></tr><tr><td>

Release Calendar

 \[sn\_dpr\_model.release\_calendar\]

</td><td>

Calendars that can contain related release readiness targets within them. Release calendars can have exclusion schedules attached to them so that no release targets are created on dates that fall within those exclusion schedules.

</td></tr><tr><td>

Release Phase

 \[sn\_dpr\_model\_release\_phase\]

</td><td>

Phases in a release for a product or service.

</td></tr><tr><td>

Release Phase CI

 \[sn\_dpr\_model\_release\_phase\_ci\_m2m\]

</td><td>

Mapping of configuration items and phases of a release.

</td></tr><tr><td>

Release Phase CR

 \[sn\_dpr\_model\_release\_phase\_cr\]

</td><td>

Mapping of change requests and phases of a release.

</td></tr><tr><td>

Release Phase M2M

 \[sn\_dpr\_release\_phase\_m2m\]

</td><td>

Mapping of releases and phases to the policies that are mapped to each phase.

</td></tr><tr><td>

Release Policy Execution

 \[sn\_dpr\_policy\_execution\]

</td><td>

Results of policies run ona phase ofa release.

</td></tr><tr><td>

Release Readiness Target

 \[sn\_dpr\_model\_release\_target\]

</td><td>

Release readiness target that defines schedules for a single or recurring releases.Release targets are added to a release calendar.

</td></tr><tr><td>

Release Task

 \[sn\_dpr\_model\_release\_task\]

</td><td>

Tasks in phases for a release.

</td></tr><tr><td>

Release Template

 \[sn\_dpr\_model\_release\_template\]

</td><td>

Release templates containing predefined phases, tasks, approvals, and policies. While creating a release, you can apply a release template to pre-populate these phases, tasks, approvals, and policies.

</td></tr><tr><td>

Work Item

 \[sn\_dpr\_model\_product\_enhancement\_work\_item\_mapping\]

</td><td>

Mapping between product enhancements and work items\(records in the Work Item table \(sn\_devops\_work\_item\)\).

</td></tr></tbody>
</table>**Parent Topic:**[Digital Product Release reference](../concept/dpr-reference.md)

