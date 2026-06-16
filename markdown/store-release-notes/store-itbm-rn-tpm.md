---
title: Technology Portfolio Management release notes
description: Version history for the Technology Portfolio Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-tpm.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Technology Portfolio Management release notes

Version history for the Technology Portfolio Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.10.0 - June 2026**
    -   New: Added support for query\_range access control lists \(ACLs\).
    -   Fixed: TPM Discovered Technologies with empty discovery model are automatically cleaned up.
-   **Version 1.9.1 - March 2026**

    Fixed: Fixed a bug where duplicates or no records were being created for a large number of TPM discovered technology records.

-   **Version 1.9.0 - December 2025**
    -   New:
        -   Added a TPM lifecycle record identifier in the TPM Lifecycles tab of the Technology Portfolio page.
        -   Added a new field to provide owner details of TRM categories in the Create new TRM category form.
    -   Fixed: Fixed the issue of TPM discovered technologies records not getting removed from the TPM Discovered Technologies table, when the associated software installation record is removed.
-   **Version 1.7.3 - August 2025**

    Fixed: Bug which resulted in creation of duplicate entries in the TPM Lifecycle Exception table.

-   **Version 1.7.2 - May 2025**
    -   Fixed:
        -   The indicator direction for Technology Lifecycle Risk indicator is set to Minimize On a node restart, the Populate TPM discovered technologies and lifecycles schedule job is resumed
    -   The following issues are fixed:
        -   For the Populate Technology Lifecycle Risk scheduled job:
            -   Fixed the issue of the scheduled job getting stuck when a hardware model in TPM discovered technology was empty.
            -   Reduced the batch size to 50k For the Populate TRM Technical
        -   Debt for EA Workspace scheduled job:
            -   Fixed the issues of missing technical debts when there are different lifecycles for the same software products and business applications.
            -   Reduced the batch size to 50k
        -   For the Populate TPM Discovered Technologies and lifecycles scheduled job:
            -   Fixed the issue of performance lifecycles when multiple hardware models or software products have the same display value.
            -   Reduced the batch size to half.
-   **Version 1.7.1 - February 2025**
    -   Changed:
        -   Improved the performance of TPM, TRM scheduled jobs to handle large volumes of data
        -   Added Server field in the Technical Debt form
    -   Fixed: Added a new workspace view for all TPM tables to fix an issue with a preview of records
-   **Version 1.6.0 - November 2024**
    -   New:
        -   New system property to support tracking of installed software on any configuration item apart from computers, example docker containers, serverless hardwares
        -   Support wild card in version \(TRM\)
-   **Version 1.5.0 - August 2024**

    Fixed: The 'Update TPM data' action for a Business Application record is fixed to not delete valid software entries in the TPM discovered technology table.

-   **Version 1.4.0 - May 2024**

    New: Option to exclude unwanted software products.

-   **Version 1.3.1 - March 2024**

    Removed: SAM plugin dependency.

-   **Version 1.3.0 - November 2023**

    New: A scheduled job \(Populate TRM technical debts in the EA Workspace\) is created to update the Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table with the latest technical debt data in the EA Workspace.

-   **Version 1.2.0 - August 2023**

    New:

    -   Added a scheduled job to calculate technology risk scores for Business Applications, Application Services, Software Products, and Hardware Models on the basis of Software or Hardware Lifecycles.
    -   Added Technology Risk in Default Scoring Profile.
-   **Version 1.0.2 - May 2023**

    Manage technology lifecycle risks and technology lifecycle exceptions. Evaluate all your business applications and application services by accessing the discovered technologies and audit information.


**Parent Topic:**[ServiceNow Store - Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itbm-highlight.md)

