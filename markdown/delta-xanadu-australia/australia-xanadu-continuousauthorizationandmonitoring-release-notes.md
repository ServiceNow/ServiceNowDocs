---
title: Combined Continuous Authorization and Monitoring release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Continuous Authorization and Monitoring from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-continuousauthorizationandmonitoring-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined Continuous Authorization and Monitoring release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Continuous Authorization and Monitoring from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Continuous Authorization and Monitoring release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Continuous Authorization and Monitoring to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Continuous Authorization and Monitoring.

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


</td></tr><tr><td>

Zurich

</td><td>

-   **[\[Placeholder link text to key cam-workflow-configurator\]](https://www.servicenow.com/docs/access?context=cam-workflow-configurator&family=zurich&ft:locale=en-US)**

Streamline governance, risk, and compliance processes with the CAM Workflow Configuration. This feature allows administrators to:

    -   Create and manage multiple workflows within a package.
    -   Define GRC State Models for custom workflows.
    -   Configure and version workflows.
    -   Evaluate workflow version impacts to retrieve baseline controls.
    -   Set up workflow-specific approval configurations.
    -   Perform risk assessments across CAM objects.
    -   Migrate the NIST RMF flow to workflow configuration for improved standardization.
-   **[\[Placeholder link text to key add-child-boundary\]](https://www.servicenow.com/docs/access?context=add-child-boundary&family=zurich&ft:locale=en-US)**

Introducing a new Child Boundaries list that enables a one-to-many boundary hierarchy, allowing you to create relationships between boundaries. This hierarchy is visualized in both the sidebar and diagram view, showing one parent boundary with multiple child boundaries. OSCAL export and import now include the parent boundary relationship if present.

-   **Dynamic Boundary Filters [Dynamic boundary filters](https://www.servicenow.com/docs/access?context=create-boundary-filter&family=zurich&ft:locale=en-US)**

Select the **Dynamic Filter** option in boundary filters to update system elements according to filter conditions. When disabled, the system elements remain unchanged. This update enhances the flexibility of boundary filter management.

-   **[Boundary operational status automation](https://www.servicenow.com/docs/access?context=cam-form-authorization-boundary&family=zurich&ft:locale=en-US)**

Linking boundary operational status to the package life cycle ensures seamless integration. Key changes include:

    -   Automatic update of boundary status to Operational when a package moves to the Monitor state.
    -   Transition of Boundary status to Reauthorize as the Package Authorization date approaches. This update maintains synchronization between package and boundary states, enhancing overall system coherence.
-   **[\[Placeholder link text to key export-oscal-files-from-authorization-package\]](https://www.servicenow.com/docs/access?context=export-oscal-files-from-authorization-package&family=zurich&ft:locale=en-US)**

Generating and downloading OSCAL SSP and POA&amp;M files is supported directly from within a authorization package. The supported file types include:

    -   Catalog
    -   Overlay Catalog
    -   Profile
    -   SSP
    -   POA&amp;M
-   **[OSCAL import enhancements](https://www.servicenow.com/docs/access?context=import-oscal&family=zurich&ft:locale=en-US)**

Enhancing the OSCAL import experience, the OSCAL import playbook now allows you to:

    -   Import individual POA&amp;M JSON files.
    -   **User Mapping**: Automatically map users to existing ServiceNow users based on exact name matches, with the option to manually adjust mappings.
    -   **Group Mapping**: Automatically map groups to existing ServiceNow groups based on exact name matches, with the option to manually adjust mappings.
    -   **Roles and Responsibilities**: Populate relevant package fields with roles and responsibilities.
-   **[Overlay enhancement](https://www.servicenow.com/docs/access?context=prepare-auth-pkg&family=zurich&ft:locale=en-US)**

Apply policies as an overlay in an authorization package to determine how the control objectives in the policy impact the baseline. This can be done in the following ways:

    -   Addition: Create control objectives to address specific requirements not covered in the baseline.
    -   Subtraction: Move existing control objectives to **Not Applicable**.
    -   Customization: Create, move existing control objectives to not applicable, or skip control objectives.
-   **[OSCAL enhancements](https://www.servicenow.com/docs/access?context=oscal-cam-ws&family=zurich&ft:locale=en-US)**

Use the OSCAL import playbook to follow a user-friendly, step-by-step approach for importing OSCAL models. Using the playbook, you can:

    -   Add multiple Catalog overlay files.
    -   Preview OSCAL data before importing them to confirm accuracy. You can preview the following:
        -   Authorization boundary
        -   Authorization package
        -   System elements
        -   Information types
        -   Baseline controls
        -   Inherited controls
        -   Hybrid controls
        -   Not applicable controls
        -   Policies
        -   Control objectives
        -   Control objectives requirements
    -   Skipped objects in the preview, such as control objectives, policies, authorization boundaries and packages can be individually overridden.

</td></tr><tr><td>

Australia

</td><td>

-   **[Support for exporting and importing the OSCAL Assessment Results \(AR\) model](https://www.servicenow.com/docs/access?context=import-oscal-assessment-plan&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, Continuous Authorization and Monitoring supports import and export of OSCAL data for Assessment Results \(AR\) format.

-   **[Skip attestations configuration for controls within a package](https://www.servicenow.com/docs/access?context=categorize&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, skip the attestation stage at the package level and move controls directly from Draft to Review without completing the attestation workflow.

-   **[Control tailoring request enhancements](https://www.servicenow.com/docs/access?context=request-control-tailoring&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, control tailoring requests support changes to overlay controls. You can add new overlay controls or modify existing ones within a control tailoring request.

-   **[OSCAL export and import enhancements](https://www.servicenow.com/docs/access?context=oscal-cam-ws&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, OSCAL import and export support additional details for various records, including status, frequency, weighting, implementation statement, control tailoring requests, overlays, and activities.

-   **[Support for exporting and importing the OSCAL Assessment Plan \(AP\) model](https://www.servicenow.com/docs/access?context=oscal-cam-ws&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, Continuous Authorization and Monitoring supports import and export of OSCAL data for Assessment Plan \(AP\) format.

-   **[Request control tailoring](https://www.servicenow.com/docs/access?context=request-control-tailoring&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, make incremental changes to control sets while preserving the state of unchanged controls without having to reset the entire package life cycle. Supported modifications include adding new controls, marking controls as not applicable, changing control allocation \(baseline to inherited or hybrid\), and modifying inheritance configurations.

-   **[Inherit from multiple providers](https://www.servicenow.com/docs/access?context=inherit-from-multiple-providers&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, Controls can inherit individual control requirements from multiple Common Control Providers \(CCPs\) across different authorization packages. Previously, inheritance was limited to a single provider per control, which required creating duplicate inherited controls when requirements came from different sources.

-   **[Control grid view](https://www.servicenow.com/docs/access?context=view-controls-in-grid-view&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, edit implementation statements and attestation respondents directly in a hierarchical data grid through the Controls tab in an authorization package.

-   **[Control tests grid view in Engagements](https://www.servicenow.com/docs/access?context=view-control-tests-in-grid-view&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, toggle between traditional related list and hierarchical data grid on the Control tests tab. Changes to assessment procedure effectiveness automatically cascade to parent control test effectiveness.

Package detail forms now use a structured vertical layout instead of the previous horizontal tab arrangement.

-   **[CAM workflow configuration enhancements](https://www.servicenow.com/docs/access?context=cam-workflow-configurator&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, configure control button visibility, UI page access, and related list actions across different workflow steps. Previously, related list actions \(such as add or remove buttons for information types or baseline control actions\) required manual scripting to support custom workflows.

The following new state model attributes have been introduced:

    -   Required Authorization Documents Page
    -   Required Overlay Page
    -   Required Information Type Actions
    -   Required Baseline Actions
    -   Required Overlay Actions
    -   Request Control Tailoring
    -   Generate OSCAL AP
    -   Generate OSCAL AR

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Continuous Authorization and Monitoring features.

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


</td></tr><tr><td>

Zurich

</td><td>

-   **[New Authorization Documents tab for ATO reports](https://www.servicenow.com/docs/access?context=prepare-auth-pkg&family=zurich&ft:locale=en-US)**

Access all Authority to Operate \(ATO\) artifacts reports from the new **Authorization Documents** tab available in the Authorization Package.


-   **[New CAM System Properties page for administrators](https://www.servicenow.com/docs/access?context=cam-components-installed&family=zurich&ft:locale=en-US)**

Access the new CAM **System Properties** page to enable administrators to configure various system properties.

-   **[Track package progress with the Ageing of Packages widget](https://www.servicenow.com/docs/access?context=cam-ws-home-page&family=zurich&ft:locale=en-US)**

View the duration that a package stayed in each step, like Prepare, Categorize, Select, Implement, Assess, Authorize, and Monitor, using the Ageing of Packages widget.

-   **[Set Next Engagement Date for Automated Audit Generation](https://www.servicenow.com/docs/access?context=prepare-auth-pkg&family=zurich&ft:locale=en-US)**

Enter the **Next engagement date** to automatically generate the audit engagement on the specified date.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Continuous Authorization and Monitoring features or functionality were removed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Continuous Authorization and Monitoring features or functionality were deprecated.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Zurich

</td><td>

Install CAM by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Continuous Authorization and Monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Zurich

</td><td>

-   Simplify Governance, Risk, and Compliance processes by enabling admins to create, version, and manage custom workflows, define state models, configure approvals, assess risks, and standardize with NIST RMF migration.
-   The CAM workspace homepage now features card-based containers with headers, sidebars, and overviews for a more organized and modern experience.
-   Authorization boundaries and package layout are now vertical. New **Boundary Type** and **Classification** records are included in OSCAL export file.
-   Add a **Child Boundaries** to create one-to-many relationships between boundaries. You can view the parent-child boundary mapping of a authorization boundary in the **Highlighted details** panel under the **Boundary hierarchy** section.
-   Select the **Dynamic Filter** option to make boundary filters update system elements automatically based on conditions, enhancing filter flexibility.
-   Boundary operational status now automatically syncs with the package life cycle.
-   Generate and download Open Security Controls Assessment Language \(OSCAL\) System Security Plans \(SSP\) and Plan of Action and Milestones \(POA&amp;M\) files directly from within a package.
-   The OSCAL import playbook now supports importing single POA&amp;M JSON files, automatically maps users and groups by exact names to ServiceNow, and populates package roles and responsibilities for a streamlined import experience.
-   CAM overlays new capability has been introduced to perform various operations like addition, subtraction, custom while applying a policy overlay to an authorization package.
-   Import OSCAL models using a user-friendly playbook that guides you through preview and customization steps.

 See [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Import and export OSCAL data for Assessment Plan \(AP\) and Assessment Results \(AR\) formats to streamline compliance reporting.
-   Skip the attestation stage for all controls in a package and move controls directly to the Monitor step to accelerate package progression.
-   Populate additional control fields when importing and exporting OSCAL data for SSP, AP, and AR formats to capture richer compliance details.
-   Raise control tailoring requests to make incremental changes to control sets in authorized packages without resetting the entire package life cycle.

 See [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

