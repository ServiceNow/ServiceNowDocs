---
title: Edit Related Records in list view
description: Edit related records for a security incident directly from the Related Records list view. This allows security analysts to quickly update the records without leaving their current context.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-10-27"
reading_time_minutes: 2
breadcrumb: [Working with Security Incident Records, Using SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Edit Related Records in list view

Edit related records for a security incident directly from the Related Records list view. This allows security analysts to quickly update the records without leaving their current context.

## Before you begin

Use cases:

-   Analyst can update the severity and confidence levels of multiple IP address observables directly within the incident workspace.
-   Analyst can manage multiple findings by updating status and assignee inline from the workspace view. This enhances SOC team coordination during active investigations.
-   Analyst can enrich observables with updated descriptions and attributes as new information becomes available instantly.

Limitations:

-   Complex field dependencies may still require accessing the full form for accurate updates.
-   Certain advanced field types, such as **Modified**, are not supported for inline editing.
-   Bulk editing is restricted for non-compatible field types and logically grouped items.

**Note:** The following are the example steps for updating the associated observables records of a security incident. You can refer this to update any record in the **Related Records** tab.

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open a security incident.

3.  Select the **Related Records** tab.

4.  Select **Threat Intel** and then select **Associated Observables**.

5.  Select the fields to update.

6.  Update the value of the fields as required.


## Result

The updated field values are saved.

**Parent Topic:**[Working with Security Incident Records](../concept/using-analyst-workspace.md)

**Related topics**  


[Security Incident Overview section](../concept/security-incident-overview.md)

[Security Incident Details section](../concept/security-incident-details.md)

[SIR Workspace Orchestration](../concept/security-incident-response-workspace-orchestration-activities.md)

[Security Incident Response Tasks](../concept/security-incident-response-tasks.md)

[Security Incident Response Other Records](../concept/security-incident-response-other-records.md#)

[Security Incident Response Post Incident Review](../concept/security-incident-response-post-incident-review.md)

[TISC integration within SIR Workspace](../../secops-integration-threat-security-center/concept/tisc-sir-workspace.md)

[Reports in Security Incident Response](../concept/report-templates-sir.md)

[Collaborate using conference call or chat in Security Incident Response](../concept/collab-sir-call-chat.md)

[Viewing incident details with a relationship graph](../concept/sir-relationship-graph.md)

[MITRE attack and defend technique graph](../concept/mitre-attack-defend-graph-sir.md)

