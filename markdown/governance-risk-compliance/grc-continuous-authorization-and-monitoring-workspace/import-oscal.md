---
title: Import in OSCAL format
description: Import Open Security Controls Assessment Language \(OSCAL\) formatted Catalog, System Security Plan \(SSP\), and Plan of Action and Milestones \(POA&amp;M\) into Continuous Authorization and Monitoring using a guided playbook experience that validates data and manages conflicts.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2025-12-29"
reading_time_minutes: 3
breadcrumb: [CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import in OSCAL format

Import Open Security Controls Assessment Language \(OSCAL\) formatted Catalog, System Security Plan \(SSP\), and Plan of Action and Milestones \(POA&amp;M\) into Continuous Authorization and Monitoring using a guided playbook experience that validates data and manages conflicts.

The Continuous Authorization and Monitoring \(CAM\) Open Security Controls Assessment Language \(OSCAL\) import feature provides a structured process for integrating security control data from external sources. This guided experience supports importing JSON files in Catalog, System Security Plan \(SSP\), Plan of Action and Milestones \(POA&amp;M\) and Assessment Plan \(AP\) models using the OSCAL format developed by the National Institute of Standards and Technology \(NIST\).

CAM supports OSCAL version 1.1.2.

The import process guides you through structured stages from the OSCAL Import landing page. The landing page displays previously imported OSCAL files with their current statuses. Select New Import from the All OSCAL Imports landing page to start a new import.

The import process follows these structured stages.

-   The Details stage captures import information including the OSCAL model, source, and notification recipients for import status updates.
-   The Attachments stage accepts file uploads for OSCAL-formatted content corresponding to the selected model. For Catalog OSCAL model, upload the catalog file to proceed. For SSP OSCAL model, upload catalog, profile, SSP, overlay files if applicable, and POA&amp;M files if needed. For POA&amp;M OSCAL model, upload one or more POA&amp;M files linked to the same authorization package.
-   The Package Mapping stage associates Plan of Action and Milestones \(POA&amp;M\) files with specific authorization packages. This stage applies only when selecting the POA&amp;M OSCAL model.
-   The Roles and Responsibilities stage assigns users to specific roles for the imported files. These users maintain their roles throughout each step in the authorization package. This stage applies only when selecting the System Security Plan \(SSP\) Open Security Controls Assessment Language \(OSCAL\) model.
-   The Preview and Override stage displays files for upload with counts of records to be created or skipped. Take appropriate actions including importing, skipping, or overriding records. You can override only files in the skipped state. Overriding a package overrides all associated package data.

For step-by-step instructions on importing each OSCAL model, see the following topics:

-   [Import OSCAL catalog](../task/import-oscal-cam-ws.md)
-   [Import OSCAL SSP](../task/import-oscal-ssp-cam-ws.md)
-   [Import OSCAL POA&amp;M](../task/import-oscal-poa-m.md)

For more information on the OSCAL import error and control catalog, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.

-   **[Import OSCAL catalog](../task/import-oscal-cam-ws.md)**  
Import Open Security Controls Assessment Language \(OSCAL\) JSON format in the Catalog files into CAM workspace. This task focuses on uploading and processing the required JSON files to begin the import process.
-   **[Import OSCAL SSP](../task/import-oscal-ssp-cam-ws.md)**  
Import Open Security Controls Assessment Language \(OSCAL\) files in the System Security Plan \(SSP\) model into Continuous Authorization and Monitoring workspace. Import OSCAL SSP enables you import authorization packages, authorization boundary, controls, and others in OSCAL format.
-   **[Import OSCAL POA&amp;M](../task/import-oscal-poa-m.md)**  
Import Open Security Controls Assessment Language \(OSCAL\) Plans of Action and Milestones \(POA&amp;M\) JSON files by selecting the **POA&amp;M** model into Continuous Authorization and Monitoring workspace. Import OSCAL POA&amp;M action enables you to upload POA&amp;Ms files and link it to CAM relevant objects like controls, authorization packages, engagements, and others in OSCAL format.
-   **[Import OSCAL AP](../task/import-oscal-ap-cam-ws.md)**  
Import Assessment Plan \(AP\) data in Open Security Controls Assessment Language \(OSCAL\) format to create or update authorization packages with assessment-related information including engagements, control tests, test plans, and assessment procedures.

**Parent Topic:**[CAM OSCAL](oscal-cam-ws.md)

