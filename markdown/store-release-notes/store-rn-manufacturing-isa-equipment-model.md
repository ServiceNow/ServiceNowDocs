---
title: ISA Equipment Model release notes
description: Version history for the ISA Equipment Model application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-manufacturing-isa-equipment-model.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Operational Technology release notes, ServiceNow Store release notes]
---

# ISA Equipment Model release notes

Version history for the ISA Equipment Model application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.0 - June 2026**

    New: Certified for Australia Patch 3

-   **Version 3.1.0 - March 2026**

    New: Certified for Australia

-   **Version 3.0.0 - December 2025**

    Changed: Minor Platform enhancement.

-   **Version 2.0.8 - September 2025**
    -   -   Assign Processing Order value to child entities to sort equipment model entities in a Site.
-   In the Equipment Model menu, the Daily Activity tab displays the list of previous day's activities on the OT devices.
-   View all vulnerable items that have been created from the OT Vulnerable Items List View in the Industrial Workspace.
-   View all remediation tasks that have been created from the OT Remediation Tasks List View in the Industrial Workspace.
-   View all vulnerability exceptions that have been created from the OT Vulnerability Exception Approvals List View in the Industrial Workspace.
-   **Version 2.0.5 - August 2025**
    -   New:
        -   Assign Processing Order value to child entities to sort equipment model entities in a Site.
        -   In the Equipment Model menu, the Daily Activity tab displays the list of previous day's activities on the OT devices.
        -   View all vulnerable items that have been created from the OT Vulnerable Items List View in the Industrial Workspace.
        -   View all remediation tasks that have been created from the OT Remediation Tasks List View in the Industrial Workspace.
        -   View all vulnerability exceptions that have been created from the OT Vulnerability Exception Approvals List View in the Industrial Workspace.
-   **Version 2.0.4 - February 2025**

    No changes.

-   **Version 2.0.3 - November 2024**

    Fixed: Updated with various bug fixes.

-   **Version 2.0.1 - September 2024**

    New: Certified for Xanadu.

-   **Version 2.0.0 - August 2024**

    Certified for Xanadu.

-   **Version 1.0.12 - February 2024**
    -   Certified for Washington DC
    -   Improved site level access control to use User Criteria to define read or write level user access to equipment model entity sites. With the additional assignment of OT viewer \(cmdb\_ot\_viewer\) or OT Editor \(cmdb\_ot\_editor\) roles, users will also have either view or edit access to OT devices in the sites assigned accordingly.
    -   On upgrade to version 1.0.12 of ISA Equipment Model, existing Site User records will be migrated to an improved access control model using User Criteria to preserve the same access permissions. For each site with ISA Entity Site User records:
        -   For users with viewer access:
            -   A new User Criteria record will be created and named Read User Criteria for &lt;site name&gt; Site \[System Generated\]
            -   A new User Group with all Site Users from this site will be created and named Read Group for &lt;site name&gt; Site \[System Generated\]
            -   A new record in the new Equipment Model Entity View Access table \(isa\_entity\_m2m\_user\_criteria\_can\_view\) will be created with the User Criteria and User Group just created as described above.
        -   For users with editor access:
            -   A new User Criteria record will be created and named Edit User Criteria for &lt;site name&gt; Site \[System Generated\]
            -   A new User Group with all Site Users from this site will be created and named Edit Group for &lt;site name&gt; Site \[System Generated\]
            -   A new record in the new Equipment Model Entity Edit Access table \(isa\_entity\_m2m\_user\_criteria\_can\_edit\) will be created with the User Criteria and User Group just created as described above.
    -   Removed the Site User application menu and Site Users related list on the Equipment Model Entity record for a site
    -   Set all Site User \(isa\_entity\_site\_user\) records to inactive
    -   Added application menu items for both
        -   Site User - Can Read
        -   Site User - Can Edit
    -   Added related lists on the Equipment Model Entity record for a site for both
        -   Can Read Equipment Models
        -   Can Edit Equipment Models
-   **Version 1.0.11 - August 2023**
    -   Certified for Vancouver
    -   Removed Read-only protection policy for the ISAEquipmentModelConstants script include
    -   For ISA Equipment Model Import, please see the Industrial Process Manager application
-   **Version 1.0.10 - February 2023**

    New: Certified for Utah

-   **Version 1.0.8 - August 2022**
    -   Removed: Dependency on Manufacturing Process Manager
    -   New: Certified for Tokyo
-   **Version 1.0.6 - February 2022**

    Changed: Updated application menu name from "Equipment Models" to "Equipment Model Entities"


**Parent Topic:**[ServiceNow Store - Operational Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-manufacturing-highlights.md)

