---
title: License usage view
description: The License usage view provides a single plane to understand the license position of all software products. Use it to remediate non-compliance, view reconciliation results, manage removal candidates, and access Software Asset Management related reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/sam-workspace-workbench.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 7
breadcrumb: [Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# License usage view

The License usage view provides a single plane to understand the license position of all software products. Use it to remediate non-compliance, view reconciliation results, manage removal candidates, and access Software Asset Management related reports.

## Overview of the License usage view

The License usage view enables you to view license usage trends for your organization. It helps you forecast license needs by comparing the number of licenses required against the number of licenses purchased. Manage your license positions by purchasing additional rights before software consumption surpasses the number of rights owned.

Access the License usage view by navigating to **Software Asset Workspace** &gt; **License usage**. This view provides a unified dashboard to:

-   Pin publishers in the card view for quick access. Pinned publishers are user-specific and saved.
-   View key metrics for publishers, such as over-licensed amount and true-up cost.
-   Filter publishers by domain and compliance status.
-   Sort publishers by true-up cost, over-licensed amount, and potential savings.
-   Run a reconciliation and view its results.
-   Check the last reconciliation run date.
-   View reclamation summary.
-   View and export reports.
-   Generate a report on your effective license position \(ELP\) data.
-   View publisher cards specific to the software products that you published as part of the phase-wise implementation of Software Asset Management. For more information, see [Publish a specific set of your software products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/add-published-products.md).

\[Omitted image "license-usage-publishers-tab.png"\] Alt text: License usage view showing Publishers tab

## Publishers tab

View the compliance status of all your publishers. Each publisher card displays its color-coded compliance status along with the percentage of compliance. As the products get compliant, the color changes to green.

-   **Compliance status and indicators**

    Each publisher card displays one of the following compliance indicators:

    -   Compliant: Indicated by the color green. All products under the publisher are compliant.
    -   Non-compliant: Indicated by the color red. All products under the publisher are not compliant.
    A red icon \[Omitted image "recon-info-icon.png"\] on a publisher card indicates that reconciliation failed for that publisher. Open the card to read the details. For details on which specific products failed, refer to the navigation tree on the Publisher details page.

    **Note:** Even though a publisher card may display a red icon, you may not notice any failed products on the navigation tree because the failure may have occurred before the product results were generated.

-   **Key metrics display**

    View key metrics for publishers directly on the publisher cards, such as over-licensed amount and true-up cost. Use these metrics to identify publishers that need attention for compliance remediation and cost optimization.

-   **Pin publishers**

    Pin publishers for easy access. Select the bookmark icon on a card to pin it. A pinned publisher moves from the Unpinned publishers section to the Pinned publishers section. Pinned publishers are displayed first, followed by unpinned publishers.

    **Note:** The list of pinned publishers is saved on a per-user basis. The pinned publishers are stored in the Pinned User Publisher \[samp\_pinned\_user\_publisher\] table.

-   **Filter and sort publishers**

    Use filtering and sorting options to analyze publisher compliance details.

    -   Filter by domain and compliance status.
    -   Sort by true-up cost, over-licensed amount, and potential savings.
-   **Switch between card and list views**

    Toggle between card view and list view. The card view is the default.

    -   Card view \(default\): Shows compliance status with color-coded indicators and key metrics.
    -   List view: Lets you analyze publisher compliance details further, such as the publisher with the highest true-up cost or the highest potential savings. You can also filter publishers in this view.
    If the **com.snc.samp.manage.published.products** property is enabled, the list view displays published publishers along with the Status column. If domain separation is supported on your instance, the list view also displays the Domain column.

-   **View publisher details**

    Select a publisher card to open the Publisher details page and view the compliance details of that publisher. For more details, see [Publisher details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/sam-workspace-publisher-details.md).

-   **Phase-wise implementation filtering**

    If you implement Software Asset Management in phases, use the Published status filter to view publisher cards for the software products that you manage in the current phase. Filtering by Published status reduces clutter on the License usage view.

    **Note:** The Published status filter appears when the system property **com.snc.samp.manage.published.products** is enabled on your ServiceNow instance. By default, this filter is set to **Published**, and all publisher cards show details of published products. To view license compliance reports for products that are not published, set this filter to **Unpublished**. To view reports for all products, clear the Published status filter.


## Reconciliation tab

The Reconciliation tab shows all historical reconciliation results, along with the following status:

-   **Completed**: All products and publishers completed reconciliation successfully.
-   **Failed**: All products and publishers failed reconciliation.
-   **Partially Completed**: Only some products or publishers completed reconciliation successfully.

Results of the latest reconciliation run appear in the License usage view. For more details, see [Software reconciliation for compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/c_SAMReconciliation.md).

## Reclamation tab

View consolidated reclamation summary across all publishers, SaaS integrations, installed software, and reconciliation flows. Access individual records to review the reclamation details and act accordingly.

## Reports tab

Create, view, and run reports from this tab. The following base system reports are available:

-   [Software product lifecycle report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/software-models-and-entitlements.md)
-   [Software license compliance position](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/sam-license-position-report.md)
-   [Azure BYOL realized savings report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/azure-byol-realized-savings-report.md)
-   [Software models with deactivated discovery maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/sam-content-updates.md)
-   [Oracle Database Deployments per Agreement report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/oracle-server-agreement.md)
-   [Oracle Infrastructure report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/oracle-infrastructure-report.md)
-   [Microsoft Windows and SQL Server infrastructure details reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/azure-byol-realized-savings-report.md)
-   [SaaS detection report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/shadow-saas-analytics.md)
-   [Microsoft Server Infrastructure and License Consumption report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/device-license-consumption-report.md)

To create and manage reports, see [Create and manage reports in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/create-new-report-workspace.md).

## ELP Grouping tab

Generate a report that groups your effective license position \(ELP\) data on existing reconciliation groups without re-running the reconciliation process.

For details on generating an ELP report, see [Generate an Effective License Position \(ELP\) report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/generate-elp-report-sam.md).

**Related topics**  


[Publisher details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/sam-workspace-publisher-details.md)

[License operations view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/operations-workspace.md)

[Software reconciliation for compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/c_SAMReconciliation.md)

[Software installation optimization and removal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/c_SAMOptimization.md)

[Run software reconciliation in the workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/run-recon-workspace.md)

