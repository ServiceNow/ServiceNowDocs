---
title: Task Dependencies for Task Plan Templates
description: Task dependencies define the execution order between tasks, case, and case tasks in a Task Plan Template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/task-dependencies-for-task-plan-templates.html
release: brazil
topic_type: concept
last_updated: "2026-09-04"
reading_time_minutes: 2
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Task Dependencies for Task Plan Templates

Task dependencies define the execution order between tasks, case, and case tasks in a Task Plan Template.

Overview

Task dependencies provide controlled sequencing within the generated records from the template items in the **Task Plan Template Dependency** table. By defining predecessor and successor relationships, the tasks can start at the correct time reducing ambiguity for agents. Administrators and users with edit permissions can add or update dependencies when the template is in the **Draft** state. Users with read‑only access can view dependency information after the template is shared.

All dependency records are stored in the **Task Plan Template Dependency** table. Each record includes the predecessor, successor, dependency type, minimum and maximum lag times, use max lag time, and assignment criteria.

The user interface provides list views, form views, and a related list on the template record to support dependency management. UI policies dynamically show or hide fields based on user selections. For example, selecting **Use maximum lag time** displays the **Maximum lag time** field, allowing users to specify the maximum lag duration.

The **Assignment criteria** field contains the drop‑down list with options such as **Same agent** and **Same day, same agent**. Built‑in validations prevent circular, self‑referencing, or duplicate dependencies. Role‑based access controls determine who can view, create, update, or delete dependency records, depending on the user’s role and the template state.

option.

**Apply Template** is available only after a task plan template is published. When selected, it generates task records in the corresponding tables and populates the defined dependencies between template items in the **Task Dependency**table. Task plan template users and administrators can add, edit, or remove dependencies using the provided UI controls only when the template is in **Draft** state. When a dependency is removed, the system displays a custom confirmation message indicating that only the dependent tasks are affected.

You define a dependency once, between two template items. When records are generated from a published task plan template, the dependency creates a pair between the corresponding predecessor and successor records. When records are generated for multiple business organizations, a separate pair is created for each business organization: a predecessor is paired only with a successor that was generated for the same business organization, never with a record generated for another business organization.

The predecessor and the successor do not need to be created in the same target table. Pairing works across target tables, such as a case task that depends on a case.

Task dependencies help ensure clear and predictable task sequencing and support multiple dependency types through minimum and maximum lag times.

  **Apply Template** e items

