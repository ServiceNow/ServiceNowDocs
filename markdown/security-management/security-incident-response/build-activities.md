---
title: Activity Definitions
description: The ServiceNow AI Platform provides a few activity definitions within the base system. In addition, for the playbooks that SIR Workspace base system, there are a few activity definitions defined in the base system under Enterprise Security Case Management PAD Commons application.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Activity Definitions

The ServiceNow AI Platform provides a few activity definitions within the base system. In addition, for the playbooks that SIR Workspace base system, there are a few activity definitions defined in the base system under Enterprise Security Case Management PAD Commons application.

Role required: sn\_si.admin.

Here’s the list of activity definitions that are a part of the base system:

|Activity Definition|Table|Description|Application|
|-------------------|-----|-----------|-----------|
|Wait For Condition with No Experience|Global\[global\]|Wait for Condition with no experience|Enterprise Security Case Management PAD Commons|
|Submit to CSF X Sandbox|Security Incident \[sn\_si\_incident\]|Submit to sandbox|Enterprise Security Case Management PAD Commons|
|Send Email|Security Incident \[sn\_si\_incident\]|Send email activity for SIR playbooks.|Enterprise Security Case Management PAD Commons|
|Search Email|Security Incident \[sn\_si\_incident\]|Search emails on email server|Enterprise Security Case Management PAD Commons|
|Update Task State|Security Incident \[sn\_si\_incident\]|Update the task state|Enterprise Security Case Management PAD Commons|
|Delete Email|Security Incident \[sn\_si\_incident\]|Delete emails|Enterprise Security Case Management PAD Commons|
|Yes No Outcome|Task \[task\]|Expected outcome|Enterprise Security Case Management PAD Commons|

-   **[Example Activity Definition: Send email](../task/example-activity-definition-send-email.md)**  
The following is an example of Send email activity definition.
-   **[Submit to CSF X Sandbox](../task/submit-to-csf-x-sandbox.md)**  
Submit to CSF X Sandbox is an example of an activity definition process.

**Parent Topic:**[Using SIR Workspace](../../secops-analyst-workspace/reference/using-sir-workspace.md)

**Related topics**  


[Working with Security Incident Records](../../secops-analyst-workspace/concept/using-analyst-workspace.md)

[Security Incident Playbook](../../secops-analyst-workspace/concept/security-incident-playbook.md#)

[Prerequisites for the Playbooks](getting-started-with-processes.md)

[Rebuilding existing playbooks in Workflow Studio](rebuilding-existing-playbooks-on-pad.md)

[Sample Playbooks for SIR Workspace](sir-workspace-playbooks.md)

[Working with MSI Records](../../secops-analyst-workspace/concept/working-with-msi-records.md)

[Working with Form UI actions](../../secops-analyst-workspace/concept/enable_workspace_form_ui_actions.md)

[Security Incident Closure workflow](../../secops-analyst-workspace/concept/security-incident-closure-workflow_0.md)

[Handle security incidents using AWA](../../secops-analyst-workspace/task/handle-incidents-using-awa.md)

