---
title: SPM Enterprise-Wide Deployment release notes
description: The ServiceNow SPM Enterprise-Wide Deployment application provides data partitioning capabilities for Strategic Portfolio Management \(SPM\) tables that enable organizations to separate and control record visibility across functions such as departments and business units. Enterprise-Wide Deployment is a new application in the Australia release.The ServiceNow SPM Enterprise-Wide Deployment application provides data partitioning capabilities for Strategic Portfolio Management \(SPM\) tables that enable organizations to separate and control record visibility across functions such as departments and business units. Enterprise-Wide Deployment is a new application in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-05-15"
reading_time_minutes: 2
---

# SPM Enterprise-Wide Deployment release notes

The ServiceNow® SPM Enterprise-Wide Deployment application provides data partitioning capabilities for Strategic Portfolio Management \(SPM\) tables that enable organizations to separate and control record visibility across functions such as departments and business units. Enterprise-Wide Deployment is a new application in the Australia release.

## About SPM Enterprise-Wide Deployment

-   Separate and control record visibility across functions using partitions.
-   Enforce partition visibility automatically across Project Workspace, Portfolio Planning Workspace, Resource Management Workspace, and Strategic Planning Workspace.
-   Assign the EWD PMO role to users who require visibility across all partitions, such as PMO leads and portfolio managers.

See [SPM Enterprise-Wide Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/ewd-landing-page.md) for more information.

## Activation and other requirements

**Important:** Enterprise-Wide Deployment is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Enterprise-Wide Deployment by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-business-management-rn-landing.md)

## Australia

The ServiceNow® SPM Enterprise-Wide Deployment application provides data partitioning capabilities for Strategic Portfolio Management \(SPM\) tables that enable organizations to separate and control record visibility across functions such as departments and business units. Enterprise-Wide Deployment is a new application in the Australia release.

### What's new

-   **[Partitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/create-partition-ewd.md)**

    Separate and control record visibility across functions using partitions.

    -   Create partitions for functions such as IT Operations, HR, and Finance using the EWD admin \(sn\_spm\_ewd.ewd\_admin\) role.
    -   Configure partition criteria using reference fields such as Department on the project, demand, program, and portfolio tables.
-   **[Supported tables and workspaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/supported-tables-for-partition-ewd.md)**
    -   Partitioning is supported on the following primary tables and their related entities:

        -   Project \[pm\_project\]
        -   Demand \[dmn\_demand\]
        -   Program \[pm\_program\]
        -   Portfolio \[pm\_portfolio\]
        Related entities such as cost plans, resource plans, and planning items automatically inherit the partition value from the parent record.

    -   Partition enforcement applies automatically at runtime across the following workspaces:
        -   Strategic Planning Workspace
        -   Portfolio Planning Workspace
        -   Project Workspace
        -   Resource Management Workspace
-   **[Assign PMO role for visibility across all partitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/assign-pmo-roles-for-visibility-across-all-partitions.md)**

    Assign the EWD PMO \(sn\_spm\_ewd.ewd\_pmo\) role to users or user groups who require visibility across all partitions, regardless of their assigned partition role. This role is intended for PMO users such as organization leads who require enterprise-wide visibility across all departments.

-   **[Update existing records with partition details scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/update-partition-details-for-existing-records.md)**

    Populate partition details on records in the project, demand, program, portfolio, and planning item tables that were created before partition configuration was completed. Run this job only after completing partition configuration and assigning partition roles to users or user groups.


### Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    Enterprise-Wide Deployment \(sn\_spm\_ewd\): Provides data partitioning capabilities that enable organizations to separate and control record visibility across departments and business units.


