---
title: Continuous Authorization and Monitoring release notes
description: The ServiceNow Continuous Authorization and Monitoring \(CAM\) application provides a standardized approach to defining an authorization package and walking through the seven stages of the National Institute of Standards and Technology \(NIST\) Risk Management Framework \(RMF\). CAM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Continuous Authorization and Monitoring release notes

The ServiceNow® Continuous Authorization and Monitoring \(CAM\) application provides a standardized approach to defining an authorization package and walking through the seven stages of the National Institute of Standards and Technology \(NIST\) Risk Management Framework \(RMF\). CAM was enhanced and updated in the Yokohama release.

## CAM highlights for the Yokohama release

-   Import catalog and System Security Plan \(SSP\) models with the new CAM Open Security Controls Assessment Language \(OSCAL\) import landing page.
-   Export and import SSP models and catalog models in the OSCAL format.
-   Export control objectives as a catalog in the OSCAL format.
-   Generate additional reports in Microsoft Word format, such as a Security Assessment Plan \(SAP\), Authorization to Operate \(ATO\) Letter, and Executive Summary.
-   Generate reports based on a Microsoft Word template.

See [Continuous Authorization and Monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/grc-cam-landing-page.md) for more information.

**Important:** Continuous Authorization and Monitoring is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[OSCAL Import landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/import-oscal.md)**

    Import files for catalog and SSP models on the new OSCAL Import landing page. Once the import process is initiated, you can check the status under the Import status section.

-   **[OSCAL Export button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/export-catalog-cam-ws.md)**

    Export selected control objectives in the OSCAL format with the new **OSCAL Export** button while in the control objectives list view.

-   **[ATO artifacts in Microsoft Word](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/generate-ato-artifacts-cam-ws.md)**

    Generate ATO artifacts from an authorization package in the Microsoft Word format. In CAM Workspace, you can use the **Generate SSP** drop-down list in a selected authorization package to generate the following reports:

    -   Security Assessment Plan \(SAP\)
    -   Authorization to Operate \(ATO\) Letter
    -   Executive Summary
    This enhancement verifies that all ATO artifacts are formatted consistently and can be shared and reviewed.


## Changed in this release

-   **[Generate the OSCAL SSP model of an authorization package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/generate-oscal-models.md)**

    Export the SSP model of an authorization package in the OSCAL format. The exported report contains only the control objectives linked to the authorization package and their additional information, such as inherited controls and the hierarchy of the control objectives.

-   **[Generate ATO artifacts in Microsoft Word and HTML templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/generate-ato-artifacts-cam-ws.md)**

    Use the Document designer plugin \(com.sn\_grc\_doc\_design\) to create report templates in Microsoft Word. A new property module has been introduced to select the template type as a Microsoft Word template in addition to an HTML template.


## Activation information

Install CAM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/grc-rn-landing.md)

