---
title: Continuous Authorization and Monitoring release notes
description: The ServiceNow Continuous Authorization and Monitoring application provides a structured approach to defining an authorization package and walking through the seven stages of the NIST Risk Management Framework. Continuous Authorization and Monitoring was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Continuous Authorization and Monitoring release notes

The ServiceNow® Continuous Authorization and Monitoring application provides a structured approach to defining an authorization package and walking through the seven stages of the NIST Risk Management Framework. Continuous Authorization and Monitoring was enhanced and updated in the Australia release.

## Continuous Authorization and Monitoring highlights for the Australia release

-   Import and export OSCAL data for Assessment Plan \(AP\) and Assessment Results \(AR\) formats to streamline compliance reporting.
-   Skip the attestation stage for all controls in a package and move controls directly to the Monitor step to accelerate package progression.
-   Populate additional control fields when importing and exporting OSCAL data for SSP, AP, and AR formats to capture richer compliance details.
-   Raise control tailoring requests to make incremental changes to control sets in authorized packages without resetting the entire package life cycle.

See [Continuous Authorization and Monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-cam-landing-page.md) for more information.

**Important:** Continuous Authorization and Monitoring is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **Support for exporting and importing the OSCAL Assessment Results \(AR\) model**

    After upgrading to version 22.3.3, Continuous Authorization and Monitoring supports import and export of OSCAL data for Assessment Results \(AR\) format.

-   **[Skip attestations configuration for controls within a package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/categorize.md)**

    After upgrading to version 22.3.3, skip the attestation stage at the package level and move controls directly from Draft to Review without completing the attestation workflow.

-   **[Control tailoring request enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/request-control-tailoring.md)**

    After upgrading to version 22.3.3, control tailoring requests support changes to overlay controls. You can add new overlay controls or modify existing ones within a control tailoring request.

-   **[OSCAL export and import enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/oscal-cam-ws.md)**

    After upgrading to version 22.0.2, OSCAL import and export support additional details for various records, including status, frequency, weighting, implementation statement, control tailoring requests, overlays, and activities.

-   **[Support for exporting and importing the OSCAL Assessment Plan \(AP\) model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/oscal-cam-ws.md)**

    After upgrading to version 22.0.2, Continuous Authorization and Monitoring supports import and export of OSCAL data for Assessment Plan \(AP\) format.

-   **[Request control tailoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/request-control-tailoring.md)**

    After upgrading to version 22.0.2, make incremental changes to control sets while preserving the state of unchanged controls without having to reset the entire package life cycle. Supported modifications include adding new controls, marking controls as not applicable, changing control allocation \(baseline to inherited or hybrid\), and modifying inheritance configurations.

-   **[Inherit from multiple providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/inherit-from-multiple-providers.md)**

    After upgrading to version 22.0.2, Controls can inherit individual control requirements from multiple Common Control Providers \(CCPs\) across different authorization packages. Previously, inheritance was limited to a single provider per control, which required creating duplicate inherited controls when requirements came from different sources.

-   **[Control grid view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/view-controls-in-grid-view.md)**

    After upgrading to version 22.0.2, edit implementation statements and attestation respondents directly in a hierarchical data grid through the Controls tab in an authorization package.

-   **[Control tests grid view in Engagements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/view-control-tests-in-grid-view.md)**

    After upgrading to version 22.0.2, toggle between traditional related list and hierarchical data grid on the Control tests tab. Changes to assessment procedure effectiveness automatically cascade to parent control test effectiveness.

    Package detail forms now use a structured vertical layout instead of the previous horizontal tab arrangement.

-   **[CAM workflow configuration enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/cam-workflow-configurator.md)**

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

## UI changes

-   **[Properties page enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/cam-components-installed.md)**

    The Properties page includes new configuration options:

    -   Use **Homepage Title** to customize the workspace homepage name.
    -   The **Days Before Next Authorization** property is now available on the UI page.

## Activation information

Install Continuous Authorization and Monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

