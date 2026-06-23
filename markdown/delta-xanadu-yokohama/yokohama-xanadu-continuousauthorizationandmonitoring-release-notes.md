---
title: Combined Continuous Authorization and Monitoring release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Continuous Authorization and Monitoring from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-continuousauthorizationandmonitoring-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Continuous Authorization and Monitoring release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Continuous Authorization and Monitoring from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Continuous Authorization and Monitoring release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Continuous Authorization and Monitoring to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Continuous Authorization and Monitoring.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[CAM Workspace](https://www.servicenow.com/docs/access?context=cam-ws-home-page&family=xanadu&ft:locale=en-US)**

Use the CAM Workspace for an end-to-end user experience. The Home page, overview pages of authorization boundary and authorization package, unified tasks page, and the dashboards help you capture information and give you a better insight into the data that aids in decision making.

CAM Workspace includes exclusive features with which you can:

    -   Add related control objectives.
    -   View controls by family for a control objective and report based on families for NIST 800-53.
    -   Add attachments to assessment procedures and document notes.
    -   View all Plan of Actions and Milestones \(POA&amp;M\) in a single pane.
-   **[CAM supports the OSCAL format to export control-related information](https://www.servicenow.com/docs/access?context=oscal-support-cam&family=xanadu&ft:locale=en-US)**

Export SSP files in the OSCAL format based on various models such as SSP, Profile, Catalog, and Catalog overlay. The generated report is compatible to share the information with other systems. CAM supports the National Institute of Standards and Technology \(NIST\) recommended OSCAL format to provide control-based information in machine-readable formats.

-   **[CAM ATO artifacts](https://www.servicenow.com/docs/access?context=generate-ato-artifacts-cam-ws&family=xanadu&ft:locale=en-US)**

Generate ATO artifacts from an authorization package in Microsoft Word format for the following reports:

    -   SSP
    -   Security Assessment Report \(SAR\)
    -   POA&amp;M
-   **[Enhancements in CAM user roles](https://www.servicenow.com/docs/access?context=assign-cam-roles&family=xanadu&ft:locale=en-US)**

The existing user roles in CAM application have been enhanced with the following privileges:

    -   Use the Information Owner \(sn\_irm\_cont\_auth.information\_owner\) role to view and update the information types of an authorization package.
    -   Use the Audit reader \(sn\_audit.reader\) lite role to view audit-related entities, such as engagements.
    -   Create and manage issues as a system user.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[OSCAL Import landing page](https://www.servicenow.com/docs/access?context=import-oscal&family=yokohama&ft:locale=en-US)**

Import files for catalog and SSP models on the new OSCAL Import landing page. Once the import process is initiated, you can check the status under the Import status section.

-   **[OSCAL Export button](https://www.servicenow.com/docs/access?context=export-catalog-cam-ws&family=yokohama&ft:locale=en-US)**

Export selected control objectives in the OSCAL format with the new **OSCAL Export** button while in the control objectives list view.

-   **[ATO artifacts in Microsoft Word](https://www.servicenow.com/docs/access?context=generate-ato-artifacts-cam-ws&family=yokohama&ft:locale=en-US)**

Generate ATO artifacts from an authorization package in the Microsoft Word format. In CAM Workspace, you can use the **Generate SSP** drop-down list in a selected authorization package to generate the following reports:

    -   Security Assessment Plan \(SAP\)
    -   Authorization to Operate \(ATO\) Letter
    -   Executive Summary
This enhancement verifies that all ATO artifacts are formatted consistently and can be shared and reviewed.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Continuous Authorization and Monitoring features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Role changes for Continuous Authorization and Monitoring Workspace users](https://www.servicenow.com/docs/access?context=cam-roles-list&family=xanadu&ft:locale=en-US)**

Reader \(sn\_irm\_cont\_auth.reader\), Authorization Official \(sn\_irm\_cont\_auth.authorization\_official\), and Executive Reader \(sn\_irm\_cont\_auth.executive\_read\) can now access Continuous Authorization and Monitoring Workspace.

-   **[OSCAL Catalog model export](https://www.servicenow.com/docs/access?context=oscal-support-cam&family=xanadu&ft:locale=en-US)**

In exporting the control-related information as part of the Catalog model, the child control objectives of a control objective are mapped to the Control field. Furthermore, related control objectives of the control objective are mapped to the Links field.

-   **[Enhancements in CAM Workspace](https://www.servicenow.com/docs/access?context=cam-ws-home-page&family=xanadu&ft:locale=en-US)**

The following enhancements have been made in CAM Workspace:

    -   New pop-ups with additional capabilities are added to the hybrid controls creation.
    -   POA&amp;Ms include all authorization package issues.
    -   The **Family** field and **Family ID** field are added to the Control objective page.
    -   The **Notes** field and **Attachment** field are added to the Assessment procedure page.
    -   The **360° View** button is configured in all pages of CAM Workspace.
-   **[CAM user role changes](https://www.servicenow.com/docs/access?context=assign-cam-roles&family=xanadu&ft:locale=en-US)**

Defining roles and assigning privileges and permissions for approvals is critical to ensure security in the CAM application. The user role changes are:

    -   The Information Owner \(sn\_irm\_cont\_auth.information\_owner\) role can also update information types of an authorization package, and the role also contains the Audit user \(sn\_audit.user\) role in addition to the Reader \(sn\_irm\_cont\_auth.reader\) role.
    -   The Information System Security Manager \(sn\_irm\_cont\_auth.info\_system\_sec\_manager\) role can update the authorization package, and the role contains the Compliance user \(sn\_compliance.user\) and Reader \(sn\_irm\_cont\_auth.reader\) roles.
    -   The Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\) role can update the authorization package.
    -   The Reader \(sn\_irm\_cont\_auth.reader\) role contains the Audit reader \(sn\_audit.reader\) role.
    -   The System User \(sn\_irm\_cont\_auth.system\_user\) role contains the Audit user \(sn\_audit.user\) role.
    -   The System Owner \(sn\_irm\_cont\_auth.system\_owner\) role also contains the Audit user \(sn\_audit.user\) and Compliance user \(sn\_compliance.user\) roles.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Generate the OSCAL SSP model of an authorization package](https://www.servicenow.com/docs/access?context=generate-oscal-models&family=yokohama&ft:locale=en-US)**

Export the SSP model of an authorization package in the OSCAL format. The exported report contains only the control objectives linked to the authorization package and their additional information, such as inherited controls and the hierarchy of the control objectives.

-   **[Generate ATO artifacts in Microsoft Word and HTML templates](https://www.servicenow.com/docs/access?context=generate-ato-artifacts-cam-ws&family=yokohama&ft:locale=en-US)**

Use the Document designer plugin \(com.sn\_grc\_doc\_design\) to create report templates in Microsoft Word. A new property module has been introduced to select the template type as a Microsoft Word template in addition to an HTML template.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Continuous Authorization and Monitoring features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   The Authorization Official \(AO\) \(sn\_irm\_cont\_auth.authorization\_official\) role no longer contains the sn\_audit.user and sn\_compliance.user roles. The AO role can only read and approve an authorization package.
-   The Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\) role no longer contains the sn\_audit.user role.
-   The Reader \(sn\_irm\_cont\_auth.reader\) role no longer contains the sn\_audit.user role.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Continuous Authorization and Monitoring features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Continuous Authorization and Monitoring.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Continuous Authorization and Monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install CAM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Continuous Authorization and Monitoring we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Continuous Authorization and Monitoring we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Continuous Authorization and Monitoring, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Continuous Authorization and Monitoring we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Continuous Authorization and Monitoring we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Use the added features in the CAM Workspace to help streamline your work and have an efficient end-to-end user experience.
-   Export System Security Plan \(SSP\) files in the OSCAL format, which includes models like Catalog, Profile, and SSP.
-   Use the lite roles introduced in CAM for lighter business operations.
-   Group similar controls into a family-related and club-related to help identify and understand the controls.

 See [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Import catalog and System Security Plan \(SSP\) models with the new CAM Open Security Controls Assessment Language \(OSCAL\) import landing page.
-   Export and import SSP models and catalog models in the OSCAL format.
-   Export control objectives as a catalog in the OSCAL format.
-   Generate additional reports in Microsoft Word format, such as a Security Assessment Plan \(SAP\), Authorization to Operate \(ATO\) Letter, and Executive Summary.
-   Generate reports based on a Microsoft Word template.

 See [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

