---
title: Threat Hunting Playbook
description: The Threat Hunting playbook is a guided workflow for a TISC Case record that helps analysts move a threat hunt from an initial hypothesis to a final outcome.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-threat-hunt-playbook.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 3
keywords: [tisc, threat hunting, playbook, case management, workflow]
breadcrumb: [Using playbooks, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Threat Hunting Playbook

The Threat Hunting playbook is a guided workflow for a TISC Case record that helps analysts move a threat hunt from an initial hypothesis to a final outcome.

You can view and manage the playbook executions in the **Playbooks** tab of the Case record. The Threat Hunting playbook runs once per Case. After the playbook reaches completion, you can't run it on the same Case. You can add the playbook again for cancelled executions.

## Workflow stages

1.  **Intake** — Capture the hunt hypothesis and link related entities.
2.  **Triage** — The case owner reviews the hunt hypothesis from Intake and decides whether to proceed with the hunt or cancel it.
3.  **Scoping** — Select MITRE TTPs, define hunt scenarios, and create hunt tasks for analysts.
4.  **Hunt** — Analysts record findings; case-task status is tracked here.
5.  **Review Outcomes** — Review aggregated findings, recommendations, and closure summary.
6.  **Post Hunt** — Create a Security Incident or a report and complete the playbook.

## How the playbook is initiated

The playbook is initiated automatically when a Case is created with the following values:

-   **Case Type**: **Threat Hunting**
-   **Status**: **Draft**

A system work note on the Case record indicates that the playbook has been initiated. Open the **Playbooks** tab on the Case record to view execution details.

**Important:** The Threat Hunting Playbook is shipped in a deactivated state. Before the auto-initiation takes effect, an administrator must activate the playbook. For details, see [Activate the Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-activate-threat-hunt-playbook.md).

You can also attach the playbook manually to a Case that does not meet the auto-trigger conditions. For details, see [Add the Threat Hunting Playbook to a Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-add-playbook-manually.md).

## Roles and permissions

Any user with access to a Case record can read playbook details and contribute information at each stage. The case owner \(the user in the **Assigned to** field\) is the decision-maker for approvals and stage transitions.

|Action|Who can do it|
|------|-------------|
|Update the hunt hypothesis, scenarios, or findings|Any user with access to the Case record.|
|Approve or reject the hypothesis \(Triage\)|Case owner only.|
|Approve or reject hunt scenarios \(Scoping\)|Case owner only.|
|Transition between stages|Case owner only.|
|Create a Security Incident \(Post Hunt\)|Users with create access on the Security Incident table. If the user does not have this access, the **Create Security Incident** action is not displayed.|

## Playbook card in the context menu

While you work on other tabs of the Case record, you can monitor playbook status and cancel the playbook from the **Playbook** card in the right-side context menu.

-   **[Use the Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-use-threat-hunt-playbook.md)**  
Run threat hunt on a Case record — from capturing the hunt hypothesis through to creating a Security incident or reporting.
-   **[Add the Threat Hunting Playbook to a Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-add-playbook-manually.md)**  
If a Case does not meet the auto-trigger conditions for the Threat Hunting playbook, you can attach the playbook to the Case manually.

**Parent Topic:**[Using playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-playbooks-analyst.md)

**Related topics**  


[Use the Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-use-threat-hunt-playbook.md)

[Activate the Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-activate-threat-hunt-playbook.md)

