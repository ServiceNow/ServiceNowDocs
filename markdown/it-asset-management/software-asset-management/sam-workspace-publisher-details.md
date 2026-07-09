---
title: Publisher details
description: Monitor publisher license compliance, review true-up costs and potential savings, and identify software installations that requires remediation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/sam-workspace-publisher-details.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [License usage view, Software Asset Workspace, Explore, Software Asset Management, IT Asset Management, Asset Management]
---

# Publisher details

Monitor publisher license compliance, review true-up costs and potential savings, and identify software installations that requires remediation.

## Overview of the Publisher details

Select a publisher card from the Publishers tab to open the Publisher details page. The Publisher details page provides a detailed view of the publisher's compliance status, license metrics, product results, software model results, and related software installations.

Use the Publisher details page to analyze the implementation path: navigate from the publisher to products, check software installations requiring action, review remediation options, examine license metric results, and determine license requirements needed to achieve compliance.

\[Omitted image "publisherdetails-updated.png"\] Alt text: Publisher details page showing product navigation, license metrics, and compliance-related information.

## Navigation tree

The navigation tree for the publisher appears on the Publisher details page with one of the following compliant statuses:

-   Compliant: All products and installations under this publisher are fully compliant with license entitlements.
-   Not compliant: One or more products or installations under this publisher are not compliant with license entitlements.
-   Failed: Reconciliation failed for this publisher or one of its products. Review reconciliation logs to identify and resolve the failure.

Use the navigation tree to drill down through the publisher hierarchy and identify which products and installations require remediation actions to achieve compliance.

## Publisher metrics

The table explains the report, the source, and the description of each publisher metric.

<table id="table_oqt_xty_rjc"><thead><tr><th>

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

After you select Installs requiring action, a list appears showing installs that need action, organized by reason categorizes. Select **Show all** to expand and view the specific list of installs. You can further select a value in the Reason column for a more detailed explanation of the reason. For details on reconciliation results such as product results and software model results, see [Software reconciliation results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/software-reconciliation-results.md).

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
</table>## Related lists

The Publisher details page includes the following related lists to support detailed analysis and remediation:

|Related list|Purpose|
|------------|-------|
|Product Results|Displays reconciliation results for each product under the publisher, including compliance status, license metrics, and unlicensed installations requiring action.|
|Software Model Results|Shows reconciliation results at the software model level, including compliance status, entitlement details, and license calculations for each model. A software model result is not generated for products without software models or entitlements unless the **com.snc.samp.unlicensed\_smr\_creation** property is enabled.|
|License Metric Results|Provides detailed license metric calculations, including licensed count, unlicensed count, true-up requirements, and potential savings for each license metric.|
|Entitlements|Lists all entitlements \(licenses\) defined for the publisher's products, including license counts, license models, and compliance status.|
|Product Install Analysis|Provides a comprehensive analysis of software installations across the publisher's products, including installation counts by status, compliance alignment, and remediation recommendations. For more details, see [View license usage for your installations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/view-install-usage.md).|
|Removal candidates|Lists software installations identified for removal or reclamation. Displays removal candidate details including number, name, publisher, product, potential savings, and current state for managing unused software.|
|Remediation options|Displays available remediation actions to address non-compliance for each product or installation, including purchasing licenses, removing installations, updating license allocations, or modifying software models and entitlements.|

For more details on the related lists, refer to [License usage publisher fields in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/workbench-publisherfields-workspace.md).

## Remediation workflow and options

The Publisher details page supports a systematic workflow for achieving compliance through the following remediation options and actions:

-   **Review installation details**

    Examine individual software installations linked to the publisher. Identify installations requiring action, including unlicensed, over-licensed, or conflicting installations.

-   **Assess remediation options**

    For each non-compliant product or installation, review available remediation options: purchase additional licenses, remove unused installations, update license allocations, or modify software models and entitlements.

-   **Apply license metric results**

    Use license metric calculation results to determine the most cost-effective remediation path. Compare true-up cost versus potential savings to prioritize actions that deliver maximum compliance and cost benefit.

-   **Execute remediation actions**

    Process removal candidates to reclaim unused licenses, allocate additional licenses to compliant installations, or update entitlements to match discovered software usage.

-   **Verify license requirements**

    Confirm that remediation actions have resolved non-compliance and that total licenses required now aligns with or is less than licenses purchased. Run a new reconciliation to validate the updated compliance status.


**Related topics**  


[License usage view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sam-workspace-workbench.md)

[License operations view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/operations-workspace.md)

[Software license metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/c_SAMLicenseMetrics.md)

[Software installation optimization and removal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/c_SAMOptimization.md)

[Allocation management on Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/allocation-management-sam.md)

[Reclaim software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/reclaiming-software-sam.md)

