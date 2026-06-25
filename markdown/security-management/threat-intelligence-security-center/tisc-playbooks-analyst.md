---
title: Using playbooks
description: Playbooks in Threat Intelligence Security Center guide analysts through structured threat investigation stages. Each stage defines the actions to complete before the case advances to the next phase of the response process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-playbooks-analyst.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-06-05"
reading_time_minutes: 4
keywords: [tisc, playbook, analyst, threat investigation, case, stages]
breadcrumb: [Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Using playbooks

Playbooks in Threat Intelligence Security Center guide analysts through structured threat investigation stages. Each stage defines the actions to complete before the case advances to the next phase of the response process.

When a Case record is created in Threat Intelligence Security Center with the appropriate Case type and status, a playbook starts automatically. The playbook appears in the **Playbooks** tab of the Case record and shows the current stage, pending activities, and overall progress. The Threat Hunting playbook runs once per Case. After the playbook reaches completion, you can't run it on the same Case. You can add the playbook again for cancelled executions.

## How stages work

A playbook moves through a fixed sequence of stages. Each stage contains activities — such as entering data, completing tasks, or waiting for an approval. You must complete all required activities in a stage before the case owner can advance the playbook to the next stage.

The **Playbooks** tab shows which stage is active and what activities remain. The playbook marks completed stages so you can track progress at a glance.

## Analyst contributions

Any analyst with access to a Case record can read playbook details and contribute information at each stage. Typical analyst activities include recording findings, linking related entities, selecting MITRE ATT&amp;CK techniques, and completing case tasks.

Stage transitions and approval decisions are made by the case owner — the user in the **Assigned to** field. If you aren't the case owner, complete your assigned activities and notify the case owner when the stage is ready to advance.

## Monitoring playbook status

While you work on other tabs of the Case record, you can monitor playbook status from the **Playbook** card in the right-side context menu. The card shows the current stage and lets you cancel the playbook if needed.

The system adds a work note to the Case record when the playbook starts. Check the work notes for a record of key playbook events, including stage transitions and completion.

## Playbook completion

A playbook runs once per Case. After it reaches completion, it can't run again on the same Case. If a playbook execution is cancelled, the case owner or an administrator can attach the playbook again manually.

At the final stage, analysts typically create a security incident or a report to document the outcome. This action requires create access on the Security Incident table. If you don't have this access, the playbook does not display the option.

-   **[Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-threat-hunt-playbook.md)**  
The Threat Hunting playbook is a guided workflow for a TISC Case record that helps analysts move a threat hunt from an initial hypothesis to a final outcome.

**Parent Topic:**[Threat Analyst Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/threat-analyst-workbench.md)

**Related topics**  


[Workbench Overview]()

[Creating cases using Threat Analyst Workbench]()

[Creating case task using Threat Analyst Workbench]()

[Working with Investigation Canvas]()

[Add artifacts to case\(s\) or case task\(s\)]()

[Run Enrichment Actions within a case]()

[View Case Reports]()

[Create a security incident from a TISC case]()

[Upload Secure File Attachments]()

[Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-threat-hunt-playbook.md)

[Use the Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-use-threat-hunt-playbook.md)

[Add the Threat Hunting Playbook to a Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-add-playbook-manually.md)

