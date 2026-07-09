---
title: Export OSCAL Assessment Results
description: Export the OSCAL Assessment Results \(AR\) file for an authorization package from the CAM Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-oscal-assessment-result-export.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 2
breadcrumb: [Export in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export OSCAL Assessment Results

Export the OSCAL Assessment Results \(AR\) file for an authorization package from the CAM Workspace.

## Before you begin

-   The authorization package must be in the Assess, Authorize, or Monitor step.
-   At least one control test in the engagement must have a closed state. Accepted closed states are:
    -   Closed Complete
    -   Closed Incomplete
    -   Closed Skipped

Roles required:

-   Information System Security Manager \(sn\_irm\_cont\_auth.info\_system\_sec\_manager\)
-   Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\)
-   CAM Administrator \(sn\_irm\_cont\_auth.admin\)

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the **List** icon.

3.  Select **Authorization packages** from the RMF list.

4.  Select the authorization package record in the Assess, Authorize, or Monitor step for which you want to generate an AR file.

5.  Select **Generate OSCAL**.

    A banner appears with the message: `The files are being generated. Refresh the page after some time, then select Download OSCAL Files to download the OSCAL files.`

    The system starts generating OSCAL files asynchronously. This process takes a few minutes depending on package complexity. The Download OSCAL Files button appears when the process is complete.

    A single AR JSON file is generated for each engagement linked to the authorization package. If the package has multiple engagements, multiple AR files are generated.

    **Warning:** Each time you run a generate operation, any previously generated OSCAL files for the package are deleted and replaced.

6.  After the files are generated, select **Download OSCAL Files**.

    \[Omitted image "download-oscal.png"\] Alt text: Download OSCAL files

    The **Download OSCAL Files** button appears only after file generation completes. If generation is in progress, the button is unavailable.

    **Note:** Confirm that the pop-up blocker is turned off for the URL so that the ZIP file downloads automatically to your local machine.

    A ZIP file is downloaded containing the following OSCAL files:

    -   Catalog JSON file
    -   Profile JSON file
    -   SSP JSON file
    -   Overlay Catalog JSON file \(if overlays are configured. Also includes overlays from associated control tailoring requests\)
    -   Assessment Plan \(AP\) JSON file \(one per engagement\)
    -   Assessment Results \(AR\) JSON file \(one per engagement\)
    -   POA&amp;M JSON file \(included if POA&amp;M items exist\)
    The exported OSCAL AR JSON file contains the following structure:

    -   Reviewed controls: Control selections with control IDs and statement IDs from completed control tests
    -   Control objective IDs: References to test templates associated with the engagement
    -   Findings: Array of issues linked to control tests that failed assessment
        -   UUID corresponds to the issue or POAM record
        -   Target contains control test reference and UUID
        -   State is "not satisfied" when findings exist
        -   Description and title provide issue details
    -   Attestations: Objects for all completed controls including:
        -   Responsible parties \(control test owner and UUID\)
        -   Control test title and UUID
        -   Operational effectiveness rating from the control test
        -   Assessment procedures linked to the control test with their operational effectiveness ratings
    -   Metadata and Local Definitions
        -   Metadata: Responsible parties, roles, and all engagement fields
        -   Local definitions: Related controls with control IDs, control objectives, and assessment procedure labels

## What to do next

Validate these files using the OSCAL CLI validator and import them into other systems or share them with external auditors for assessment planning.

For information about the OSCAL fields exported in the AR file and their corresponding ServiceNow CAM fields, see .

**Parent Topic:**[Export in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-support-cam.md)

