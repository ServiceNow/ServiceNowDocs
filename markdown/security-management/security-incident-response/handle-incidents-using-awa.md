---
title: Handle security incidents using AWA
description: Using AWA, security analysts can handle the security incidents assigned to them, which are available in the inbox folder of SIR Workspace.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-11-26"
reading_time_minutes: 2
breadcrumb: [Using SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Handle security incidents using AWA

Using AWA, security analysts can handle the security incidents assigned to them, which are available in the inbox folder of SIR Workspace.

## Before you begin

Role required: sn\_si\_analyst and awa\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Select the **Inbox** button.

3.  Select your presence state using the **Status** field.

    Available presence states are:

    -   **Available**: Analyst is available and can accept security incidents. Incidents are available for picking only to agents whose status is available.

        **Note:** If auto-assigned is configured, security incidents are directly assigned to you.

    -   **Away**: Analyst isn’t available. Incoming incidents and not assigned.
    -   **Offline**: The analyst is offline. Incoming incidents and not assigned. This is the default option.
    If your status is available, based on the configured service channel, queues and assignment rules, the incoming incidents are assigned to all the available security analysts including you. These incidents are either listed for you to accept or reject \(if configured\) or are auto-assigned to you.

4.  You can **Accept** or **Reject** a security incident.

    **Note:** Reject option is only available if rejection handling is enabled in AWA. If rejection handling isn’t enabled in AWA, incident is assigned to you on the basis of the configured service channel, queues, assignment rules, and your availability.

    When you accept a security incident, it’s assigned to you. When you reject a security incident, you have to select the reason for rejecting the security incident.


**Parent Topic:**[Using SIR Workspace](../reference/using-sir-workspace.md)

**Related topics**  


[Working with Security Incident Records](../concept/using-analyst-workspace.md)

[Security Incident Playbook](../concept/security-incident-playbook.md#)

[Prerequisites for the Playbooks](../../playbook-migration-guide/concept/getting-started-with-processes.md)

[Rebuilding existing playbooks in Workflow Studio](../../playbook-migration-guide/concept/rebuilding-existing-playbooks-on-pad.md)

[Activity Definitions](../../playbook-migration-guide/concept/build-activities.md)

[Sample Playbooks for SIR Workspace](../../playbook-migration-guide/concept/sir-workspace-playbooks.md)

[Working with MSI Records](../concept/working-with-msi-records.md)

[Working with Form UI actions](../concept/enable_workspace_form_ui_actions.md)

[Security Incident Closure workflow](../concept/security-incident-closure-workflow_0.md)

