---
title: Continuous Authorization and Monitoring release notes
description: The ServiceNow Continuous Authorization and Monitoring application provides a standardized approach to defining an authorization package and walking through the seven stages of the National Institute of Standards and Technology \(NIST\) Risk Management Framework \(RMF\). CAM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Continuous Authorization and Monitoring release notes

The ServiceNow® Continuous Authorization and Monitoring application provides a standardized approach to defining an authorization package and walking through the seven stages of the National Institute of Standards and Technology \(NIST\) Risk Management Framework \(RMF\). CAM was enhanced and updated in the Zurich release.

## CAM highlights for the Zurich release

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

See [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** CAM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   ****

    Streamline governance, risk, and compliance processes with the CAM Workflow Configuration. This feature allows administrators to:

    -   Create and manage multiple workflows within a package.
    -   Define GRC State Models for custom workflows.
    -   Configure and version workflows.
    -   Evaluate workflow version impacts to retrieve baseline controls.
    -   Set up workflow-specific approval configurations.
    -   Perform risk assessments across CAM objects.
    -   Migrate the NIST RMF flow to workflow configuration for improved standardization.
-   ****

    Introducing a new Child Boundaries list that enables a one-to-many boundary hierarchy, allowing you to create relationships between boundaries. This hierarchy is visualized in both the sidebar and diagram view, showing one parent boundary with multiple child boundaries. OSCAL export and import now include the parent boundary relationship if present.

-   **Dynamic Boundary Filters Dynamic boundary filters**

    Select the **Dynamic Filter** option in boundary filters to update system elements according to filter conditions. When disabled, the system elements remain unchanged. This update enhances the flexibility of boundary filter management.

-   **Boundary operational status automation**

    Linking boundary operational status to the package life cycle ensures seamless integration. Key changes include:

    -   Automatic update of boundary status to Operational when a package moves to the Monitor state.
    -   Transition of Boundary status to Reauthorize as the Package Authorization date approaches. This update maintains synchronization between package and boundary states, enhancing overall system coherence.
-   ****

    Generating and downloading OSCAL SSP and POA&amp;M files is supported directly from within a authorization package. The supported file types include:

    -   Catalog
    -   Overlay Catalog
    -   Profile
    -   SSP
    -   POA&amp;M
-   **OSCAL import enhancements**

    Enhancing the OSCAL import experience, the OSCAL import playbook now allows you to:

    -   Import individual POA&amp;M JSON files.
    -   **User Mapping**: Automatically map users to existing ServiceNow users based on exact name matches, with the option to manually adjust mappings.
    -   **Group Mapping**: Automatically map groups to existing ServiceNow groups based on exact name matches, with the option to manually adjust mappings.
    -   **Roles and Responsibilities**: Populate relevant package fields with roles and responsibilities.
-   **[Overlay enhancement](https://www.servicenow.com/docs/access?context=prepare-auth-pkg&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Apply policies as an overlay in an authorization package to determine how the control objectives in the policy impact the baseline. This can be done in the following ways:

    -   Addition: Create control objectives to address specific requirements not covered in the baseline.
    -   Subtraction: Move existing control objectives to **Not Applicable**.
    -   Customization: Create, move existing control objectives to not applicable, or skip control objectives.
-   **[OSCAL enhancements](https://www.servicenow.com/docs/access?context=oscal-cam-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

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

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[New Authorization Documents tab for ATO reports](https://www.servicenow.com/docs/access?context=prepare-auth-pkg&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Access all Authority to Operate \(ATO\) artifacts reports from the new **Authorization Documents** tab available in the Authorization Package.


-   **[New CAM System Properties page for administrators](https://www.servicenow.com/docs/access?context=cam-components-installed&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Access the new CAM **System Properties** page to enable administrators to configure various system properties.

-   **[Track package progress with the Ageing of Packages widget](https://www.servicenow.com/docs/access?context=cam-ws-home-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    View the duration that a package stayed in each step, like Prepare, Categorize, Select, Implement, Assess, Authorize, and Monitor, using the Ageing of Packages widget.

-   **[Set Next Engagement Date for Automated Audit Generation](https://www.servicenow.com/docs/access?context=prepare-auth-pkg&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Enter the **Next engagement date** to automatically generate the audit engagement on the specified date.


## Activation information

Install CAM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

