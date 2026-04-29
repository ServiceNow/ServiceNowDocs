---
title: License usage view
description: Use the license usage view as a single plane to understand the license position of all software products, remediate non-compliance, view reconciliation results, view, or add removal candidates, and view Software Asset Management related reports.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# License usage view

Use the license usage view as a single plane to understand the license position of all software products, remediate non-compliance, view reconciliation results, view, or add removal candidates, and view Software Asset Management related reports.

## Overview of the License usage view

The License usage view enables you to view the license usage trends for your organization and helps forecast the needs of your organization by trending the number of licenses required against the number of licenses purchased. Manage your license positions by purchasing additional rights before software consumption surpasses the number of rights owned.

Access the License usage view by navigating to **Software Asset Workspace** &gt; **License usage**.

![License usage view](../image/license-usage-publishers-tab.png)

Use the License usage view to:

-   pin publishers \(user specific, saved\).
-   view key metrics for the publishers, such as over-licensed amount and true-up cost.
-   filter by domain and compliance status.
-   sort by true-up cost, over-licensed amount, and potential savings.
-   run a reconciliation and view its results.
-   be informed about the last reconciliation run.
-   view and add new removal candidates.
-   view and export reports.
-   generate a report on your ELP data.
-   view publisher cards specific to the software products that you published as part of the phase-wise implementation of Software Asset Management. For more information, see [Publish a specific set of your software products](../task/add-published-products.md).

    **Note:** The filter for published status is automatically applied.


## Publishers tab

View the compliance status of all your publishers. Each publisher card displays its color-coded compliance status along with the percentage of compliance. As the products get compliant, the color changes to green.

-   compliant: Indicated by the color green. All products under the publisher are compliant.
-   non-compliant: Indicated by the color red. All products under the publisher aren’t compliant.

A red icon ![](../image/recon-info-icon.png) on a publisher card indicates that reconciliation failed for that publisher. Open the card to read the details. For details on which specific products failed, refer to the navigation tree on the Publisher details page.

**Note:** Even though a publisher card may display a red icon, you may not notice any failed products on the navigation tree because the failure may have occurred before the product results were generated.

You can view publishers by toggling between a card view and a list view. The list view lets you further analyze publisher compliance details such as the publisher with highest true up or the highest potential savings or filter on publishers. By default, the card view appears. If the **com.snc.samp.manage.published.products** property is enabled on your instance, the list view displays published publishers along with the Status column. If domain separation is supported on your instance, the list view displays the Domain column too.

The pinned publishers are displayed followed by unpinned publishers. To view the compliance of selected publishers, you can pin publishers for easy access. Select the bookmark icon on a card to pin it. As soon as you pin a publisher card, it moves from the Unpinned publishers section to the Pinned publishers section.

**Note:** The list of pinned publishers is saved on a per-user basis. The pinned publishers are stored in the Pinned User Publisher \[samp\_pinned\_user\_publisher\] table.

View publisher cards related to the software products that you manage in a phase-wise implementation of Software Asset Management using the Published status filter. Filtering by Published status enables you to reduce clutter on the License usage view.

**Note:** The Published status filter is shown when the system property **com.snc.samp.manage.published.products** is enabled on your ServiceNow instance. By default, this filter is set to **Published** and all the publisher cards show details of published products. However, you can also view license compliance reports related to the products that aren't published by setting this filter to **Unpublished**. To view reports related to all the products, clear the Published status filter.

## Publisher details

To view compliance details about a publisher, select a publisher card. A summary of that publisher's compliance appears in the Publisher details page.

![Publisher details page](../image/publisherdetails-updated.png "Publisher details page")

View the following related lists for a publisher and its products.

-   Product Results: A product result record for a licensable product is generated after reconciliation even if there are no software models defined for the product.
-   Software Model Results: A software model result record is generated for each individual software model related to a product and is only created when a software model or entitlement exists for the product.

    **Note:** To generate software models results for all software models, with or without entitlements, you can set the property **com.snc.samp.unlicensed\_smr\_creation** to true. By default this property is set to false.

