---
title: Retail Core release notes
description: Version history for the Retail Core on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-retail-operations-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Retail release notes, ServiceNow Store release notes]
---

# Retail Core release notes

Version history for the Retail Core on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.3.0 - June 2026**
    -   Fixed:
        -   Implemented WCAG 2.2AA compliance including 400% zoom and reflow support across Retail Core screens.
        -   Completed OOTB Role Inheritance and ACL Review for Subscription Alignment.
-   **Version 6.5.0 - June 2026 \(Zurich\)**
    -   Fixed:
        -   Implemented WCAG 2.2AA compliance including 400% zoom and reflow support across Retail Core screens.
        -   Completed out-of-the-box role inheritance and ACL review for subscription alignment.
-   **Version 6.4.0 - May 2026 \(Zurich\)**
    -   New:
        -   Added capability to track the status of HQ tasks within each HQ case
        -   Added capability to fulfil HQ tasks on the workspace
-   **Version 7.2.0 - May 2026**
    -   New:
        -   Added capability to track the status of HQ tasks within each HQ case
        -   Added capability to fulfill HQ tasks on the workspace
-   **Version 7.0.0 - March 2026 \(Australia\)**
    -   New:
        -   Introduced a new admin role,retail\_admin, which provides CRUD access to the Retail Organization.
        -   Added support to build store plans using task plan templates and planned work management.
-   **Version 6.2.0 - March 2026 \(Zurich\)**

    New: Added support to build store plans using task plan templates and planned work management.

-   **Version 5.4.0 - December 2025**
    -   Now Assist for Retail Service Management \(RSM\) highlights for the Zurich release
        -   The Store Inquiry AI agent enables retail HQ teams by:
            -   Intelligently searching knowledge base articles, past cases, and attached documents to provide clear, policy-compliant responses.
            -   Sharing resolution steps and prompting agents to accept, edit, or reject AI-suggested solutions, reducing manual effort and improving decision-making speed.
            -   Learning continuously from resolved queries to deliver more accurate and relevant suggestions over time.
-   **Version 5.2.0 - August 2025**

    Changed: Retail case made abstract: The Retail Case \(sn\_retail\_case\) is an abstract table. It would serve as a parent table that provides a common structure and functionality to multiple child tables. It will not be meant to store records directly but act as a template for inheritance. Multiple use case-oriented extensions will be drawn from this table which could then be used to store retail case records. Please refrain from creating any records, workflows in this table and use table extensions for your use cases.

-   **Version 5.1.0 - August 2025 \(Yokohama\)**

    Changed: Retail case made abstract: The Retail Case \(sn\_retail\_case\) is an abstract table. It would serve as a parent table that provides a common structure and functionality to multiple child tables. It will not be meant to store records directly but act as a template for inheritance. Multiple use case-oriented extensions will be drawn from this table which could then be used to store retail case records. Please refrain from creating any records, workflows in this table and use table extensions for your use cases.

-   **Version 4.0.0 - February 2025**
    -   New:
        -   Added retail service portal to the retail core with menus such as catalog, Knowledge, cases and tasks, and more information.
        -   Knowledge base articles, quicks links and the most popular articles are added as the demo data.
        -   Retail standard ticket widget is added to work on the case actions.
        -   KPI widgets are added to show the scores, based on the persona the reports varies.
        -   Store info contains store 360 data view to look at the store level details like cases, tasks, members, child retail organizations.
    -   Changed:
        -   The role sn\_retail.report\_viewer has been added to the following roles \(sn\_retail.sn\_retail.associate\_contributor, sn\_retail.associate\_fulfiller, sn\_retail.manager\_contributor and sn\_retail.manager\_fulfiller \).
-   **Version 3.0.0 - November 2024**
    -   New:
        -   Added two new roles: Store Associate - Fulfiller and Store Manager - Fulfiller.
        -   Added Tasks related list to retail cases.
        -   Added ability to escalate or de-escalate retail cases.
    -   Changed: The Retail Organization table now has a bi-directional reference to Service Organization. The "Restrict SO update" business rule has been added to accomplish this.
-   **Version 2.0.0 - August 2024**

    The ServiceNow Retail Operations application empowers frontline managers and associates to seamlessly manage day-to-day store operations by automating tasks, resolving issues quickly with self-service, and freeing up time to better serve customers. It enables seamless two-way communication and visibility between stores and HQ, thus delivering a great customer experience while enhancing staff productivity and reducing costs.


