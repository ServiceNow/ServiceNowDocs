---
title: Continuous Authorization and Monitoring release notes
description: The ServiceNow Continuous Authorization and Monitoring application provides a standardized approach to defining an authorization package and walking through the seven stages of the NIST Risk Management Framework. Continuous Authorization and Monitoring was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Continuous Authorization and Monitoring release notes

The ServiceNow® Continuous Authorization and Monitoring application provides a standardized approach to defining an authorization package and walking through the seven stages of the NIST Risk Management Framework. Continuous Authorization and Monitoring was enhanced and updated in the Australia release.

## Continuous Authorization and Monitoring highlights for the Australia release

-   Automatically generate engagements by importing Assessment Plan \(AP\) files. Additionally, export engagement data in OSCAL format from the current instance.
-   Make incremental changes to control sets in authorized packages without having to reset the entire package life cycle.
-   Inherit individual requirements for baseline controls from multiple Common Control Providers \(CCPs\) across different authorization packages.
-   View and edit Controls and Engagements sections in Authorization Packages in a hierarchical grid.
-   Control visibility of UI elements across different workflow steps through state model attributes.

See [Continuous Authorization and Monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/continuous-risk-monitoring/grc-cam-landing-page.md) for more information.

**Important:** Continuous Authorization and Monitoring is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[OSCAL Assessment Plan export and import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-assessment-plan-import-export.md)**

    After upgrading to version 22.0.2, Continuous Authorization and Monitoring supports import and export of OSCAL Assessment Plan \(AP\) files.

    Import OSCAL AP files from external tools to automatically generate engagements, control tests, test plans, user assignments, and test scope. Multiple AP files can be imported together for packages with multiple engagements.

    Export generates OSCAL AP files for auditors and authorizers, enabling other systems to understand what testing is planned or was performed.

-   **[Request control tailoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/continuous-risk-monitoring/request-control-tailoring.md)**

    After upgrading to version 22.0.2, make incremental changes to control sets while preserving the state of unchanged controls without having to reset the entire package life cycle. Supported modifications include adding new controls, marking controls as not applicable, changing control allocation \(baseline to inherited or hybrid\), and modifying inheritance configurations.

-   **[Inherit from multiple providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/continuous-risk-monitoring/inherit-from-multiple-providers.md)**

    After upgrading to version 22.0.2, Controls can inherit individual control requirements from multiple Common Control Providers \(CCPs\) across different authorization packages. Previously, inheritance was limited to a single provider per control, which required creating multiple duplicate inherited controls when requirements came from different sources.

-   **[Control grid view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/continuous-risk-monitoring/view-controls-in-grid-view.md)**

    After upgrading to version 22.0.2, edit implementation statements and attestation respondents directly in a hierarchical data grid through the Controls tab in an authorization package.

-   **[Control tests grid view in Engagements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/continuous-risk-monitoring/view-control-tests-in-grid-view.md)**

    After upgrading to version 22.0.2, toggle between traditional related list and hierarchical data grid on the Control tests tab. Changes to assessment procedure effectiveness automatically cascade to parent control test effectiveness.

-   **[CAM workflow configuration enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/continuous-risk-monitoring/cam-workflow-configurator.md)**

    After upgrading to version 22.0.2, control button visibility, UI page access, and related list actions across different workflow steps. Previously, related list actions \(such as add or remove buttons for information types or baseline control actions\) required manual scripting to support custom workflows.

    The following new state model attributes have been introduced:

    -   Required Authorization Documents Page
    -   Required Overlay Page
    -   Required Information Type Actions
    -   Required Baseline Actions
    -   Required Overlay Actions
    -   Request Control Tailoring
    -   Generate OSCAL AP
    -   Generate OSCAL AR

## UI changes

-   **[Properties page enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/continuous-risk-monitoring/cam-components-installed.md)**

    The Properties page includes new configuration options:

    -   **Homepage Title** enables you to customize the workspace homepage name.
    -   The **Days Before Next Authorization** property is now available on the UI page.
-   **Vertical layout for package forms**

    Package detail forms now use a structured vertical layout instead of the previous horizontal tab arrangement.


## Activation information

Install Continuous Authorization and Monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

