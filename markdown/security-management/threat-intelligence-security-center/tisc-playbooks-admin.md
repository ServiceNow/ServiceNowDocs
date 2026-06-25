---
title: Playbooks
description: Playbooks in Threat Intelligence Security Center are structured, automated workflows that guide threat response from detection to resolution. Administrators configure, activate, and manage playbooks to standardize how analysts handle threat cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-playbooks-admin.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-06-05"
reading_time_minutes: 2
keywords: [tisc, playbook, administrator, workflow, threat response, configure]
breadcrumb: [Administer, Threat Intelligence Security Center, Security Operations]
---

# Playbooks

Playbooks in Threat Intelligence Security Center are structured, automated workflows that guide threat response from detection to resolution. Administrators configure, activate, and manage playbooks to standardize how analysts handle threat cases.

A playbook is a predefined sequence of stages and activities that runs against a Case record in Threat Intelligence Security Center. Each stage defines the actions analysts must complete before the case advances. Playbooks reduce manual coordination by enforcing a consistent response process across your security team.

## Playbook structure

A playbook consists of stages arranged in a fixed sequence. Each stage contains one or more activities. Activities can include data collection tasks, approval gates, or automated actions. The playbook advances to the next stage only after all required activities in the current stage are complete.

Playbooks are defined in Workflow Studio. Each playbook is associated with a specific Case type. When a Case record meets the trigger conditions, the playbook initiates automatically.

## Trigger conditions

A playbook initiates automatically when a Case record is created with the Case type and status values that match the playbook trigger configuration. You define these conditions in Workflow Studio when you configure the playbook.

A system work note on the Case record confirms that the playbook has started. If the trigger conditions aren't met, analysts can attach the playbook to a Case manually.

**Note:** Playbooks ship in a deactivated state. Activate each playbook in Workflow Studio to auto-trigger its execution.

## Playbook lifecycle

Each playbook runs once per Case. After a playbook reaches completion, it can't run again on the same Case. For cancelled executions, you can attach the playbook again manually.

Administrators can monitor all active playbook executions from the **Playbooks** tab on each Case record. The tab displays the current stage, pending activities, and execution history.

## Roles and access

Playbook configuration and activation require the admin role. Analysts with access to a Case record can read playbook details and contribute information at each stage. Stage transitions and approval decisions are restricted to the case owner — the user in the **Assigned to** field on the Case record.

Some stage activities, such as creating a security incident, require additional roles. If a user does not have the required access, the playbook does not display the corresponding action.

## Managing playbooks

Use Workflow Studio to create, edit, activate, and deactivate playbooks. Changes to a playbook definition don't affect executions that are already in progress. Only new Case records that meet the trigger conditions use the updated playbook.

To test a playbook before activating it, use the **Test** option in Workflow Studio and provide a Case record as input. This lets you verify stage transitions and activity behavior without affecting live cases.

**Related topics**  


[Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-threat-hunt-playbook.md)

[Activate the Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-activate-threat-hunt-playbook.md)

[Add the Threat Hunting Playbook to a Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-add-playbook-manually.md)

