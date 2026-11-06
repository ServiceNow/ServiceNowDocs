---
title: Publisher details
description: Monitor publisher license compliance, review true-up costs and potential savings, and identify software installations that require remediation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/sam-workspace-publisher-details.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 6
breadcrumb: [License usage view, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Publisher details

Monitor publisher license compliance, review true-up costs and potential savings, and identify software installations that require remediation.

## Overview of the Publisher details

Select a publisher card on the Publishers tab to open the Publisher details page. The page shows a summary of the publisher's compliance status, along with related lists for the publisher and its products.

\[Omitted image "publisherdetails-sam.png"\] Alt text: Publisher details page

## Navigation tree

The navigation tree for the publisher appears on the Publisher details page with one of the following compliance statuses:

-   Compliant: Reconciliation completed successfully, and the installations and subscriptions are in compliance.
-   Not compliant: Reconciliation completed successfully, and the installations and subscriptions are not in compliance with purchased licenses.
-   Failed: Reconciliation failed, so compliance cannot be determined correctly. If a product fails, everything under that product, such as software model results, also fails.

The navigation view shows the license compliance details of products that were published. To view details and compliance results for unpublished products, set the Published status filter to **Unpublished**.

A non-consumption icon appears next to a software model that has not used any licenses. These software models appear at the bottom of the tree, and no software model results appear for them.

Use the navigation tree to:

-   Drill down to a product, software model, or license metric to view the calculation and compliance information from the latest reconciliation results.
-   Filter products, including collapsed items.
-   Expand and collapse tree links.

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

Indicates the unlicensed entities for this publisher, product, and software model. The following are some of the indicators:-   Unlicensed installs: refers to installations for which you have purchased some entitlements, but the rights owned are not sufficient to cover all the entities that require rights. You can perform remediation actions such as removing unlicensed installations or purchasing more rights.
-   Non-entitled product installs: indicates products with installations at ServiceNow that currently have no associated entitlements. You need to create entitlements for these products.
-   Installs requiring action: indicates an action that you need to perform to fix an issue for an installation, such as problems with CIs, entitlement, or software model setup.

After you select Installs requiring action, a list appears that groups installs by reason category. Select **Show all** to expand the list and view each install. Select a value in the Reason column for a more detailed explanation of the reason. For details on reconciliation results, such as product results and software model results, see [Software reconciliation results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/software-reconciliation-results.md).

**Note:** An installation may have more than one issue. Address each issue to fully resolve problems with an installation. The number shown on the progress indicator and the details when you drill down may not align. Make sure all issues are fixed for the installation.

-   Unlicensed subscriptions: indicates that there are insufficient entitlements to cover the purchased subscriptions on SaaS. You need to create the necessary entitlements.
-   Non-entitled product subscriptions: indicates subscriptions at ServiceNow that currently have no associated entitlements. You need to create entitlements for these subscriptions.
-   Subscriptions requiring action: Analyze subscription-related issues and perform the necessary corrective measures.
-   Unlicensed client access: refers to unlicensed CAL records because there are not enough rights on entitlements to cover the CAL records. You need to purchase more CAL licenses for the products.
-   Unlicensed options: refers to unlicensed Oracle Database options and management packs.

Select the number adjacent to each category for a more detailed explanation of each installation, including the reason and causes of its unlicensed status.

</td></tr><tr><td>

Progress indicators

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

 Requested Item \[sc\_req\_item\]

 Removal Candidate \[samp\_sw\_reclamation\_candidate\]

</td><td>

Indicates the compliance progress already made for this publisher, product, and software model. The progress indicators differ for each publisher. The following are some of the indicators:

-   Ignored installs: installations ignored from the reconciliation process.
-   Inactive installs: software installs that Software Asset Management Professional marked as inactive. These installs are not included in license calculations and do not require any action.
-   Ignored subscriptions: subscriptions that Software Asset Management Professional marked as inactive. These subscriptions are not included in license calculations and do not require any action.
-   Removal candidates: details of all removal candidates created for reasons such as low usage and unlicensed install removal.
-   Health issues: all health check issues for your Software Asset Management configurations. Select a health check issue to address and fix the error. If there are no health issues, the Health issue indicator does not appear.

 Select the number adjacent to each category for a more detailed explanation of each installation.

</td></tr></tbody>
</table>## Related lists

The Publisher details page includes the following related lists for a publisher and its products:

|Related list|Purpose|
|------------|-------|
|Product Results|A product result record for a licensable product is generated after reconciliation, even if the product has no software models defined.|
|Software Model Results|A software model result record is generated for each software model related to a product. It is created only when a software model or entitlement exists for the product. To generate software model results for all software models, with or without entitlements, set the **com.snc.samp.unlicensed\_smr\_creation** property to true. By default, this property is set to false.|
|License Metric Results|A license metric result record is generated for each license metric associated with a software model.|
|Removal candidates|A list of removal candidates.|
|Entitlements|The entitlements associated with the publisher.|
|Product install analysis|The license consumption analysis for the publisher's products. Open a record to view a hierarchical node map that shows how the installations of a specific product are being licensed. This analysis is available at the publisher level, not at the individual product level. For more details, see [View license usage for your installations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/view-install-usage.md).|

To prevent clutter on the Publisher details page, software model results appear only for software models that have entitlements. Software models without entitlements appear at the product level in the product results.

For more details on the related lists, refer to [License usage publisher fields in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/workbench-publisherfields-workspace.md).

**Related topics**  


[License usage view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/sam-workspace-workbench.md)

[License operations view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/operations-workspace.md)

[Software license metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/c_SAMLicenseMetrics.md)

[Software installation optimization and removal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/c_SAMOptimization.md)

[Allocation management on Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/allocation-management-sam.md)

[Reclaim software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/reclaiming-software-sam.md)

