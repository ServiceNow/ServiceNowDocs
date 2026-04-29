---
title: Export an OSCAL Assessment Plan
description: Export engagement data as OSCAL Assessment Plan files to share testing plans with auditors or import into external systems.
locale: en-US
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OSCAL Assessment Plan export and import, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export an OSCAL Assessment Plan

Export engagement data as OSCAL Assessment Plan files to share testing plans with auditors or import into external systems.

## Before you begin

-   Authorization package is in the Assess step or later
-   At least one engagement with associated entities exists in the package

Role required: sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, or sn\_irm\_cont\_auth.admin

## About this task

Exporting an OSCAL Assessment Plan from CAM generates a zip file containing all necessary OSCAL model files. The export includes the Assessment Plan file for each engagement, along with supporting files \(Catalog, Profile, SSP, Overlay, and POAM\). You can use exported files to share testing plans with external auditors or import into other OSCAL-compliant systems.

The export process generates files asynchronously. After generation completes, download buttons appear on the package form.

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** and then select the **lists icon**.

2.  From the **Authorization packages in the RMF** list, select an authorization package record in Assess step or later.

3.  On the Controls tab, select **Generate OSCAL** from the form actions.

4.  From the drop-down menu, select **Generate OSCAL AP**.

    The system starts generating OSCAL files asynchronously. This process takes a few minutes depending on package complexity. The **Download OSCAL AP** button appears when the process is complete.

5.  Select **Download OSCAL AP**.

    A zip file downloads containing all generated OSCAL files: Catalog, Profile, SSP, and one AP file per engagement in the package.

    The downloaded zip file contains OSCAL-compliant JSON files. You can validate these files using the OSCAL CLI validator and import them into other systems or share them with external auditors for assessment planning.


**Parent Topic:**[OSCAL Assessment Plan export and import](../concept/oscal-assessment-plan-import-export.md)

