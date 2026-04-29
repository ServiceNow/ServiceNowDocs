---
title: Document References in Task Plan Templates
description: Document references in task plan templates allow documents to be associated with tasks or cases and made available to task owners. This capability supports adding, viewing, and managing documents within template items, ensuring task owners have access to the required files when working on assigned tasks or cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Document References in Task Plan Templates

Document references in task plan templates allow documents to be associated with tasks or cases and made available to task owners. This capability supports adding, viewing, and managing documents within template items, ensuring task owners have access to the required files when working on assigned tasks or cases.

The following roles can add, view, and manage documents—such as PDFs, Word documents, images, and PowerPoint files to task plan template items. Document management capabilities follow existing access controls, ensuring that only authorized users can modify document content.

-   `sn_task_plan.admin`
-   `sn_task_plan.creator` \(draft templates only\)
-   `sn_task_plan.writer`
-   `sn_task_plan.viewer` \(viewers can only view documents and cannot create, edit, or delete document references\).

Document references are stored in the  **Task Plan Template Document**`(sn_task_plan_template_document)`  table and are available through form views and related lists, depending on the template state and user permissions. ACLs ensure proper read and write control across forms and lists.

When a published task plan template is applied, the system automatically adds all the document references from the template items to the newly created tasks. These references are associated with the corresponding tasks, ensuring that access permissions and business logic operate as expected, and preventing regeneration of documents during template application. This capability allows task owners to easily access all the documents required to complete their assigned tasks.

Key Features:

-   The Task Plan Template feature \(`sn_task_plan_feature`\) stores feature definitions, such as **Document Support** and **Task Dependency**.
-   The Task Plan Template Item feature \(`sn_task_plan_template_feature`\) links specific features to template items.
-   Document Reference Storage: The system uses the `sn_task_plan_template_document` table to store document references. Visibility and edit rights depend on ACLs and template state \(draft or published\).

Key Benefits:

-   The user interface provides a consistent experience for managing task plan features and their associated documents.
-   Document handling is secure and aligned with template access controls, ensuring that only authorized users can view or modify attached files.
-   The framework supports extensibility for cross‑product teams, enabling broader adoption and integration across different organization units.

