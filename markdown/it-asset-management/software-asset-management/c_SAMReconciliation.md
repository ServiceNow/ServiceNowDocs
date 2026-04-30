---
title: Software reconciliation for compliance
description: Automated license reconciliation keeps license positions accurate and up-to-date without manual calculations. Reconciliation runs weekly or on demand.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software reconciliation for compliance

Automated license reconciliation keeps license positions accurate and up-to-date without manual calculations. Reconciliation runs weekly or on demand.

Reconciliation is a scheduled job that is run at a specified frequency \(default is weekly\). It can also be run on demand for specific or all publishers, groups, and subgroups.

Group and subgroup values include country, department, company, region, or cost center. Default group and subgroup [properties](../reference/sam-properties.md) that apply to the weekly reconciliation run can be set in **Software Asset** &gt; **Administration** &gt; **Properties**.

When reconciliation runs, a list of reconciliation results is created that shows the compliance status of software products concerning discovery and entitlements. Users with the sam\_user role can view reconciliation results.

In addition to creating a purchase order for new software licenses, additional remediation options are available in software model results. Use the results to automatically create and remove allocations, remove unallocated installs, and remove unlicensed installs.

Review reconciliation results in a simplified License Workbench view, and use the License Position report to see compliance details for each software model in a single list.

-   **[Software reconciliation results](software-reconciliation-results.md)**  
Software reconciliation results show the compliance status of software products concerning discovery and entitlements. Users with the sam\_user role can view the reconciliation results.
-   **[Accurately reporting your software true-up cost](accurate-trueup-cost.md)**  
Accurately report your software true-up costs to avoid compliance issues.
-   **[Software license compliance position](sam-license-position-report.md)**  
The Software Asset Management License Position report shows compliance details for each software model in a single list.
-   **[Grouping and consumption rules in reconciliation](grouping-consumptionrules.md)**  
Grouping and consumption rules can work in tandem during the reconciliation process in the Software Asset Management application.
-   **[Determining license compliance through Virtualization Adapter](software-recon-virt-tech.md)**  
Software Asset Management Virtualization Adapter determines the license compliance of Microsoft SQL Server, Windows Server, and Red Hat Enterprise Linux Server \(RHEL\) deployed on virtualization technologies by applying license compliance rules. This feature is activated and installed with the base system in Software Asset Management.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