-   License Metric Results: A license metric result record is generated for each license metric associated with a software model.
-   Removal candidates: list of removal candidates.
-   Entitlements: entitlements associated to the publisher.
-   Product install analysis: the license consumption analysis for products of a publisher. Open a record to view a hierarchical node map that illustrates how the installations of a specific product are being licensed. Product install analysis is available at the publisher level and not at the individual product level. For more details, see [View license usage for your installations](../task/view-install-usage.md).

To prevent clutter in the Publisher details page, software models results are shown only for software models that have entitlements. Software models without any entitlements are shown at the product level in the product results. To view software model results for all software models with or without entitlements, you can set the property, **com.snc.samp.unlicensed\_smr\_creation**, to true. By default, this property is set to false.

The navigation tree for the publisher appears on the Publisher details page with one of the following compliant statuses:

-   Compliant: Reconciliation completed successfully and it was determined that installations and subscriptions are in compliance.
-   Not compliant: Reconciliation completed successfully and it was determined that the installations and subscriptions aren’t in compliance with purchased licenses.
-   Failed: Reconciliation failure occurred and so can't correctly determine compliance. If a product fails, then everything underneath that product, such as software model results, also fails.

The navigation view shows license compliance details of products that were published. Scroll down to the reports mentioned in the Publisher metrics table to view details of published products. If you want to view details and compliance results of other unpublished products, you must set the Published status filter to **Unpublished**.

In the navigation view, a non-consumption icon is displayed next to a software model that has not utilized any licenses. Such software models are always positioned at the bottom of the tree and no software model results are shown for that software model.

A brief summary of metrics appears along with related lists pertaining to that publisher. For details on the metrics, refer to the Publisher metrics table. For details on the related lists, refer to [License usage publisher fields in workspace](../reference/workbench-publisherfields-workspace.md).

The navigation tree enables you to perform the following actions:

-   drill down to a product, software model, or license metric to view the calculation and compliance information from the latest reconciliation results.
-   filter products \(active filtering, including collapsed items\).
-   expand and collapse tree links.

By default, the navigation tree is collapsed.

## Publisher metrics

The table explains the report, the source, and the description of each publisher metric.

<table id="table_vt5_tp3_g3c"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

True-up cost

</td><td>

Product Result \[samp\_product\_result\]

</td><td>

Estimated cost of remediating unlicensed installations based on the lowest number of rights needed \(rights needed multiplied by average price per right from entitlements\).The lowest cost from Purchase Rights remediation options.

</td></tr><tr><td>

Potential savings

</td><td>

Removal Candidate\[samp\_sw\_reclamation\_candidate\]

</td><td>

Estimated cost of savings if software installations are reclaimed. The sum of all potential savings from all removal candidates.Select the report to see the list of removal candidates.

</td></tr><tr><td>

Actual savings

</td><td>

Removal Candidate\[samp\_sw\_reclamation\_candidate\]

</td><td>

The total savings achieved if removal candidates are reclaimed.Select the report to see the list of removal candidates.

</td></tr><tr><td>

Unlicensed entities

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

 Software Subscription \[samp\_sw\_subscription\]

 Oracle Options \[samp\_oracle\_options\].

 SAP Users \[samp\_sap\_system\_user\]

 SAP Engine Usage \[samp\_sap\_sw\_client\_access\]

 Entity unlicensed reason \[samp\_entity\_unlicensed\_reason\]

 Unlicensed reason \[samp\_install\_unlicensed\_reason\]

</td><td>

Indicates the unlicensed entities for this publisher, product, and software model. The following are some of the indicators:-   Unlicensed installs: refers to installations for which you have purchased some entitlements, but the rights owned are not sufficient to cover all the entities that require rights. You can perform remediation actions such as removing unlicensed installations or you can purchase more rights.
-   Non-entitled product installs: indicates products with installations at ServiceNow that currently have no associated entitlements. You need to create entitlements for these products.
-   Installs requiring action: indicates an action that you need to perform to fix an issue for an installation, such as problems with CIs, entitlement, or software model setup.

