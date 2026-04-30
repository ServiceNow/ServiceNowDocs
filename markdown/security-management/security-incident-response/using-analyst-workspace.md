---
title: Working with Security Incident Records
description: The Security Incident Record consists of the following.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Using SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Working with Security Incident Records

The Security Incident Record consists of the following.

Key components available on a security incident record:

![Working with Security Incident Records](../image/key-features-security-incident-record.png "Key components of a security incident")

<table id="table_ijt_rl5_x5b"><thead><tr><th>

Number

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Security incident number

</td><td>

The security incident number is available against the tab name.

</td></tr><tr><td>

2

</td><td>

Short description

</td><td>

Short description of the security incident which is displayed above the form banner.

</td></tr><tr><td>

3

</td><td>

Form banner

</td><td>

This is read-only section, which contains the key fields such as Category, Priority, Risk score, State, and the incident assignment details.**Note:** The regular platform tags can be applied here as well.

</td></tr><tr><td>

4

</td><td>

Security tags

</td><td>

Displays the security tags associated with a security incident.

</td></tr><tr><td>

5

</td><td>

Overview

</td><td>

Provides a snapshot overview of the security incident such as Description, Business Impact comprising of asset details by type, affected users by criticality, Threat intelligence items comprising of observables by finding and by type, Response Tasks, Related security incidents comprising of child security incidents and similar security incidents.

</td></tr><tr><td>

6

</td><td>

Details

</td><td>

The details tab displays the security incident form.

</td></tr><tr><td>

7

</td><td>

Investigation

</td><td>

The Investigation tab displays the incident investigation experience.

</td></tr><tr><td>

8

</td><td>

Playbook

</td><td>

Playbook is triggered through Process Automation Designer \(PAD\). If a process is created, and if the a trigger condition is set to trigger the playbook for a security incident. Then a playbook appears.

</td></tr><tr><td>

9

</td><td>

Response Tasks

</td><td>

The Response Tasks captures all the response tasks associated with a security incident.

</td></tr><tr><td>

10

</td><td>

Related Records

</td><td>

The Related Records tab consists of all the related lists from the classic UI under this section. The related lists are grouped under various section such as business impact, threat intel, and so on for an easy navigation.

</td></tr><tr><td>

11

</td><td>

Other Records

</td><td>

Other records tab consists of IT records such as changes requests, incidents, and emails grouped and displayed in this section.

</td></tr><tr><td>

12

</td><td>

Post Incident Review tab

</td><td>

As the security incident progresses to the Review state, the Post Incident Review tab is displayed with the post incident assessments and reports within the tab.

</td></tr><tr><td>

13

</td><td>

Contextual menu

</td><td>

Provides easy access to the quick actions and is available across all the tabs for the analyst to access whenever required. The contextual menu provides easy navigation to the multiple resources such as:

 1.  Activity Stream
2.  Playbook
3.  Analyst Assist
4.  Runbook
5.  Templates
6.  Attachments

</td></tr><tr><td>

14

</td><td>

Form UI actions

</td><td>

The various security incident form UI actions are displayed on the top right of the incident form. The available form UI actions are:-   Discuss
-   Save
-   Create Response Task
-   Compose Email
-   Add Playbook
-   Open Associated Workflow\(s\)
-   Crete incident
-   Create Problem
-   Create Change Request
-   Create Outage
-   Calculate Severity
-   Link to Major Security Incident
-   Propose as Major Security Incident
-   Promote to Major Security Incident
-   Run Additional Action\(s\) on Endpoint
-   Associate MITRE ATT&amp;CK Technique
-   Switch to Classic UI
-   Add to Security Case
-   Delete

For more information, see [Working with Form UI actions](enable_workspace_form_ui_actions.md).

</td></tr></tbody>
</table>-   **[Security Incident Overview section](security-incident-overview.md)**  
The Overview section on the workspace presents the key information associated with the security incident.
-   **[Security Incident Details section](security-incident-details.md)**  
This section displays the security incident form fields that are rendered from the security incident classic UI.
-   **[SIR Workspace Orchestration](security-incident-response-workspace-orchestration-activities.md)**  
Security Incident Response Workspace orchestration activities will help the security analysts to view the investigation canvas and perform various actions that are applicable.
-   **[Security Incident Response Tasks](security-incident-response-tasks.md)**  
All the response tasks associated with a security incident are displayed within the Response Tasks section.
-   **[Security Incident Response Other Records](security-incident-response-other-records.md#)**  
This section displays the other records such as IT related records and email records. Under IT records, Incident, Change Request, Problem and Outages are displayed.
-   **[Security Incident Response Post Incident Review](security-incident-response-post-incident-review.md)**  
Post incident review appears when an incident is moved to a Review state.
-   **[Edit Related Records in list view](../task/edit-related-records-in-list.md)**  
Edit related records for a security incident directly from the Related Records list view. This allows security analysts to quickly update the records without leaving their current context.
-   **[TISC integration within SIR Workspace](../../secops-integration-threat-security-center/concept/tisc-sir-workspace.md)**  
The following section includes information about the Threat Intelligence Security Center integration from within the SIR workspace context.
-   **[Reports in Security Incident Response](report-templates-sir.md)**  
All the reports associated with a security incident are available within the Reports section for analysis and sharing.
-   **[Collaborate using conference call or chat in Security Incident Response](collab-sir-call-chat.md)**  
You can collaborate with analysts and affected users to resolve or discuss about an incident in Security Incident Response application.
-   **[Viewing incident details with a relationship graph](sir-relationship-graph.md)**  
Relationship graphs in the Security Incident Response workspace visually display the connections between a security incident and its related items to help you analyze the full context of a security incident.
-   **[MITRE attack and defend technique graph](mitre-attack-defend-graph-sir.md)**  
The MITRE attack and defend technique graph provides security analysts with an interactive, node-based visualization of attack techniques, defense techniques, and associated artifacts for a security incident.

**Parent Topic:**[Using SIR Workspace](../reference/using-sir-workspace.md)

**Related topics**  


[Security Incident Playbook](security-incident-playbook.md#)

[Prerequisites for the Playbooks](../../playbook-migration-guide/concept/getting-started-with-processes.md)

[Rebuilding existing playbooks in Workflow Studio](../../playbook-migration-guide/concept/rebuilding-existing-playbooks-on-pad.md)

[Activity Definitions](../../playbook-migration-guide/concept/build-activities.md)

[Sample Playbooks for SIR Workspace](../../playbook-migration-guide/concept/sir-workspace-playbooks.md)

[Working with MSI Records](working-with-msi-records.md)

[Working with Form UI actions](enable_workspace_form_ui_actions.md)

[Security Incident Closure workflow](security-incident-closure-workflow_0.md)

[Handle security incidents using AWA](../task/handle-incidents-using-awa.md)

