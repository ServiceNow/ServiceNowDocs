---
title: Software install deduplication
description: Software install deduplication consolidates redundant installation records for the same product on a single device, improving data accuracy and license compliance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/deduplication-rule.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Software install deduplication, deduplication logic, software duplicate installs]
breadcrumb: [Software discovery and normalization, Exploring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Software install deduplication

Software install deduplication consolidates redundant installation records for the same product on a single device, improving data accuracy and license compliance.

Software upgrades, incomplete removals of installs, and multiple discovery sources often create duplicate software installations on the same device. Deduplication is the process of identifying redundant installation records and designating one record as the primary installation while marking others as duplicates. Without deduplication, inflated license counts, inaccurate entitlement reports, and conflicting installation records complicate compliance and cost management.

Starting with the Brazil release, the deduplication logic includes the following improvements:

-   The deduplication logic correctly identifies duplicates within the same discovery source or across discovery sources consistently.
-   When duplicates are found, the logic has a consistent way to choose which record to keep as the primary installation.
-   The Software Asset Management application users get a clear explanation of why a particular installation is marked as primary and others as duplicates.

## Configure a product-level deduplication rule

The product must exist as a normalized record in the Software Models \[cmdb\_software\_product\_model\] table before you can assign a deduplication rule. A deduplication rule can't be assigned to unnormalized products.

The software install deduplication framework provides three version-matching levels that control how the system identifies duplicate installations:

-   **Exact**

    The system matches installations only when the full version string is identical. For example, SQL Server 2019.1 and SQL Server 2019 are treated as different versions and aren't deduplicated together. Use this level for software with discrete version lifecycles.

-   **Major**

    The system matches installations when the major version is the same, regardless of point release differences. For example, both SQL Server 2019.1 and SQL Server 2019 are treated as the same major version and are deduplicated together. Use this level for most enterprise software.

    **Note:** This is the default version-matching level applied when a custom rule is not defined for a product.

-   **Any**

    The system ignores version entirely and consolidates all installations of the same software title on a device into a single primary installation. Use this level for volatile or auto-updating software such as Google Chrome, where version differences are frequent and don't impact licensing.


For more information about configuring a deduplication rule for a software product, see [Create a custom deduplication rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-custom-deduplication-rule.md).

## Software install deduplication logic

The deduplication logic operates in two main stages:

-   **Duplicate detection**

    The system compares software installations and identifies duplicates based on version matching. By default, the system considers installations duplicate if the major version component of the normalized version is identical. For example, SQL Server Enterprise 2019.1 and 2019.3 are duplicates because both have major version 19. However, you can configure custom comparison levels if required. For more information about configuring deduplication rule for a software product, see [Create a custom deduplication rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-custom-deduplication-rule.md).

-   **Primary selection**

    After the deduplication logic identifies duplicate installations, it applies tiered selection criteria to choose which installation becomes the primary record. The criteria tiers are evaluated in sequence, and if a tie occurs at any tier, the system moves to the next tier. The selection criteria, in order of priority, are:

    -   Discovery source reliability: Installations from more reliable discovery sources are preferred.
    -   Information completeness: Installations with more complete information are preferred.
    -   Installation version: The latest version is selected as primary.

For example, your organization operates multiple servers and workstations running SQL Server Enterprise. Over time, discovery tools scan your environment and report installations of this product across different devices, from different discovery sources, and at different scan times. Your software records now contain three separate installation records for SQL Server Enterprise, each showing slightly different version information:

|Installation|Version|Scan Date|Completeness|
|------------|-------|---------|------------|
|SQL Server Install \#1|2019|Jan 15, 2026|95% \(all major files present\)|
|SQL Server Install \#2|2019.1|Jul 10, 2026|100% \(complete installation\)|
|SQL Server Install \#3|2019|Jul 8, 2026|60% \(partial, missing executables\)|

Without deduplication, your licensing compliance report counts all three installations. Entitlement data shows three instances when, in reality, fewer active SQL Server installations may exist in your environment.

**Parent Topic:**[Software discovery and normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/c_SAMDiscovery.md)

**Related topics**  


[Create a custom deduplication rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-custom-deduplication-rule.md)

