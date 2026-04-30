---
title: Software reconciliation for compliance
description: Automated license reconciliation keeps license positions accurate and up-to-date without manual calculations. Reconciliation runs weekly or on demand.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software reconciliation for compliance

Automated license reconciliation keeps license positions accurate and up-to-date without manual calculations. Reconciliation runs weekly or on demand.

## Overview of reconciliation

Reconciliation is a scheduled job that is run at a specified frequency \(default is weekly\). It can also be run on demand for specific or all publishers, groups, and subgroups.

Group and subgroup values include country, department, company, region, or cost center. Default group and subgroup [properties](../reference/sam-properties.md) that apply to the weekly reconciliation run can be set in **Software Asset** &gt; **Administration** &gt; **Properties**.

When reconciliation runs, a list of reconciliation results is created that shows the compliance status of software products concerning discovery and entitlements. Users with the sam\_user role can view reconciliation results.

In addition to creating a purchase order for new software licenses, additional remediation options are available in software model results. Use the results to automatically create and remove allocations, remove unallocated installs, and remove unlicensed installs.

Review reconciliation results in a simplified License Workbench view, and use the License Position report to see compliance details for each software model in a single list.

## Upgrade considerations for customized reconciliation script includes

Starting from the Yokohama release, all the reconciliation script includes are being moved from the family release to the Software Asset Management store application \(com.sn\_itam\_samp'\).

**Note:** When you activate the Software Asset Management Professional \(com.sn\_samp\_master\) plugin or the Software Asset Management Foundation \(com.snc.sams\) plugin, the Software Asset Management store application \(com.sn\_itam\_samp'\) is automatically activated.

When upgrading to Yokohama, if you have made customizations to reconciliation script includes, you need to move your customizations to the new script includes. The old script includes will be deprecated.

-   **[Software reconciliation results](software-reconciliation-results.md)**  
Software reconciliation results show the compliance status of software products concerning discovery and entitlements. Users with the sam\_user role can view the reconciliation results.
-   **[Accurately reporting your software true-up cost](accurate-trueup-cost.md)**  
Accurately report your software true-up costs to avoid compliance issues.
-   **[Software license compliance position](sam-license-position-report.md)**  
The Software Asset Management License Position report shows compliance details for each software model in a single list.
-   **[Determining license compliance through Virtualization Adapter](software-recon-virt-tech.md)**  
Software Asset Management Virtualization Adapter determines the license compliance of several software products deployed on virtualization technologies by applying license compliance rules. This feature is activated and installed with the base system in Software Asset Management.
-   **[Explanation of license rights post reconciliation](explanation-rights-post-recon.md)**  
Get visibility into how your rights are calculated and consumed post the reconciliation process.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

