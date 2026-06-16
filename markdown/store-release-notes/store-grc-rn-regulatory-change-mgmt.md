---
title: GRC: Regulatory Change Management release notes
description: Version history for the GRC: Regulatory Change Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-regulatory-change-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Regulatory Change Management release notes

Version history for the GRC: Regulatory Change Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New:
        -   Enabled Regulatory change management product support for IRM Standard customers.
        -   Implemented functional domain changes on regulatory alert record.
        -   Adopted feature roles feature on regulatory change management product.
        -   Manage Smart Assessment templates with versioning support. Create, publish, and delete template versions to support consistent assessment governance.
    -   Changed:
        -   Standardized query range security ACLs are now applied across all tables, ensuring consistent query access for authenticated users with appropriate read permissions throughout the platform. These ACL rules are installed automatically during upgrade with no administrator action required. Automated upgrade scripts handle the full transition, including detection and processing of previously customized ACLs to ensure existing configurations continue to function without interruption. If your instance includes administrator-modified query range ACLs, a post-upgrade review is recommended to confirm alignment with your intended access policies.
        -   Enabled audit entries support for RCM related records.
    -   Fixed: Fixed issues related to automated indexing of regulatory alert and other compliance objects index sources.
-   **Version 22.0.1 - March 2026**

    Fixed: Resolved security-related issues to improve protection and stability.

-   **Version 21.1.1 - December 2025 \(Zurich\)**
    -   New: Ability to configure recommendation template for policies. This will enable policy recommendations for given regulatory change alert.
    -   Changed:
        -   Introduced an 'Active' flag in the GRC Choice table; updates to these flags are now reflected in the AI Risk and Compliance Management application
        -   Implemented the impacts of Citation to Control mapping feature across the dashboards and overview pages.
    -   Fixed:
        -   Resolved a security vulnerability that allowed unintended edits to read-only fields.
        -   Replaced hard-coded Admin role dependencies with granular roles to improve security and align with least privilege principles.
-   **Version 21.0.1 - August 2025**
    -   New:
        -   Multiple regulatory tasks per alert: Regulatory alerts can now include multiple regulatory tasks, allowing teams to assign responsibilities and track progress across distinct impact areas for comprehensive compliance management.
        -   Source document import tasks: Multiple source document import tasks can be linked to a single alert to manage regulatory content ingestion, ensuring accurate capture and organization of relevant documents for compliance planning. These tasks follow a defined workflow from new to completed states.
        -   Regulatory task workflow updates: Regulatory tasks progress through new, work in progress, implementation, optional awaiting approval, and completed states. Tasks can be closed manually during Implementation if all action tasks are completed, providing flexibility in managing approvals.
        -   Action tasks management: Action tasks can be created when regulatory tasks are in new, work in progress, or implementation states, enabling detailed breakdown and monitoring of activities. Reopening action tasks is possible if regulatory tasks are rejected and moved back to implementation for rework.
-   **Version 20.2.2 - June 2025**

    Fixed: Enhanced security by creating Query range ACLs across multiple tables.

-   **Version 20.1.2 - May 2025**
    -   New: Added new impacted areas feature supporting multiple compliance and risk objects like controls, policies, control objectives, risks and so on.
    -   Changed:
        -   Enhanced the RCM action task form view to support new impacted areas feature.
        -   Impact radius calculation is updated to handle new impacted areas feature.
    -   Removed:
        -   Replaced legacy related documents feature with new Impacted areas.
        -   Automated action task creation as part of Impact radius now only creates tasks present in impacted areas table.
-   **Version 20.0.1 - February 2025**
    -   New: Introduced new Impact assessment feature based on smart assessment engine for a regulatory alert.
    -   Changed:
        -   Unified experience to trigger both impact and risk assessment.
        -   Improved overview and landing page experience with new reports on impact assessment.
    -   Removed:
        -   Entity class configuration is removed to provide flexibility in selection all the entities for risk assessment.
        -   All open assessments for a regulatory alert, whether they are risk assessments or regulatory assessments, are not marked as canceled and remain open even after an alert is marked applicable.
