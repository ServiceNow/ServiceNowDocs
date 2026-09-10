---
title: Task Plan Templates release notes
description: Version history for the Task Plan Templates application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-task-plan-templates.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Customer Service Management version history release notes, ServiceNow Store version history release notes]
---

# Task Plan Templates release notes

Version history for the Task Plan Templates application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.0.0 - September 2026**
    -   Admins and template authors can now configure advanced conditions on template items using referenced fields from parent or target tables. The Template Item Condition table supports both simple and advanced modes, enabling conditions based on related tables and mapping fields. Dynamic field visibility and mandatory validation are enforced, with error messages shown for missing required fields.
    -   Template authors can now define and propagate three new tracking fields for generated records. Template Item and Template Item Config forms expose item, execution, and business organization tracking fields, allowing authors to configure back-reference tracking for generated records. These fields are visible and editable in the UI, with dependent visibility and updated labels.
    -   Multi-case task dependencies and document associations are now supported at scale. Dependency relationships and document links are created for all generated records across multiple stores, with optimized insert paths to handle large volumes efficiently. Feature hooks for dependency and document association fire exactly once per execution after all workers finish.
    -   Clone feature now supports affected stores and dependencies. When cloning a template, all related features—including affected stores, scheduling details, and dependencies—are cloned, ensuring complete plans without manual setup. Cloned dependent tasks are maintained and visible in relevant tables.
    -   Document references are maintained during task generation and template cloning. Generated tasks refer to documents attached to template items, and cloned templates preserve document associations.
    -   Cascade confirmation popup added for template item configuration changes. When updating configuration fields, admins are prompted to cascade changes to existing template items, ensuring consistent tracking across linked items.
    -   Workspace and platform UI layouts updated for advanced condition fields. New fields are added to form and list layouts, with conditional visibility and proper spacing across all views.
    -   White papers available for multi-case changes and Task Plan Template features. Comprehensive documentation covers design, functionality, and usage for stakeholders.
-   **Version 4.0.0 - June 2026**
    -   Task Dependencies
        -   TheTemplate Dependencies tab on a task plan template record displays a node-map of dependencies between template items. SelectNew Dependency to create a dependency, and select an edge to edit or delete it. Each edge is labelled with one of the following dependency types:
            -   Finish to start
            -   Start after start
            -   Start together
    -   Sharing and Access Control of task plan templates
        -   The Share plan modal in the task plan template workspace provides three views: Share plan, Success, and Manage access. These views enable you to configure, confirm, and manage access to a task plan template.
        -   Apply template as an action in Task plan templates
        -   Apply Template action is available in Flow Designer. Use this action to automatically create tasks from a task plan template.
-   **Version 3.0.0 - March 2026**
    -   New in the  Australia  release:
        -   Task Dependency
            -   The dependency relationships between template items \(e.g. tasks, case, and case tasks\) are defined in sn\_task\_plan\_template\_dependency table and by applying the template, the dependencies between the generated tasks are created and stored in the sn\_task\_dependency\_m2m table. Task dependencies provide controlled sequencing within Task Plan Template items. By defining predecessor and successor relationships, the tasks can start at correct time reducing ambiguity for agents.
        -   Add and Manage Document References in Task Plan Templates
            -   The Task Plan Framework now supports attaching documents to task plan template items. Document references are stored in the sn\_task\_plan\_template\_document table and are available through form views and related lists, depending on template state and user permissions. Document handling is secure and aligned with template access controls, ensuring that only authorized users can view or modify attached files.
            -   By selecting “Apply Template” for any published task plan templates, the system automatically adds all document references from the original template items to the newly created tasks, ensuring seamless access for task owners to all required documents.
-   **Version 2.0.0 - December 2025**
    -   New:
        -   Admin Configuration setup:
            -   Configuration data model for admin to define the task plan configuration types
            -   Platform UI for the admin to create task plan configurations including hierarchy and the fields that need to be shown on the task plan template item page when a business persona is creating a task plan template item.
        -   Sharing and Access control of task plan templates: Users can now provide access to task plan templates at various levels, including user, group, and service organization. Access types include read, write, and delete.
        -   UI Page: A new record page has been created for Task Plan template items.
    -   Changed:
        -   Ownership Management: Admins and owners can change the owner of a task plan template.
        -   Global Templates: Task plan templates can be marked as global, making them visible to all users with read access.
        -   Read Only fields:Some fields were changed to Read Only for enhanced security.
    -   Fixed: Contains some UI-related and security-related defect fixes.
-   **Version 1.0.1 - August 2025**

    A task plan template allows the business user to define repeatable tasks and other items needed to complete a business process. The task plan template consists of template items which include the task definitions along which any child tasks or other related items that need to be created when the task plan template is applied.


**Parent Topic:**[ServiceNow Store - Customer Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

