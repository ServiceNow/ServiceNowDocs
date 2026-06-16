---
title: Software Asset Management release notes
description: Version history for the ITAM Software Asset Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itam-software-asset-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - IT Asset Management release notes, ServiceNow Store release notes]
---

# Software Asset Management release notes

Version history for the ITAM Software Asset Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.1.3 - June 2026 \(Australia\)**

    Critical fixes for regex normalization

-   **Version 3.2.7 - June 2026 \(Zurich\)**

    Minor defect fixes related to suite inference and reclamation candidates.

-   **Version 3.2.6 - May 2026 \(Zurich\)**

    In this version, a defect causing software reconciliation failures with common per-core or per-processor consumption rules has been fixed.

-   **Version 4.1.1 - April 2026 \(Australia\)**

    Minor defects related to reconciliation and software normalization were fixed in this release.

-   **Version 3.2.5 - April 2026 \(Zurich\)**

    Minor defects related to software reconciliation were fixed in this release.

-   **Version 2.1.18 - April 2026 \(Yokohama\)**

    Minor defects related to reconciliation and the software product lifecycle were fixed in this release.

-   **Version 4.1.0 - March 2026 \(Australia\)**

    In this version, changes to the explanation of rights have been added for CrowdStrike license consumption through SaaS-based integration.

-   **Version 4.0.0 - March 2026 \(Australia\)**
    -   New:
        -   Microsoft SQL Server Enterprise \(Server+CAL licensing\): Use the updated licensing rule to optimize legacy SQL Server Enterprise Edition licenses with Software Assurance \(SA\). Under this rule, one server license can cover up to four virtual machines as long as their combined usage does not exceed 20 cores or hardware threads at any time.
        -   Microsoft Server Infrastructure and License consumption report: View a single, unified report that shows Microsoft server installations and license usage across all license types. The report combines device infrastructure data with license usage and exemptions and clearly explains reasons for exemptions, such as unlicensed or ignored installs—making it easier to track, analyze, and optimize your IT resources.
    -   Changed: Improved handling of unlicensed entities in License Usage: The license usage now shows clearer reason codes and guidance for unlicensed entities. This helps SAM managers and users understand exactly why something is unlicensed and what actions to take to fix it.
-   **Version 3.2.4 - March 2026 \(Zurich\)**

    Minor defects related to reconciliation and the software product lifecycle were fixed in this release.

-   **Version 3.2.3 - February 2026 \(Zurich\)**

    Minor defects related to Reconciliation and Software Product lifecycle were fixed in this release

-   **Version 2.1.17 - February 2026 \(Yokohama\)**

    Minor defects related to Reconciliation and Software Product Lifecycle were fixed in this release

-   **Version 3.2.1 - January 2026 \(Zurich\)**

    Minor defects related to Reconciliation and Software Product Lifecycle were fixed in this release

-   **Version 2.1.13 - January 2026 \(Yokohama\)**

    Minor defects related to Reconciliation were fixed in this release.

-   **Version 3.2.0 - December 2025 \(Zurich\)**

    This release introduces support for BYOL using the Microsoft Per Processor license metric on Azure for Windows Server, as well as several minor fixes related to reconciliation.

-   **Version 2.1.12 - December 2025 \(Yokohama\)**

    Minor defects related to Reconciliation and Software Product lifecycle have been fixed in this release.

-   **Version 2.1.11 - November 2025 \(Yokohama\)**

    Minor defects related to reconciliation performance have been resolved in this release.

-   **Version 3.0.2 - October 2025**

    Minor bug fixes related to Reconciliation.

-   **Version 2.1.10 - October 2025**

    Minor defects related to Reconciliation were fixed in this release.

-   **Version 3.0.1 - September 2025 \(Zurich\)**

    Minor bug fixes related to Reconciliation and Software Product Lifecycle

-   **Version 2.1.9 - September 2025 \(Yokohama\)**

    Minor bug fixes related to Suites and Reconciliation

-   **Version 2.1.7 - September 2025 \(Yokohama\)**

    Fixed minor bug fixes related to Reconciliation and Software Product Lifecycle

