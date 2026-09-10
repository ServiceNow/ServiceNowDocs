---
title: Group ownership in BIA, plan, and event records
description: Assign a user group as the owner of business impact analysis \(BIA\), plans, and event records, instead of or alongside an individual owner. Every member of the owner group gets the same access to these records as an individual owner.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/group-ownership-bias.html
release: zurich
topic_type: concept
last_updated: "2026-08-14"
reading_time_minutes: 11
keywords: [BCM, group ownership, owner group, BIA, business continuity plan, recovery event, team-based ownership]
breadcrumb: [Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Group ownership in BIA, plan, and event records

Assign a user group as the owner of business impact analysis \(BIA\), plans, and event records, instead of or alongside an individual owner. Every member of the owner group gets the same access to these records as an individual owner.

A comprehensive group ownership capability now enables organizational teams to collectively own and manage critical business continuity records. This feature is implemented across the business impact analysis \(BIA\), plans, and event records.

## Records enhanced

-   Business Impact Analysis \(BIA\) – Impact assessments owned by groups
-   Plans – Business continuity plans with team-based ownership
-   Events – Recovery and escalation events with collaborative ownership

## Why group ownership matters

Business continuity records including BIAs, plans, and recovery events often belong to a team or function rather than a single person. Traditional single-owner models create several challenges:

-   **Single point of failure**

    When the named owner leaves or changes roles, ownership becomes orphaned and records lack clear accountability.

-   **Maintenance overhead**

    Team composition changes require manual updates to individual ownership records across multiple business continuity assets.

-   **Role-based accountability**

    Some organizations require team-level rather than individual responsibility for critical record management and updates.


Group ownership addresses these issues by allowing ownership to be assigned at the team level, providing more flexible and durable team-based accountability.

## Owner and Owner group fields

Business continuity records now show two related ownership fields:

-   **Owner** – An individual user responsible for the record
-   **Owner group** – A group of users collectively responsible for the record

Either the **Owner** or the **Owner group** field is required to save the record. If you submit a record with both fields empty, an error message displays indicating the required fields.

-   **Default behavior**
    -   When you open a new record form, the current user is preselected as the owner.
    -   The **Owner group** field stays empty until you select a group.
    -   Clearing the preselected owner and saving with only an owner group results in an empty **Owner** field.
-   **Ownership validation**

    At least one ownership field must be populated before saving:

    -   If both the **Owner group** and **Owner** fields are empty, both fields highlight in red with an asterisk.
    -   A validation error message appears displaying: `Select either a group or an individual to save the record and proceed with the workflow.`
    -   An informational banner prompts you to populate at least one ownership field.
    -   The record can only be saved when at least one ownership field is populated.

## Owner group requirements and owner filtering

The **Owner group** field filters candidate groups based on role eligibility. Only groups that hold an eligible edit role are shown as selectable options. This confirms that groups shown in the owner field actually have the permissions needed to manage the record.

-   **Eligible groups and roles**

    Only groups that hold an eligible edit role are listed in the owner group lookup, whether or not the group currently has members.

    Eligible roles:

    -   BIA planner \(sn\_bia.bia\_planner\)
    -   BIA manager \(sn\_bia.bia\_manager\)
    -   Plan manager \(sn\_bcp.plan\_manager\)
    -   Plan contributor \(sn\_bcp.plan\_contributor\)
    -   Event manager \(sn\_recovery.event\_manager\)
    -   Event user \(sn\_recovery.event\_user\)
-   **Intelligent filtering behavior**

    The **Owner** and **Owner group** fields work together with intelligent filtering to verify the right people can be selected in the right order:

    -   Group selected first: The **Owner** field automatically filters to show only members of that group who hold an eligible role. This confirms the selected owner is part of the assigned team.
    -   Individual selected first: The **Owner group** field remains unfiltered. If a group is later selected and the individual is not a member of that group, the system allows the selection. An informational message displays rather than blocking the selection. This flexibility accommodates edge cases where an individual may serve as owner even if not formally part of the group.
    -   Neither field populated: Both fields remain unfiltered, matching legacy behavior before the group ownership feature.
-   **Selecting an owner outside the group**

    You can select an owner who isn't a member of the selected owner group.

-   **Group member filtering edge cases**

    If the selected owner group has no eligible members, the owner lookup returns no users.


For the role API names, see [Group owner fields and role requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/owner-group-eligibility-roles.md).

## Manage ownership scenarios

The following scenarios describe common ownership management tasks applicable across BIA, plan, and event records.

-   **Change the individual owner within a group**

    When a group is assigned as the owner group, you can designate or change the individual owner to any member of that group. The individual owner updates while the group ownership remains unchanged. If the individual owner leaves the group, the group ownership persists, and another group member is set to the new individual owner.

-   **Assign an owner outside the group**

    In some scenarios, you may assign an individual owner who is not a member of the selected owner group. The record saves with both the individual owner and the group. This supports use cases where an individual outside the group is responsible for the record while maintaining group-level visibility and responsibility.

-   **Revert from group ownership to individual ownership**

    You can remove group ownership and return to individual-only ownership at any time. The group field clears, and ownership reverts to individual-only mode with the selected individual as the sole owner of the record.

-   **Update owner after record submission \(BIA-specific\)**

    For Business Impact Analysis records, if an assessment is already submitted, changing the BIA owner does not sync the change to the assessment.

-   **Manage contributors and group membership changes**

    When contributors are added to or removed from a BIA, or when group members are added or removed, the system automatically syncs changes. This maintains real-time alignment between the record and related assessments \(BIA-specific\). During contributor synchronization from the BIA to the assessment, the member assigned to the **BCM lead** field is also synced to the assessment.

-   **Contributor access is independent of group ownership**

    Being listed as a contributor on a BIA does not grant the access level of an owner group member. Being a member of the owner group does not add you to the contributor list. These are two independent access mechanisms: contributor access is controlled by the contributor list, and owner group access is controlled by group membership. A user may need a separate role assignment to access the BCM workspace even if they hold one of these two access types.


## BIA owner fields and contributor synchronization

When a BIA is created, the **BIA Owner**, **BIA Owner group**, and **BCM Lead** fields are automatically synced to the assessment. Additionally, any contributors added to the BIA are also synced to the assessment.

-   **Detailed behavior**
    -   When creating a BIA, the **BIA Owner**, **BIA Owner group**, and **BCM Lead** fields are synced to the assessment
    -   If you add contributors to the BIA \(for example, Abel Tuter\), these contributors are synced to the assessment
    -   Contributors can access the BIA if they have the proper role
    -   The synced contributors appear in the assessment's contributor list
-   **Auto-sync on removal**
    -   If you remove any contributor from the BIA, it automatically syncs and removes them from the assessment
    -   This verifies the assessment reflects the current BIA contributor list
-   **One-way sync and assessment-level customization**

    Contributor synchronization flows in one direction only, from the BIA to the assessment. Contributors added directly in the assessment view aren't synced back to the BIA contributor list.

    When you add or remove a contributor on the BIA, only that change syncs to the assessment. Existing assessment-level customizations to the contributor list aren't overwritten.

    You can add a contributor to a specific assessment without affecting other assessments linked to the same BIA. For example, if a BIA has multiple linked assessments and you add a contributor to only one assessment, that contributor isn't automatically added to the BIA's other assessments.

-   **BIA Owner change behavior**

    -   If you change the BIA owner from one user to another user and save the record, the assigned owner in the assessment gets updated
    -   When accessing the assessment after owner change, the "assigned to" field will show the new owner \(for example, planner instead of manager\)
    **Note:** If an assessment is already submitted, changing the BIA owner does not sync the change to the assessment. When you change the BIA owner after submission, a message displays indicating that the assessment is not synced because it's already submitted.


## Smart Assessment owner assignment

When a BIA uses a Smart Assessment template and the BIA owner field is empty, the assessment owner defaults according to the following priority:

-   Group manager – If the owner group has a designated manager
-   First group member – If the group has members but no manager
-   Skip assessment – If the group has no members; a warning is logged, and no user-facing error appears

The following example shows a contributor list from the assessment view. Contributor synchronization between a BIA and its Smart Assessment is one-way: contributors added to or removed from the BIA sync to the assessment, but contributors added directly in the assessment view don't sync back to the BIA.

\[Omitted image "bia-sa-sync-contri-list.png"\] Alt text: Contributor list.

-   **Explicit Owner override**

    When a BIA has an explicit owner \(individual\), the assessment owner is the BIA owner, regardless of the owner group setting.


## Record-specific implementation

While group ownership works consistently across BIA, plan, and event records, each record type has specific synchronization and workflow integration behaviors.

## Business Impact Analysis \(BIA\) records

BIA records include unique synchronization with Smart Assessment templates:

-   When a BIA owner or owner group is set, the owner automatically syncs with the associated assessment
-   Contributors added to the BIA sync to the assessment contributor list
-   Assessment owner defaults to the group manager or first group member if BIA owner is not explicitly selected
-   Explicit individual owners always take precedence over group-based defaults

## Plan records

Business Continuity Plan records provide team-based maintenance accountability:

-   Plans support group ownership across both UI Builder and Classic UI workspaces with identical behavior
-   Group ownership works seamlessly with existing automation and workflows built on individual assignment
-   Plan records require backward compatibility—existing single-owner plans continue to function unchanged
-   Group ownership is optional; records do not require a group to be valid

## Recovery Event records

Recovery Event records coordinate team-based incident response and escalation:

-   Event records support group ownership to ensure all responders have equal access and accountability
-   Owner group changes propagate to escalation rules and notification workflows
-   Event manager and event planner roles are eligible for owner group assignment

## Owner group field access by role and record state

Field edit permissions vary by user role and record state:

|Role|Draft|In Review|Returned|Other States|
|----|-----|---------|--------|------------|
|Manager|Edit|Read-only|Read-only|Read-only|
|Admin|Edit|Edit|Edit|Read-only|
|Other roles|Read-only|Read-only|Read-only|Read-only|

BCM Managers can edit the owner group only while records are in Draft state. BCM administrators can edit during Draft, In Review, and Returned states. In all other states and for all other roles, the field is read-only.

## Key capabilities

|Area|Details|
|----|-------|
|Data model|Added owner\_group reference field with multi-level group hierarchy filtering and reference qualifiers|
|User interface|Form sections, list-view columns, and workspace layouts display and enable ownership management|
|Permissions|Collaborator-aware ACLs: group members receive read/write access; non-members receive read-only access|
|Workflows|Group ownership integrated into record state transitions, approvals, and escalation rules|
|Document export|Group ownership details are covered in the PDF and Word reports|
|Copy and clone|When you copy a plan, the new record inherits both the original owner and owner group. When you copy a BIA, the new record inherits only the original owner group. The system automatically assigns the current user as the individual owner of the copied BIA.|
|Audit trail|Historical logging tracks ownership changes and group member role transitions|
|Smart Assessment|Assessment owners default to group manager or first group member when BIA owner is not selected|

## Workspace parity

The **Owner group** field, mandatory validation, group-based filtering, and field access rules function identically in the Business Continuity Workspace and the Classic workspace.

## Backward compatibility

The group ownership feature is fully backward compatible with existing Business Continuity Management implementations:

-   Existing BIA, plan, and event records with only an individual owner continue to work unchanged
-   Automation and workflows that reference the individual owner field are unaffected
-   Users who do not select a group see exactly the same unfiltered individual owner field behavior as before the group ownership feature
-   The group field is optional; records do not require a group to be valid
-   On record creation, the current user is still pre-populated as the individual owner by default, with the group field remaining empty
-   All existing integrations, API calls, and third-party tools continue to operate without modification

**Related topics**  


[Create a business impact analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-bia-in-uib-ws.md)

[Create a business continuity plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-bcp-plan-in-uib-ws.md)

[Create an exercise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/start-exercise-event-in-uib-ws.md)

[Group owner fields and role requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/owner-group-eligibility-roles.md)

[BIA owner field reference and validation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/bia-smart-assessment-owner-sync.md)

