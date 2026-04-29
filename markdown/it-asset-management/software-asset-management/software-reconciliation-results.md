---
title: Software reconciliation results
description: Software reconciliation results show the compliance status of software products concerning discovery and entitlements. Users with the sam\_user role can view the reconciliation results.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Software reconciliation for compliance, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software reconciliation results

Software reconciliation results show the compliance status of software products concerning discovery and entitlements. Users with the sam\_user role can view the reconciliation results.

When software reconciliation runs, it calculates compliance based on how many rights are in use compared to the number of active rights that have been purchased. Reconciliation runs weekly or on demand for a specific publisher or all publishers. This process generates a list of reconciliation results that display the compliance status of the software in relation to discovery and entitlements. For more details on running software reconciliation, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).

There are three tiers of reconciliation results:

-   Product Results
-   Software Model Results
-   License Metric Results

You can view reconciliation results using both Core UI and Software Asset Workspace.

<table id="table_x4d_vps_ncc"><thead><tr><th>

Interface

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Core UI

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **Historical Results**.
2.  Select a reconciliation result.
3.  On the Reconciliation Result form, select a Product Results record to view the product result details.

</td></tr><tr><td>

Software Asset Workspace

</td><td>

1.  Navigate to **Software Asset Workspace** &gt; **License usage**.
2.  Select a publisher card and then select a Product Results record to view the product result details.

</td></tr></tbody>
</table>## Reconciliation results

-   **Product Results**

    ![Product Results and related lists for SQL Server](../image/product-results.png)

    These results are for all models and installations associated with a software product and are specific to a publisher. Product results for licensable products are generated after reconciliation even if the products don’t have defined software models for them. These results determine the license compliance status of the product. Additionally, product results provide details on true-up cost, overlicensed amount, and potential savings. The following related lists appear when you select a Product Results record:

    -   Software Model Results
    -   Licensed Installs
    -   Unlicensed Installs \(SAP: Unlicensed Users or Unlicensed Engines\)
    -   Unlicensed Subscriptions \(Subscription-based software\)
    -   Removal Candidates
-   **Software Model Results**

    ![Software Model Results and related lists for SQL Server](../image/software-model-results-workspace.png)

    These results are for each individual software model related to the product. The Software Model Results appear as a related list on the product results records after reconciliation is run. A software model results record is created only when a software model or entitlement exists for the software product. The following related lists appear when you select the software model details:

    -   License Metric Results
    -   Remediation Options
    -   Licensed Installs
    -   Unlicensed Installs \(SAP: Unlicensed Users\)
    -   Unlicensed Subscriptions \(Subscription-based software\)
    -   Unlicensed Consumptions \(Consumption-based software models\)
    -   Unlicensed Options \(Oracle only\)
    -   Removal Candidates
    -   Purchase Orders \(only when the Procurement \(com.snc.procurement\) plugin is active\)
    For more details on software model results related lists and descriptions, see [View software model results](../task/t_ViewSWModelResults.md).

-   **License Metric Results**

    ![License Metric Results and related lists for SQL Server](../image/license-metric-results.png)

    These results are for each license metric associated with the software model. The License Metric Results appear as a related list on the software model results. License metric result details include rights owned and rights used, and the license allocation breakdown so that you can determine your options to stay compliant. There can be multiple license metric results for a software model because multiple licenses can be purchased for the same software.

    From the Software Model Results form, you can drill down on a specific metric result. The following related lists appear when you select license metrics results details:

    -   Rights Used By \(This tab isn’t visible for the Resource Value Unit \(RVU\) IBM license metric.\)
    -   Licensed Installs
    -   Installs Used \(SAP: System Users\)
    -   Downgrades/Upgrades
    -   Licensed Subscriptions
    -   Cloud Special Rights \(This tab is visible only if you have cloud installations on cloud platforms such as AWS or Azure.\)
    For more details on license metric results related lists and descriptions, see [Software model results license metric results fields](../reference/license-metric-results-fields.md).


**Parent Topic:**[Software reconciliation for compliance](c_SAMReconciliation.md)