-   **Version 3.0.0 - August 2025 \(Zurich\)**
    -   This application enables the following features when installed with:
        -   Software Asset Management Foundations: None
        -   Software Asset Management Professional:
            -   Apply preferred licensing assignment to Microsoft software products that are deployed on clusters: Define and apply preferred cluster licensing assignments to the Microsoft software products that are deployed on your hypervisor clusters. By using a preferred cluster licensing assignment, you can choose whether you want to license these software products at either the physical host layer or the virtual layer, helping you better align with your organization's predetermined licensing strategy. Built-in validations help verify that your licensing strategy setup complies with the relevant Microsoft licensing requirements.
            -   Manage licensing for Microsoft server products on Microsoft hyper-v virtualization technology: Use the Software Asset Management publisher pack for Microsoft to track and manage licensing for Microsoft Server products, such as Microsoft Windows Server and Microsoft SQL Server, on Microsoft Hyper-V virtualization technology. Track license usage and determine your license compliance position so that you can better optimize your licensing costs.
            -   Automatically identify and license MS SQL Server high availability configurations: Use the Software Asset Management publisher pack for Microsoft to automatically identify and license Microsoft SQL Server deployments in high availability configurations, such as Always On availability groups. This capability enables the Software Asset Management application to automatically classify each replica within a configuration as either active or passive, resulting in more accurate license compliance for Microsoft SQL Server.
            -   Efficiently manage user allocations in bulk using group allocations: Allocate licenses to user groups instead of individual users for a software entitlement using the group allocation feature for the user-based licensing metric software. Group allocation feature enables Software Asset Management managers to streamline and manage the license allocation process efficiently. User allocation is created for the group members based on the availability of unallocated licenses. Any changes made to the composition of the user group automatically updates the license allocation.
            -   Manage licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\): Following the updates to VMware's licensing policy, use the Software Asset Management publisher pack for VMware to track and manage licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\), which are updated suite-based product offerings for VMware vSphere. With these updated product offerings, you can measure compliance and optimize licensing for multiple VMware vSphere products under a single subscription.In addition, the publisher pack can account for the number of cores and the licensing minimums when calculating licensing requirements for VVS and VVEP.
            -   Use flexible reporting capabilities to gain deeper insights into your Effective License Position \(ELP\): Improve analysis of your ELP with flexible reporting on reconciliation results. Reports can be run on existing reconciliation groups or customer-defined groups, and the report data can be organized by unique combinations of group, subgroup, publisher, product, version, and edition. For each combination, the average cost is calculated and provides the total number of required licenses. The results are presented in a structured format for easy analysis and reporting.
-   **Version 2.1.6 - August 2025 \(Yokohama\)**

    In this version, a few minor bugs related to reconciliation have been fixed.

-   **Version 2.1.5 - July 2025 \(Yokohama\)**

    In this version, a few minor bugs related to reconciliation have been fixed.

-   **Version 1.0.13 - July 2025 \(Xanadu\)**

    In this version, the reconciliation issue related to RedHat suites has been resolved.

-   **Version 2.1.4 - June 2025 \(Yokohama\)**

    In this version, the reconciliation issue associated with Microsoft SQL Server has been resolved.

-   **Version 1.0.12 - June 2025 \(Xanadu\)**

    In this version, the reconciliation issue associated with Microsoft SQL Server has been resolved.

-   **Version 2.1.3 - May 2025**

    Minor bugs related to performance and suite reconciliation have been fixed in this release.

-   **Version 2.1.2 - April 2025**

    Minor reconciliation performance issues have been fixed.

-   **Version 2.1.1 - March 2025**

    Minor fixes to improve the accuracy of Subscription License calculations were made.

-   **Version 2.1.0 - February 2025 \(Yokohama\)**

    This release includes support for CrowdStrike products with license metrics such as Sensor Subscription and Reserved Hourly Average Sensor. This improvement enables the efficient management of entitlements for various CrowdStrike products, including Falcon Endpoint Protection, Discover, and others, ensuring better tracking and compliance.

-   **Version 2.0.0 - February 2025 \(Yokohama\)**

    This release includes the following features when installed with: SAM Foundations: Enables use of the common license metrics: Per User, Per Device, Per Core, Per Processor SAM Professional: Includes features available with SAM Foundations. Enables license compliance for the following publishers: Microsoft, Adobe, Oracle, VMware, and Citrix Improved experience with detailed explanations of licensing calculations for the above publishers.

-   **Version 1.0.10 - December 2024 \(Xanadu\)**

    Minor bug fixes related to Microsoft Reconciliation and Software Lifecycle Report.

-   **Version 1.0.9 - November 2024**

    Minor bug fixes related to Microsoft Reconciliation.

-   **Version 1.0.1 - September 2024**

    Minor bug fixes related to Microsoft Core License Optimization Report.

-   **Version 1.0.0 - August 2024**

    The Software Asset Management App supplements the capabilities of the Software Asset Management \(SAM\) Professional plugin.


