---
title: License usage view
description: Use the license usage view as a single plane to understand the license position of all software products, remediate non-compliance, view reconciliation results, view, or add removal candidates, and view Software Asset Management related reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/sam-workspace-workbench.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Software Asset Workspace, Explore, Software Asset Management, IT Asset Management, Asset Management]
---

# License usage view

Use the license usage view as a single plane to understand the license position of all software products, remediate non-compliance, view reconciliation results, view, or add removal candidates, and view Software Asset Management related reports.

## Overview of the License usage view

The License usage view enables you to view the license usage trends for your organization and helps forecast the needs of your organization by trending the number of licenses required against the number of licenses purchased. Manage your license positions by purchasing additional rights before software consumption surpasses the number of rights owned.

Access the License usage view by navigating to **Software Asset Workspace** &gt; **License usage**. This view provides a unified dashboard to:

-   View license compliance status and trends across all software publishers.
-   Monitor key metrics such as over-licensed amount, true-up cost, and potential savings.
-   Filter and sort publishers by compliance status, domain, and published status.
-   Pin publishers for quick access and organize by preferred view \(card or list\).
-   Check the last reconciliation run date and review all historical reconciliation results.
-   Run new reconciliations and review detailed product and software model results.
-   View and create software removal candidates to reclaim unused licenses.
-   Generate and export reports on license position, compliance, and asset lifecycle.
-   Create effective license position \(ELP\) reports grouped by your specified criteria.
-   View publisher cards specific to the software products that you published as part of the phase-wise implementation of Software Asset Management. For more information, see [Publish a specific set of your software products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/add-published-products.md).

\[Omitted image "license-usage-publishers-tab.png"\] Alt text: License usage view showing Publishers tab

## Publishers tab

View the compliance status of all your publishers. Each publisher card displays its color-coded compliance status along with the percentage of compliance. As the products get compliant, the color changes to green.

-   **Compliance status and indicators**

    Each publisher card displays color-coded compliance indicators:

    -   Compliant: Indicated by the color green. All products under the publisher are compliant.
    -   Non-compliant: Indicated by the color red. All products under the publisher are not compliant.
    A red icon on a publisher card indicates that reconciliation failed for that publisher. Open the card to read the details. For details on which specific products failed, refer to the navigation tree on the Publisher details page.

    **Note:** Even though a publisher card may display a red icon, you may not notice any failed products on the navigation tree because the failure may have occurred before the product results were generated.

-   **Key metrics display**

    View key metrics for publishers directly on the publisher cards, such as over-licensed amount and true-up cost. These metrics enable you to quickly identify publishers that require attention for compliance remediation and cost optimization.

-   **Pin publishers**

    Pin publishers to your view for quick access. Pinned publishers are user-specific and saved for your future sessions, allowing you to focus on your most-managed software assets. Pinned publishers appear at the top of your Publishers list for easy reference. Select the bookmark icon on a card to pin it. The pinned publishers are stored in the Pinned User Publisher \[samp\_pinned\_user\_publisher\] table.

-   **Filter and sort publishers**

    Use filtering and sorting options to analyze publisher compliance details.

    -   Filter by domain and compliance status to isolate publishers by organizational structure or compliance state.
    -   Sort by true-up cost, over-licensed amount, and potential savings to prioritize remediation efforts and identify cost-saving opportunities.
    If the `com.snc.samp.manage.published.products` property is enabled on your instance, the list view displays published publishers along with the Status column, helps you to focus on software products relevant to your current implementation phase.

    If domain separation is enabled, filtering and sorting options reflect your domain-specific publisher data.

-   **Switch between card and list views**

    Toggle between card view and list view to analyze publisher compliance data in your preferred format.

    -   Card view \(default\): Provides a visual representation of compliance status with color-coded indicators and key metrics at a glance.
    -   List view: Offers detailed columns for deeper analysis of publisher compliance details, including publishers with the highest true-up cost, highest potential savings, or specific compliance status. The list view further supports filtering and sorting for enhanced data exploration.
    If the `com.snc.samp.manage.published.products` property is enabled, the list view displays a Status column indicating the publication status of each publisher for phase-wise implementation tracking.

-   **View publisher details**

    Select a publisher card to open the Publisher details page and view comprehensive information about that publisher. The Publisher details page includes product results, software model results, license metric results, related lists, compliance indicators, and available remediation options. For more details, see [Publisher details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sam-workspace-publisher-details.md).

-   **Phase-wise implementation filtering**

    For organizations implementing Software Asset Management in phases, the Published status filter automatically applies to show only relevant software products. View publisher cards specific to the software products that you published as part of the phase-wise implementation of Software Asset Management. The system property `com.snc.samp.manage.published.products` controls visibility of published products.


## Reconciliation tab

The Reconciliation tab shows all historical reconciliation runs and their completion status:

-   **Completed**: All products and publishers completed reconciliation successfully.
-   **Failed**: All products and publishers failed reconciliation.
-   **Partially Completed**: Some products or publishers completed successfully.

The most recent results appear in the Publishers tab. To run a new reconciliation or review detailed results, see [Software reconciliation for compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/c_SAMReconciliation.md).

## Removal candidates tab

View and manage software installations marked for removal. Removal candidates help you reclaim licenses for software no longer in use.

For information on creating and managing removal candidates, see [Create a software removal candidate in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/add-sw-removal-workspace.md).

## Reports tab

Create, view, and run predefined reports on software licensing, compliance, and asset data. Available reports include:

-   [Software product lifecycle report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-models-and-entitlements.md)
-   [Software license compliance position report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sam-license-position-report.md)
-   [Azure BYOL realized savings report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/azure-byol-realized-savings-report.md)
-   [Software models with deactivated discovery maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sam-content-updates.md)
-   [Oracle Server Agreement report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/oracle-server-agreement.md)
-   [Oracle infrastructure report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/oracle-infrastructure-report.md)
-   [Device license consumption report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/device-license-consumption-report.md)

To create and manage reports, see [Create and manage reports in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-new-report-workspace.md).

## ELP Grouping tab

Generate an Effective License Position \(ELP\) report that groups reconciliation data by your specified criteria without re-running reconciliation.

For details on generating a ELP report, see [Generate an Effective License Position \(ELP\) report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/generate-elp-report-sam.md).

**Related topics**  


[License operations view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/operations-workspace.md)

[Software reconciliation for compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/c_SAMReconciliation.md)

[Software installation optimization and removal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/c_SAMOptimization.md)

[Run software reconciliation in the workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/run-recon-workspace.md)

