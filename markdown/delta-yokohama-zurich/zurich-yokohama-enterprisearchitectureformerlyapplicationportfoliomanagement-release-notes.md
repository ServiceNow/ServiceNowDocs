---
title: Combined Enterprise Architecture \(formerly Application Portfolio Management\) release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Enterprise Architecture \(formerly Application Portfolio Management\) from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-enterprisearchitectureformerlyapplicationportfoliomanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Enterprise Architecture \(formerly Application Portfolio Management\) release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Enterprise Architecture \(formerly Application Portfolio Management\) from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Enterprise Architecture \(formerly Application Portfolio Management\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Enterprise Architecture \(formerly Application Portfolio Management\) to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Enterprise Architecture \(formerly Application Portfolio Management\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Yokohama Patch 6 [Application rationalization page enhancements](https://servicenow-staging.fluidtopics.net/access?context=eaw-rationalize-business-applications&family=yokohama&ft:locale=en-US)**
    -   Apply the fiscal period filter to filter and view business applications for a specific fiscal period.
    -   Apply the application rationalization filters to filter and view specific business applications on the bubble chart or list view page. An indicator is displayed on top of the filter icon to show the number of filters currently applied.
    -   View the business application technical debt indicator score on the application rationalization list view page. On the application rationalization bubble chart view page, you can use the TRM technical debt indicator to form the bubble size based on the indicator score.
    -   Export the list view of application rationalization data to Excel or CSV file format. You can use the data to obtain insights, share with stakeholders, and prepare for analysis.
    -   Business applications with Retired or End of Life lifecycle stage aren’t displayed on the Application Rationalization bubble chart page.
-   **[Enterprise Modeling and Visualization in the EA Workspace](https://servicenow-staging.fluidtopics.net/access?context=eaw-modeling&family=yokohama&ft:locale=en-US)**
    -   Create diagrams for business process maps using the specific shapes related to the business processes.
    -   Search shapes within the shape libraries.
    -   Reorganize the order of shapes in a shape library according to your requirement.
    -   Show or hide shapes in different diagram types.
    -   General shapes can be rotated.
    -   Enhanced the overall appearance of the diagram by hiding the connector ports and displaying them only when hovering over the shapes.
    -   Open the Enterprise Modeling and Visualization diagrams from the following sections:
        -   From the Architectural Artifacts related list of a business application, business capability, or a business process record.
        -   From the My approvals tab of the Needs Attention section on the EA Workspace home page.
        -   From the Architectural Artifacts section of the Portfolio page.
    -   Added support for all ArchiMate shapes.
    -   Model Value stream diagrams.
    -   Create diagram actions for newly added custom shapes that can be used in Enterprise Modeling and Visualization to create diagrams.
    -   Add custom shapes to use in the Enterprise Modeling and Visualization.
    -   Create your own modeling diagrams using the Blank diagram option.
-   **[Business application related list enhancements](https://servicenow-staging.fluidtopics.net/access?context=eaw-app-portfolio&family=yokohama&ft:locale=en-US)**

In the **Architectural Artifacts** tab of the business application related list, selecting the **New** button displays a modal to create an architectural artifact.

-   **[Architectural Decision Records \(ADR\) enhancements](https://servicenow-staging.fluidtopics.net/access?context=eaw-managing-arch-decision-records&family=yokohama&ft:locale=en-US)**
    -   Create artifact type Architectural Decision Records \(ADR\) in one step.
    -   Create and add multiple pages to the Architectural Decision Records \(ADR\) from the Artifact content tab.
    -   In the Architectural Decision Records \(ADR\) page, you can tag the following:
        -   Tag a user
        -   Tag a record
            -   Architectural artifact
            -   Business application
            -   Business capability
            -   Business process
            -   Digital integration \(requires the digital integration plugin\)
            -   Digital interface \(requires the digital integration plugin\)
            -   Information object
            -   TRM product \(requires the TRM plugin\)
            -   Value stream \(requires the value stream plugin\)
    -   Request approval workflow for Architectural Decision Records \(ADR\).
    -   The version drop-down list is added to the Architectural Decision Records \(ADR\) page header. Select a version from the drop-down list to open the specific ADR version.
-   **[Data Certification changes](https://servicenow-staging.fluidtopics.net/access?context=eaw-config-cert-schedules&family=yokohama&ft:locale=en-US)**

In the Enterprise Architecture Workspace, the certifications data is saved to and fetched from the CMDB Data Management Task Control \(cmdb\_data\_management\_task\) table.

If your certification data is still fetched from the Certification Schedules \(cert\_schedule\) table, you might consider migrating your certification policies to the CMDB Data Management Task Control \(cmdb\_data\_management\_task\) table. For more information, see [Convert legacy certification schedules into Data Manager Certification policies](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/convert-data-cert-definitions.html)and[Publish a draft Data Manager policy in CMDB Workspace](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/data-manager-publish-draft-policy.html%22%20HYPERLINK%20%22https:/www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/data-manager-publish-draft-policy.html)

-   **[Regenerate indicator scores in Enterprise Architecture Workspace](https://servicenow-staging.fluidtopics.net/access?context=eaw-regenerate-indicator-score&family=yokohama&ft:locale=en-US)**

Generate a score for application and capability indicators for a particular period. Also, generate scores for an application scoring profile and capability scoring profile, to calculate scores for all indicators attached to that particular scoring profile.

-   **[Business stakeholder role for Enterprise Architecture Workspace](https://servicenow-staging.fluidtopics.net/access?context=eaw-business-stakeholder-role&family=yokohama&ft:locale=en-US)**

Read-only access to the  Enterprise Architecture Workspace is added to the business stakeholder role \(sn\_apm.apm\_read\).

-   **[TRM technical debt form](https://servicenow-staging.fluidtopics.net/access?context=eaw-trm-technical-debt-form&family=yokohama&ft:locale=en-US)**

The **TPM Discovered Technologies and Lifecycles** scheduled job fetches the server details for the TRM products.

-   **[Technology portfolio management \(TPM\) enhancements](https://servicenow-staging.fluidtopics.net/access?context=eaw-tpm&family=yokohama&ft:locale=en-US)**
    -   Added a restart button on the TPM Logs page to restart the Populate TPM Discovered Technologies and Lifecycles scheduled job, in case the job is stuck and doesn’t refresh the log data for more than an hour. For more information, see [View TPM logs](https://servicenow-staging.fluidtopics.net/access?context=eaw-view-tpm-logs&family=yokohama&ft:locale=en-US) and [Restart scheduled job](https://servicenow-staging.fluidtopics.net/access?context=eaw-restart-tpm-scheduled-job&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Enterprise Architecture \(formerly Application Portfolio Management\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Enterprise Architecture \(formerly Application Portfolio Management\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Enterprise Architecture \(formerly Application Portfolio Management\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Enterprise Architecture \(formerly Application Portfolio Management\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Enterprise Architecture \(formerly Application Portfolio Management\) is available with activation of the Enterprise Architecture \(com.snc.apm\), which requires a separate subscription. For details, see [Enterprise Architecture](https://servicenow-staging.fluidtopics.net/access?context=application-portfolio-management-landing-page&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Enterprise Architecture \(formerly Application Portfolio Management\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Enterprise Architecture \(formerly Application Portfolio Management\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Enterprise Architecture \(formerly Application Portfolio Management\), such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Enterprise Architecture \(formerly Application Portfolio Management\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Enterprise Architecture \(formerly Application Portfolio Management\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Yokohama Patch 6

-   Select a fiscal period on the Application Rationalization pages using the new fiscal period filter option. The fiscal period filter enables you to view application rationalization data for the selected fiscal period.
-   Evaluate the technical debt score for business applications using the Technology Reference Model \(TRM\) technical debt indicator. This helps you to identify high-risk business applications and enables you to prioritize modernization and rationalization.
-   Generate business process modeling diagrams and model the future state of the business processes using Enterprise Modeling and Visualization.
-   Associate business capabilities to a business application from the business application related list.
-   View the past due certification tasks for your business applications from the Application Portfolio tab of the Insights section.
-   Generate scores for indicators and scoring profiles in the Enterprise Architecture Workspace.
-   Read-only access to the  Enterprise Architecture Workspace is added to the business stakeholder role \(sn\_apm.apm\_read\).

 Yokohama General Availability

-   Generate business process modeling diagrams and model the future state of the business processes using Enterprise Modeling and Visualization.
-   Associate business capabilities to a business application from the business application related list.
-   View the past due certification tasks for your business applications from the Application Portfolio tab of the Insights section.
-   Generate scores for indicators and scoring profiles in the Enterprise Architecture Workspace.
-   Read-only access to the  Enterprise Architecture Workspace is added to the business stakeholder role \(sn\_apm.apm\_read\).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

