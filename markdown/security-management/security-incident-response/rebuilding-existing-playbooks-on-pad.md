---
title: Rebuilding existing playbooks in Workflow Studio
description: You can’t convert existing flows directly into playbooks in Workflow Studio. Each flow designer step that creates a response task to guide the analyst must be broken down into separate actions or subflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/rebuilding-existing-playbooks-on-pad.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Rebuilding existing playbooks in Workflow Studio

You can’t convert existing flows directly into playbooks in Workflow Studio. Each flow designer step that creates a response task to guide the analyst must be broken down into separate actions or subflows.

You are not allowed to convert existing flows directly into playbooks in Workflow Studio. Each flow designer step that creates a response task to guide the analyst must be broken down into separate actions or subflows. By using these granular subflows or actions, you must create activity definitions. After you build these activity definitions, they get added as activities within stage in the process definition. You can reuse activity definitions across multiple playbooks.

You can customize each activity to render the required actions within them and how the card should look while building the activity definition. The activity can show email clients, tables, actions, KB articles, URLs, and so on. You can define how the activity definition and underlying action or subflows are created.

For more information, refer to the following sections.

-   [Activity definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/activity-definitions.md)
-   [Process Automation Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer.md)

**Parent Topic:**[Using SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/using-sir-workspace.md)

**Related topics**  


[Working with Security Incident Records]()

[Security Incident Playbook]()

[Prerequisites for the Playbooks]()

[Activity Definitions]()

[Sample Playbooks for SIR Workspace]()

[Working with MSI Records]()

[Working with Form UI actions]()

[Security Incident Closure workflow]()

[Handle security incidents using Advanced Work Assignment]()

