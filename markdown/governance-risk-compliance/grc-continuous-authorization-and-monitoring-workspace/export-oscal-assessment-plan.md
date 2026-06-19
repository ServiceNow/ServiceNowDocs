---
title: Export an OSCAL Assessment Plan
description: Export engagement data as OSCAL Assessment Plan files to share testing plans with auditors or import into external systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/export-oscal-assessment-plan.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Export in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export an OSCAL Assessment Plan

Export engagement data as OSCAL Assessment Plan files to share testing plans with auditors or import into external systems.

## Before you begin

-   Authorization package is in the Assess step or later
-   At least one engagement with associated entities exists in the package

Role required:

-   Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\)
-   CAM Administrator \(sn\_irm\_cont\_auth.admin\)

## About this task

Exporting an OSCAL Assessment Plan from CAM generates a zip file containing all necessary OSCAL model files. The export includes the Assessment Plan file for each engagement, along with supporting files such as Catalog, Profile, SSP, Overlay, and POAM. Overlay, and POAM are optional. You can use exported files to share testing plans with external auditors or import into other OSCAL-compliant systems.

The export process generates files asynchronously. After generation completes, download buttons appear on the screen.

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** and then select the **lists icon**.

2.  From the **Authorization packages** in the RMF list, select an authorization package record in Assess step or later.

3.  Navigate to the Engagements tab.

4.  Select **Generate OSCAL**.

    A banner appears with the message: "The files are being generated. Please refresh the page after some time, then click 'Download OSCAL Files' to download the OSCAL files."

    The system starts generating OSCAL files asynchronously. This process takes a few minutes depending on package complexity. The **Download OSCAL Files** button appears when the process is complete.

5.  After the process is complete, select **Download OSCAL Files**.

    **Note:** Verify that the pop-up blocker is turned off for the URL so that the ZIP file is automatically downloaded to your local machine.

    A ZIP file is downloaded containing the following OSCAL files:

    -   Catalog JSON file
    -   Profile JSON file
    -   SSP JSON file
    -   Assessment Plan \(AP\) JSON file \(one per engagement\)
    -   Assessment Results \(AR\) JSON file \(one per engagement\)
    -   Overlay Catalog JSON file \(if overlays are configured. Also includes overlays from associated control tailoring requests\)
    -   POA&amp;M JSON file \(included if POA&amp;M items exist\)
    You can validate these files using the OSCAL CLI validator and import them into other systems or share them with external auditors for assessment planning.


**Parent Topic:**[Export in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-support-cam.md)

