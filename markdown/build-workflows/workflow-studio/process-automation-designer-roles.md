---
title: Playbooks roles
description: Grant users access to build, view, and act on Playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/process-automation-designer-roles.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-09-02"
reading_time_minutes: 2
breadcrumb: [Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Playbooks roles

Grant users access to build, view, and act on Playbook.

## Roles

Roles are hierarchical. A role grants everything it contains, so assigning playbook.admin grants every role beneath it.

|Role|Description|Contains|
|----|-----------|--------|
|playbook.admin|Create, update, and delete trigger definitions. Launch the design environment to create, activate, edit, and delete playbooks. Create, edit, and delete activity definitions. Add translations for a playbook. View the shared Experience activity types and properties tables.|pd\_author, pd\_content\_author, pd\_operator, pd\_cancel, pd\_restarter, pd\_shared.admin|
|pd\_author|Launch the design environment to create, activate, edit, and delete playbooks. View all activity definitions. View the shared Experience activity types and properties tables.|playbook.write, playbook.activity\_def\_read, pd\_shared.user|
|pd\_content\_author|Create, edit, and delete activity definitions and trigger definitions. View the shared Experience activity types and properties tables.|pd\_trigger\_author, playbook.activity\_def\_read, pd\_shared.user|
|pd\_trigger\_author|Create, update, and delete trigger definitions.|None|
|pd\_operator|View process executions, activity executions, and execution logs only.|None|
|pd\_cancel|Cancel a running playbook without holding playbook.admin or write access to the parent record. Use to give a manager an ability that agents do not have.|None|
|pd\_restarter|Restart active playbooks.|None|
|pd\_shared.user|View the shared Experience activity types and properties tables.|None|
|pd\_shared.admin|Edit the shared Experience activity types and properties tables.|pd\_shared.user|
|playbook.write|Launch the design environment to create, activate, edit, and delete playbooks. Grants no read access on its own. Assign to users whose content is restricted by content access filtering.|playbook.designer\_access, pd\_shared.user|
|playbook.read|Read access to all playbooks.|None|
|playbook.designer\_access|Launch the design environment to view playbooks. Assign to users whose content is restricted by content access filtering.|pd\_shared.user, sn\_workflow\_studio.workflow\_studio\_read, sn\_diagram\_builder.db\_read|
|playbook.activity\_def\_read|View all activity definitions, unless the definition has required roles set.|None|
|delegated\_developer|Granted automatically when a user is assigned as a delegated developer. Grants access to all activity definitions through the default content filtering rule.|None|
|playbook.write.public\_access|Create and edit public access playbooks. Users without this role have read-only access to them. Required for delegated developers as well.|None|
|playbook.content\_author.public\_access|Edit the public access field on an activity definition.|None|
|playbook.automation\_runner|The restricted runner that automations execute as in a public access playbook. Automations don't run with broad system access.|None|

## Roles granted outside playbook administration

The playbook.designer\_access role contains two roles that playbook administrators don't manage. The sn\_workflow\_studio.workflow\_studio\_read role allows a user to launch the design environment. The sn\_diagram\_builder.db\_read role allows a user to view playbooks in diagram view.

All users need the snc\_internal role to access internal resources, including playbooks. A user without it can encounter trigger validation errors when a playbook attempts to run. This is a platform requirement rather than a playbook role.

**Note:** Granting playbook roles does not grant access to the Workflow Studio design environment. Users who create activity definitions might also need Workflow Studio access.

## Related role sets

Agentic playbooks and Otto for Playbooks carry their own roles, documented separately.

