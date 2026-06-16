---
title: Sourcing Pipeline Management release notes
description: Version history for the Sourcing Pipeline Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-psm-sourcing-pipeline-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Sourcing Pipeline Management release notes

Version history for the Sourcing Pipeline Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.0.1 - June 2026 \(Australia\)**

    Changed: Remediated non‑Glide Cobalt Raven ACLs in product code \(DIRS0000421\).

-   **Version 2.4.2 - June 2026**

    Fixed: Fixed an issue where workspace summary cards displayed closed pipeline projects and expired contracts. Dashboard cards now show only active projects and contracts requiring attention.

-   **Version 2.4.0 - March 2026**
    -   Fixes:
        -   Fixes certification failures in Sourcing Pipeline Management caused by system log errors and invalid queries referencing missing database fields.
        -   Fixes pipeline creation and contract‑addition issues in Category Manager Workspace, including UI inconsistencies, incorrect navigation, and date‑related validation errors.
-   **Version 2.0.1 - December 2025**
    -   New:
        -   A new Pipeline management tab has been added in the Source-to-Pay workspace. Access to this tab is controlled by the sn\_spend\_pipeline.sourcing\_pipeline\_user role. This workspace provides sourcing managers with:
            -   Personalized savings performance
            -   Action cards to quickly navigate to time-sensitive projects
            -   Visualizations of active work
            -   Direct access to all assigned pipeline projects
        -   Introduced the Automated Contract Renewal Workflow that enables sourcing managers to trigger sourcing work directly from expiring contracts. Key features include:
            -   Automatic surfacing of contracts expiring in 180 days through the Pipeline Management workspace, with a new UI action on the contract record to create a pipeline project
            -   Automatic creation of a pipeline project from the expiring contract via the UI action, with the contract linked in the Previous Records section of the pipeline project
            -   Auto-generation of a sourcing task for the business owner, appearing in the Employee Center To-dos list
            -   Confirming the need through the sourcing task auto-creates a new sourcing request, copying details from the previous request and linking it to the pipeline project
    -   Changed: Sourcing managers and category managers can now capture estimated savings, hard savings, and cost avoidance directly during multi-supplier award actions.
-   **Version 1.0.3 - August 2025**
    -   Sourcing Pipeline Management empowers sourcing managers and category managers with a centralized, automated, and insight-driven approach to managing sourcing savings initiatives. By introducing a dedicated pipeline project object, it eliminates manual swivel-chairing and fragmented tracking by unifying sourcing requests, sourcing events, and contracts into a single, structured workflow. Automated project creation via configurable rules ensures no intake request is overlooked - reducing missed savings opportunities.
    -   The plugin also resolves the challenge of untracked savings by capturing them automatically during award or allowing manual edits at closure, enabling accurate forecasting and reporting. Email alerts tied to project timelines and out-of-the-box field validations ensure timely execution and compliance. With full visibility into pipeline progress across workspace and list views, teams gain a long-term strategic view of sourcing activities - supporting better planning, prioritization and savings management.
    -   Unlike traditional tools, this solution offers flexible linking of sourcing objects, built-in automation, and a unified view - all designed to reduce operational overhead and deliver measurable impact. It's ideal for organizations seeking to scale sourcing operations, improve savings realization, and drive strategic sourcing outcomes.

**Parent Topic:**[ServiceNow Store - Sourcing and Procurement Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-psm-procurement-service-mgmt-landing.md)

