---
title: RMA Case Management release notes
description: Version history for the RMA Case Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-rma-case-mgmt.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# RMA Case Management release notes

Version history for the RMA Case Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.1 - July 2026**
    -   New: Agents can now initiate RMA cases directly from Sold Product records. The RMA Case form supports Sold Product as a source, enabling agents to select and process returns, exchanges, repairs, or upgrades tied to original sales transactions.
    -   Changed: RMA playbook stages now display list views dynamically based on the Requested Source field.The Add case lines, Propose issue solutions, and resolve case stages fetch and display views according to the selected source, improving workflow flexibility and accuracy.
-   **Version 2.1.0 - March 2026**
    -   Changed:
        -   Added ACLs on RMA case and RMA case lines for customer persona.
        -   Minor code enhancements.
-   **Version 2.0.0 - November 2025**
    -   New:
        -   Agent Experience​
            -   Create new navigation menu for the RMA Cases.
            -   A Horizontal playbook experience is created in the CSM/FSM Agent Experience workspace with multiple stages while resolving the case.
        -   Roles and permissions
            -   RMA Agent is a new role introduced to peform read, write, update and delete on RMA Case and RMA case lines table.
            -   New granular roles to create, read, write and delete on RMA case and RMA case line.
        -   Data Model changes
            -   Added new choices for the columns: Proposed resolution and Customer expected resolution code.
-   **Version 1.0.0 - August 2025**

    The RMA Case application enables organizations to manage and triage return cases for customer products and services, addressing returns, replacements, and repair use cases. The core of this solution is the RMA Case Management application, which features a specialized RMA case type. This case type allows users to associate multiple install base items as individual case line items within a single RMA case record. This structure enables efficient tracking of various issues across different items while maintaining a consolidated view of the entire return process.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

