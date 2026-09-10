---
title: Creating global recovery teams and collaboration threads
description: Recovery teams and collaboration help organizations coordinate business continuity responses using reusable teams and integrated communication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/recovery-team-collaboration.html
release: zurich
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 5
keywords: [recovery team, business continuity management, collaboration, crisis coordination, BCM]
breadcrumb: [Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Creating global recovery teams and collaboration threads

Recovery teams and collaboration help organizations coordinate business continuity responses using reusable teams and integrated communication.

## Recovery team management

Starting with BCM core release 12.x.x, recovery teams are supported at global level and they are available across all BCM applications. BCM users can now create and store recovery teams to address defined problems and fulfill organizational requirements. Key features include an active flag for recovery teams, support for global recovery teams, ability to reference saved recovery teams within plans, and enhanced recovery team hierarchy management.

## Recovery teams module in Business Continuity Workspace

BCM administrators can create and manage recovery teams from the Recovery teams module in Business Continuity Workspace.

\[Omitted image "recovery-teams-module.png"\] Alt text: Recovery teams module.

## Benefits of using recovery teams

Implementation of BCM Recovery team and Collaboration functionality delivers measurable benefits:

|Benefit|Details|
|-------|-------|
|Centralized tracking|Eliminates scattered Excel spreadsheets and fragmented communication. All event-related collaborations, decisions, and actions are captured in a single platform.|
|Re-usability|Recovery teams are created once and can be associated with multiple recovery plans and events, reducing administrative overhead and ensuring consistent team definitions across the organization.|
|Hierarchical organization|Parent-child team relationships enable modeling of complex organizational structures \(site-level, country-level, global teams\) with automatic cycle prevention.|
|Audit trail|Built-in activity streams and historical records capture all decisions, actions, and communications for compliance requirements and post-event analysis.|
|Real-Time coordination|Integrated collaboration threads, email capabilities, and action tracking keep all team members aligned during crisis events without context switching to external tools.|
|Automatic recipient resolution|Email notifications automatically resolve team membership including nested groups, eliminating manual recipient management during urgent situations.|

## Capabilities and use cases

The BCM recovery team and collaboration functionality provides key capabilities for coordinating business continuity responses.

|Capability|Description|Use case|
|----------|-----------|--------|
|Team management|Create reusable recovery teams with hierarchical structures, configurable membership, location association, and lifecycle management|Site Evacuation Team reports to Regional Safety Team, which reports to Global Recovery Coordination Team|
|Collaboration threads|Capture discussions, decisions, coordination, action items, and email communications with timeline and attachments|Fire incident: Evacuation Team documents decisions, Safety Team reports status, Facilities Team assigns restoration tasks|
|Crisis event coordination|Automatically notify recovery team leads with context about impacted assets and recovery objectives|Crisis declared: team members receive notifications enabling immediate action without manual coordination|
|Escalation and routing|Tag events with crisis levels and automatically resolve team recipients including nested group members|High crisis level signals executive teams; system resolves all recipients eliminating manual email management|
|Multi-team coordination|Parent-child team hierarchies enable coordination between specialized teams with organizational oversight|Data Recovery team reports to Infrastructure Recovery team; Site Evacuation to Regional Safety to Global Recovery|
|Exercise and planning|Participate in exercises and tabletop discussions with automatic capture of decisions and actions|Recovery teams join exercises; all decisions captured for improvement tracking without manual spreadsheet updates|
|Plan development|Select pre-configured teams from global repository ensuring consistent definitions across all plans|Administrators reuse teams across plans; updates to team definitions benefit all referencing plans and events|
|Post-event analysis|Complete collaboration thread serves as authoritative record capturing all activity, decisions, and actions|Resolved events provide comprehensive audit trail for post-event reviews, compliance, and improvement planning|

## Components used in recovery teams

The global recovery team consists of the following components:

|Component|Description|
|---------|-----------|
|Tables|
|`sn_bcm_recovery_team`|Core table storing recovery team records with fields for name, description, location, and active status|
|`sn_bcm_m2m_recovery_team_user`|Junction table linking users to recovery teams with automatic department mapping for picker filters|
|`sn_bcm_m2m_recovery_team_group`|Junction table linking groups to recovery teams, supporting recursive group membership resolution|
|`sn_bcm_m2m_recovery_team_recovery_team`|Self-join hierarchy table supporting parent-child team relationships with automatic cyclic-relationship prevention|
|`sn_bcp_m2m_plan_recovery_team`|Junction table linking recovery teams to recovery plans|
|Access control|
|core\_viewer|Read and report-view access to recovery team records|
|core\_manager|Create, write, delete, and management permissions for recovery teams. These roles extend to all related records including collaboration threads and email communications.|
|Rules|
|Business rules|Validate parent-child relationships and prevent invalid team hierarchies. The system prevents cyclic relationships and self-loops automatically, maintaining data integrity during team configuration.|

## Key capabilities

Recovery teams and collaboration provide the following key capabilities:

-   Team management and planning
    -   Create reusable teams with hierarchical structures and configurable membership
    -   Reference teams across multiple recovery plans with automatic filtering of active teams
-   Collaboration and communication
    -   Coordinate through integrated threads with automated email notifications and recipient resolution
    -   Track activity streams, delivery status, attachments, and role-based work notes
-   Event escalation and tracking
    -   Tag events with crisis levels to indicate severity and control access
    -   Maintain persistent escalation values across all event views
-   Documentation and reporting
    -   Export complete recovery timeline to Word and PDF with collaboration threads and event details
    -   Automatically propagate email history and activity updates to parent crisis event feed

**Related topics**  


[Create and manage a recovery team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-recovery-team.md)

[List view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/list-view-uib-ws.md)

[Recovery teams, loss scenarios, and recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/recovery-teams.md)

[Creating collaborations in exercises and crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/creating-collaboration-threads-in-crisis.md)

[Create a collaboration thread in a crisis event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/compose-email-collaboration-thread-crisis.md)

[Create Collaboration thread form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-collaboration-thread-crisis-event-form.md)

