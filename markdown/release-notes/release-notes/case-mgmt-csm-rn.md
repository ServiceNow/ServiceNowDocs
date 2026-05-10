---
title: Case management for CSM release notes
description: The ServiceNow Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Case management for CSM release notes

The ServiceNow® Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Australia release.

## Case management for CSM highlights for the Australia release

-   Major cases now have the same case type as the original case, and associated child cases also have the same case type.
-   Enhancements to task plan templates to support task dependency, and to support document attachments in task plan template items.
-   Migrating several applications from family to store.

See [Case management for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-case-management.md) for more information.

## New in the Australia release

-   **[Task Dependencies for Task Plan Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/task-dependencies-for-task-plan-templates.md)**

    Define dependency relationships between template items in the \[sn\_task\_plan\_template\_dependency\] table, and upon applying the template, create and store the resulting task dependencies in the \[sn\_task\_dependency\_m2m\] table to ensure controlled task sequencing through predecessor–successor relationships.

-   **[Document References in Task Plan Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/adding-and-managing-document-references-in-task-plan-templates.md)**

    Add documents to Task Plan Template items, storing document references in the \[sn\_task\_plan\_template\_document\] table and making them accessible through form views and related lists based on template state and user permissions, ensuring secure and controlled document access aligned with template‑level permissions


## Changed in this release

-   **[Major Issue Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/major-issue-management.md)**

    Case Type consistency improvements: This update ensures case type consistency when creating and managing major cases and their related child cases, improving accuracy and reducing manual correction.

    -   Create major cases automatically upon approval, and major cases now inherit the same case type as the originating case.
    -   Promote the proposed case directly to a major case I-if no account or consumer or partner exists on the originating major case.
    -   Use the major case's case type and inherit the fields defined in \(sn\_customerservice.case\_fields\_to\_sync\) property or defined through extension point for child cases.
-   **[Task plan templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/task-plan-templates.md)**

    Add flexible task dependency management to task plan templates, and support for attachments.

    -   Schedule offsets can be defined when creating dependencies, allowing tasks to start within a specified time period \(minutes, hours, days, or weeks\).
    -   Configure and manage task dependencies directly from task dependency list and view layouts.
    -   Built‑in validations prevent circular dependencies, ensuring task plans remain accurate and reliable.
    -   Ability to attach documents to tasks or cases.
    -   Select **Apply Template** for any published task plan templates to automatically add all document references from the original template items to the newly created tasks, ensuring seamless access for task owners to all required documents.
-   **[Case type selector for creating cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-case-of-specific-case-type.md)**

    The case type selector is now activated by default when creating cases of these types:

    -   Interaction
    -   Account
    -   Contact
    -   Consumer
    -   Sold product
    -   Install base item
    -   Related lists: child case, case task
    -   List view
    -   Case task list view

## Plugin information

-   **New Plugins**

    The following plugin is new in Australia:

    [Assignment Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/case-assignment-workbench.md) \(sn\_assign\_wb\_host\): This plugin enables managers to assign tasks to agents efficiently and intelligently.

-   **Plugins planned for deprecation**

    These plugins are planned for deprecation in the C release. Beginning with the Australia release these plugins will be migrated to store applications. Upgrade your instance to Australia or later release versions and the store applications will be automatically installed:

    -   [Action Status Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-case-action-status.md) \(com.sn\_action\_status\)
    -   [Customer Service Case Action Status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-case-action-status.md) \(com.snc.csm\_action\_status\)
    -   [Case Digests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-case-digests.md) \(com.sn\_csm\_case\_digest\)
    -   [Customer Service Document Template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-case-digests.md) \(com.sn\_csm\_doc\_template\)
    -   [Customer Project Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-ppm-integration.md) \(com.snc.csm\_ppm\)
    -   Customer Service with Request Management \(com.sn\_cs\_sm\_request\)
    -   Customer Service with Service Management \(com.sn\_cs\_sm\)
    -   [Major Issue Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/major-issue-management.md) \(com.sn\_majorissue\_mgt\)
    -   [Proxy contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/employee-create-case-for-customer.md) \(com.snc.csm\_proxy\_contacts\)
    -   [Targeted communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_TargetedCommunications.md) \(com.sn\_publications\)
    -   [Case Assignment Workbench Demo](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/r_CustServMgmtAddtlPluginsTable.md) \(com.snc.case\_assignment\_workbench\_demo\): Beginning with the Australia release this plugin will be deprecated. The demo data will be migrated to the Case Assignment Workbench store application.

**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