After you select Installs requiring action, a list appears showing installs that need action, organized by reason categorizes. Select **Show all** to expand and view the specific list of installs. You can further select a value in the Reason column for a more detailed explanation of the reason. For details on reconciliation results such as product results and software model results, see [Software reconciliation results](software-reconciliation-results.md).

**Note:** An installation may have more than one issue. It is necessary to address each issue to fully resolve problems with an installation. Therefore, the number shown on the progress indicator and the details when you drill down may not align. Please ensure all issues are fixed for the installation.

-   Unlicensed subscriptions: indicates that there are insufficient entitlements to cover the purchased subscriptions on SaaS. Therefore, you need to create the necessary entitlements​
-   Non-entitled product subscriptions: indicates subscriptions at ServiceNow that currently have no associated entitlements. You need to create entitlements for these subscriptions.
-   Subscriptions requiring action: Analyze subscription-related issues and perform necessary corrective measures.
-   Unlicensed client access: refers to unlicensed CAL records on account of not having enough rights on entitlements to cover the CAL records. You need to purchase more CAL licenses for the products.
-   Unlicensed options: refers to unlicensed Oracle Database options and management packs.

Select the number adjacent to each category for a more detailed explanation of each installation, including the reason and causes of their unlicensed status.

</td></tr><tr><td>

Progress indicators

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

 Requested Item \[sc\_req\_item\]

 Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

Indicates the compliance progress already made for this publisher, product, and software model. The progress indicators differ for each publisher. The following are some of the indicators:

-   Ignored installs: installations ignored from the reconciliation process.
-   Inactive installs: Indicates software installs that are marked as inactive by Software Asset Management Professional. These installs aren’t included in license calculation and don’t require any action.
-   Ignored subscriptions: Indicates subscriptions that are marked as inactive by Software Asset Management Professional. These subscriptions aren’t included in license calculations and do not require any action.
-   Removal candidates: Details of all removal candidates created for reasons such as low usage and unlicensed install removal.
-   Health issues: Displays all health check issues for your Software Asset Management configurations. Select a health check issue to address and fix the error. If there are no health issues, the Health issue indicator isn't shown.

 Select the number adjacent to each category for a more detailed explanation of each installation.

</td></tr></tbody>
</table>## Reconciliation tab

You can view all the historical reconciliation results in this tab along with the following status:

-   **Completed**: If all the products and publishers completed reconciliation successfully.
-   **Failed**: If all the products and publishers failed reconciliation.
-   **Partially Completed**: If only some products or publishers completed reconciliation successfully.

Results of the latest reconciliation run are shown in the License usage view. For more details, see [Software reconciliation for compliance](c_SAMReconciliation.md).

## Removal candidates tab

View a list of all removal candidates in this tab. Removal candidates are used to reclaim software installations that aren’t being used.

You can also create removal candidates. For more details, see [Create a software removal candidate in workspace](../task/add-sw-removal-workspace.md).

## Reports tab

You can create, view, and run reports from this tab. All the following base system reports are available in this tab:

-   [Software product lifecycle report](software-models-and-entitlements.md)
-   [Software license compliance position](sam-license-position-report.md)
-   [Azure BYOL realized savings report](../reference/azure-byol-realized-savings-report.md)
-   [Software models with deactivated discovery maps](sam-content-updates.md)
-   [Oracle DB Server Deployments per Agreement report](../reference/oracle-server-agreement.md)
-   [Oracle Infrastructure report](../reference/oracle-infrastructure-report.md)
-   [Microsoft Windows and SQL Server infrastructure details reports](../reference/azure-byol-realized-savings-report.md)
-   [SaaS detection report](../reference/shadow-saas-analytics.md)
-   [Microsoft Server Infrastructure and License Consumption report](device-license-consumption-report.md)

To create and manage reports, see [Create and manage reports in workspace](../task/create-new-report-workspace.md).

## ELP Grouping tab

Generate a report that groups your effective license position \(ELP\) data on existing reconciliation groups without needing to re-run the reconciliation process. For details on generating a ELP report, see [Generate an Effective License Position \(ELP\) report](../task/generate-elp-report-sam.md).

