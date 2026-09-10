---
title: Explanation of license rights post reconciliation
description: Get visibility into how your rights are calculated and consumed post the reconciliation process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/explanation-rights-post-recon.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software reconciliation for compliance, Explore, Software Asset Management, IT Asset Management, Asset Management]
---

# Explanation of license rights post reconciliation

Get visibility into how your rights are calculated and consumed post the reconciliation process.

## Overview of explanation of rights

Understand how the Software Asset Management application calculates the number of licenses for your software assets.

A detailed explanation of license rights is provided for the following metric groups:

-   Microsoft
-   IBM
-   Red Hat
-   VMware
-   Oracle
-   SAP
-   Citrix
-   Common

For details on viewing the explanation of license rights, see [View calculations for your licenses in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/licenses-required-workspace.md)

## Tier-based license metric calculation

For a tier-based license metric, the consumed quantity is distributed across defined ranges or tiers. Each tier applies its own factor to the units that fall within that tier, and the results are added together to determine the total number of licenses required. The total is then rounded up to the next whole number.

The following example shows how license rights for a tier-based license metric appear on the Licenses Required by page:

The resource value **res val 2** has 50 units consumed for Content Collector for SAP Applications under the Resource Value Unit - Data Source Record \(1-2 Application Tiers\) license metric. The tiering structure for this license metric defines a factor for each range:

-   Tier 1: Range 1–1, Factor 15
-   Tier 2: Range 2–5, Factor 20
-   Tier 3: Range 6–15, Factor 2.5
-   Tier 4: Range 16–50, Factor 2.25

The factor for each tier applies only to the units within that tier. The application calculates each tier and adds the results: tier 1 \(1 unit × 15 = 15.00\), tier 2 \(4 units × 20 = 80.00\), tier 3 \(10 units × 2.5 = 25.00\), and tier 4 \(35 units × 2.25 = 78.75\). The sum is 198.75, which is rounded up to 199. Based on the tier-based calculation, res val 2 requires 199 rights, which are licensed.

\[Omitted image "tier-based-license-calculation-explanation.png"\] Alt text: License consumption explanation for tier based license metrics

**Note:** If multiple resource value records contribute to the calculated requirement, the **Licenses Required By** tab does not show a tier-by-tier breakdown. To understand the calculation, review the individual resource value records.

## Calculation for Per Device license metric

The following is an example of how an explanation of license rights for a Per Device license metric appears on the Licenses Required by page:

-   The MacBook Air 15" device has installations of Microsoft Office 2016.
-   License consumption explanation: The device D9WW4HYV - MacBook Pro 15" has installs of Microsoft Office 2016. The calculation shows that rounding off the value of licensable installs \(1\) divided by maximum installs per right \(1\) is one licensable install. Since this value can be 0 when the maximum installs per right is infinite, we take the maximum of either the licensable installs calculated \(1\) or 1, which is 1 right. Based on per device licensing, D9WW4HYV - MacBook Pro 15" requires 1 right.

\[Omitted image "explanation-rights-usecase.png"\] Alt text: License consumption explanation

**Parent Topic:**[Software reconciliation for compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/c_SAMReconciliation.md)