-   **Version 19.1.1 - November 2024**
    -   Changed: Incorporated new risk assessment feature changes to RCM product.
    -   Fixed:
        -   Improved workspace experience for users with low vision or those who rely on assistive technology, such as screen readers. This includes optimising zoom capabilities.
        -   Security fixes.
        -   Added new role changes to fix internal ML model access issue.
-   **Version 19.0.0 - August 2024**
    -   New:
        -   Define routing rules to automatically distribute regulatory alerts to internal stakeholders. Apply conditions to filter incoming regulatory feeds by Title, Description, Key dates, and many other fields. You can auto-assign filtered regulatory alerts to domain experts for further review.
        -   AI-powered recommendations from the most relevant citations through incoming regulatory changes, authority documents, child citations, and related control objects. You can drill down into the recommendation to explore its details within the context of the alert.
    -   Changed:
        -   Improved task management to facilitate the coordinator in changing the ownership of change tasks and action tasks.
        -   Next Experience Chat Collaboration and Discuss.
        -   Monitor action tasks segregated from or application for differentiation and reporting in the My Tasks portal.
-   **Version 18.1.2 - June 2024**
    -   Deprecated legacy "Regulatory Change Management" overview dashboard.
        -   Dashboard will continue for existing customers.
        -   It will not be available for new customers.
-   **Version 18.0.2 - February 2024**
    -   New:
        -   Manual Regulatory Alert Creation
            -   Core product capability to assist users in creating regulatory alerts manually
            -   Easily, create, organize and publish a regulatory alert to record changes from internal or external factors
        -   Bulk import regulatory alerts in large volume
            -   Import your regulatory alerts in bulk, Test and execute your import for data correction and accuracy
            -   Easy handling and correction of import errors
    -   Changed:
        -   UX Standardization
            -   Adopted 3-column layout user interface to maintain uniformity and consistency theme across ServiceNow
    -   Fixed:
        -   Bulk Selector options are not working when scoping multiple Entities for impact analysis
        -   Encoded string observed in regulatory alert content
        -   Content for regulatory alert are not loading when Thomson Reuters integration plugin is not installed
-   **Version 17.0.0 - August 2023**

    Changed: Implemented new Record page template changes to RCM record pages.

-   **Version 16.0.2 - July 2023**

    Fixed: Addressed an issue where the Runtime access tracking field's value was inadvertently changing from "None" to "Enforcing" during the Utah upgrade.

-   **Version 16.0.1 - February 2023**
    -   Changed: Ability to associate multiple Regulatory tasks to the same issue.
    -   Fixed:
        -   Access controls for viewing reports
        -   Localization issues
-   **Version 15.0.0 - December 2022**

    Fixed: Reduction in installation size of the application.

-   **Version 14.1.0 - March 2022**

    Fixed: Security issue

-   **Version 13.0.1 - September 2021**
    -   New: Regulatory alert contains a new provider reference.
    -   Changed:
        -   Regulatory feed nomenclature used earlier has been replaced with Regulatory alert
        -   Regulatory alert to taxonomy mapping is now added as a one to many table
        -   Related documents now have the ability to reference specific citation from library
    -   Removed:
        -   Taxonomy references on regulatory feed are deprecated and moved to the Regulatory feed to taxonomy mapping table
        -   Taxonomy related tables \(both internal and external taxonomy\) has been deprecated. The new taxnomy tables from the GRC: taxnomy management plugin is to be used
-   **Version 12.0.2 - March 2021**
    -   New:
        -   Support issue creation while implementing regulatory changes
        -   Automated action task creation to implement changes on the impacted Policies and Risk Statements in addition to Control Objectives
-   **Version 11.0.3 - November 2020**

    The ServiceNow Regulatory Change Management application provides a streamlined end-to-end process for managing regulatory changes. You can integrate content from various regulatory intelligence providers and constantly keep an eye on your regulatory horizon. Use robust workflows to assess the applicability and impact of regulatory events, map them with internal GRC objects, and execute the regulatory changes. Configurable reports and dashboards, with notifications and alerts increase the transparency of regulatory compliance across the organization.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

