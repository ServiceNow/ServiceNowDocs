---
title: Playbook record generator
description: Use the playbook record generator to guide a user through the record creation process using a playbook experience.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Designing playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Playbook record generator

Use the playbook record generator to guide a user through the record creation process using a playbook experience.

Playbooks requires a record to be created or updated before a process can start. However, you can use the playbook record generator to allow users to create a new record using the playbook experience. You can then configure your workspace or UI Builder page to display the record generator playbook experience component in place of the standard new record form when a user opens a new record tab.

Playbook record generator inserts a record generator activity as the first step within a specified process definition created with Playbooks. This record generator activity contains a new record form. Once a user submits the form, the user is redirected to the newly created record, which now contains a running process. The running process guides the user through the rest of the record creation. If no process definition is running after the new record form is submitted, then the playbook will manually trigger whichever process definition was shown to user before record creation. The user stays within the playbook experience before and after the record is created for a seamless and guided record creation experience.

Admins can specify the name of the record generator activity, the form view, and the process definition shown to the user before the record is created. Admins can also optionally configure the declarative action used to submit the form.

**Parent Topic:**[Designing playbooks](playbook-experience-admins.md)

