---
title: Combined Continuous Authorization and Monitoring release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for Continuous Authorization and Monitoring from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-continuousauthorizationandmonitoring-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Continuous Authorization and Monitoring release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for Continuous Authorization and Monitoring from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Continuous Authorization and Monitoring release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Continuous Authorization and Monitoring to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Washington DC

</td><td>

-   **[Managing controls at a granular level](https://www.servicenow.com/docs/access?context=cam-control-req-sca&family=washingtondc&ft:locale=en-US)**

Configure a control requirement at the control objective level based on the NIST 800-53 Risk Management Framework to assess the control at a granular level. You can also take attestations at the requirement level while the control moves to the Attest state in the workflow. You can monitor and track the control effectively and clearly identify specific requirements that are non-compliant, which leads to the control being non-compliant.

-   **[Set up baseline controls to generate controls and implement requirements](https://www.servicenow.com/docs/access?context=cam-hybrid-controls&family=washingtondc&ft:locale=en-US)**

Create a control that is implemented as an inherited control in part and as a system-specific control in part, which helps to adopt partial requirements from a common control provider. You can also inherit one or more requirements provided by a common control provider.

-   **[Ability to have assessment procedures based on NIST 800-53A](https://www.servicenow.com/docs/access?context=cam-assessment-objectives&family=washingtondc&ft:locale=en-US)**

Determine the control’s effectiveness based on the individual assessment procedure’s effectiveness. You can tailor the assessment procedures in test templates and mark them as Effective, Ineffective, or Not applicable.

-   **[New related lists in the CAM view of Control objective and Control forms](https://www.servicenow.com/docs/access?context=cam-cr-control-form&family=washingtondc&ft:locale=en-US)**

Use the CAM view of the Control objective form that has all the control objective requirements from the NIST 800-53 revision 5. Similarly, the CAM view of the Control form has all the requirements generated for the control in the control requirements related list.


</td></tr><tr><td>

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

Washington DC

</td><td>

-   **[Analytics and Reporting Solutions for CAM in Next Experience UI Framework](https://www.servicenow.com/docs/access?context=cam-pa-next-exp-dashboards&family=washingtondc&ft:locale=en-US)**

Starting with version 18.1.0 of Continuous Authorization and Monitoring application, the Analytics and Reporting solutions for CAM such as the CAM Overview, AO Overview, and SCA Overview dashboards are available in the Next Experience UI Framework.

-   **[Generating assessment procedure plans for a test plan](https://www.servicenow.com/docs/access?context=cam-assess-controls-assess-obj&family=washingtondc&ft:locale=en-US)**

The **Control test** section of the Test template form is updated with additional fields such as Examine, Interview, and Test that draw control test guidelines from NIST.

-   **[Determine control effectiveness of a control test](https://www.servicenow.com/docs/access?context=cam-control-effectiveness-control-test&family=washingtondc&ft:locale=en-US)**

Additional new fields such as Examine, Interview, and Test are added to the Test plan and Control test forms to test the control effectiveness.

-   **[Document implementation statement for a control](https://www.servicenow.com/docs/access?context=cam-cr-control-form&family=washingtondc&ft:locale=en-US)**

The Control form now has a new field called Implementation statement, which is required before moving the control to the Assess state.

-   **[Discussion field in the Control objective and Control forms](https://www.servicenow.com/docs/access?context=cam-cr-control-form&family=washingtondc&ft:locale=en-US)**

Based on the 800-53 controls, the Discussion content provided by NIST for each control is shipped by the base system at the control objective level, which is also updated in the Control form when the control is created.


</td></tr><tr><td>

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Washington DC

</td><td>

Install Continuous Authorization and Monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Washington DC

</td><td>

-   Enable management of controls at a granular level that is at the control requirements level, which are shipped by the base system for controls belonging to NIST 800-53 revision 5.
-   Define requirements at a control objective level that enables the breakdown of the control and create control requirements automatically, which can also be attested individually.
-   Create hybrid controls by inheriting control requirements partially and self-implementing the rest of the requirements.
-   Enable testing of the control based on the assessment procedures as defined by NIST 800-53A.

 See [Understanding Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=what_is_cam&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

