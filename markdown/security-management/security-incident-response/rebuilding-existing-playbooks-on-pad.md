---
title: Rebuilding existing playbooks in Workflow Studio
description: You can’t convert existing flows directly into playbooks in Workflow Studio. Each flow designer step that creates a response task to guide the analyst must be broken down into separate actions or subflows.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Rebuilding existing playbooks in Workflow Studio

You can’t convert existing flows directly into playbooks in Workflow Studio. Each flow designer step that creates a response task to guide the analyst must be broken down into separate actions or subflows.

You are not allowed to convert existing flows directly into playbooks in Workflow Studio. Each flow designer step that creates a response task to guide the analyst must be broken down into separate actions or subflows. By using these granular subflows or actions, you must create activity definitions. After you build these activity definitions, they get added as activities within stage in the process definition. You can reuse activity definitions across multiple playbooks.

You can customize each activity to render the required actions within them and how the card should look while building the activity definition. The activity can show email clients, tables, actions, KB articles, URLs, and so on. You can define how the activity definition and underlying action or subflows are created.

For more information, refer to the following sections.

-   [Activity definitions](https://www.servicenow.com/docs/access?context=activity-definitions&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
-   [Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

**Parent Topic:**[Using SIR Workspace](../../secops-analyst-workspace/reference/using-sir-workspace.md)

**Related topics**  


[Working with Security Incident Records](../../secops-analyst-workspace/concept/using-analyst-workspace.md)

[Security Incident Playbook](../../secops-analyst-workspace/concept/security-incident-playbook.md#)

[Prerequisites for the Playbooks](getting-started-with-processes.md)

[Activity Definitions](build-activities.md)

[Sample Playbooks for SIR Workspace](sir-workspace-playbooks.md)

[Working with MSI Records](../../secops-analyst-workspace/concept/working-with-msi-records.md)

[Working with Form UI actions](../../secops-analyst-workspace/concept/enable_workspace_form_ui_actions.md)

[Security Incident Closure workflow](../../secops-analyst-workspace/concept/security-incident-closure-workflow_0.md)

[Handle security incidents using Advanced Work Assignment](../../secops-analyst-workspace/task/handle-incidents-using-awa.md)

