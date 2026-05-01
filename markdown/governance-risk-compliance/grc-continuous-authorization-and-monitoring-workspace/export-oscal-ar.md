---
title: Export OSCAL AR
description: Export Assessment Results \(AR\) data in Open Security Controls Assessment Language \(OSCAL\) JSON format to share assessment outcomes including control test results, findings, and attestations from completed engagements. The authorization package must be in Assess, Authorize, or Monitor state.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [Export OSCAL files from authorization package, Export in OSCAL format, CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export OSCAL AR

Export Assessment Results \(AR\) data in Open Security Controls Assessment Language \(OSCAL\) JSON format to share assessment outcomes including control test results, findings, and attestations from completed engagements. The authorization package must be in Assess, Authorize, or Monitor state.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_manager, or sn\_irm\_cont\_auth.info\_system\_sec\_officer

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Select **Authorization packages** from the **RMF** list.

4.  From the list view, select the authorization package record for which you want to generate an AR file.

    **Note:** The authorization package must be in the Assess, Authorize, or Monitor state to generate OSCAL AR.

5.  To export OSCAL POA&amp;M, select **Generate OSCAL AR** from the **Generate OSCAL** drop-down.

    **Note:** To generate the OSCAL AR, the AR file must be linked to the selected Authorization package.

    A message appears to indicate that file generation is in progress. Refresh the page before downloading the JSON files.

6.  To download the AR zip file, select **Download OSCAL AR** from the **Download OSCAL** drop-down list.

    **Note:** Verify that the pop-up blocker is turned off for the URL so that the AR zip file is automatically downloaded to your local repository.

    To customize the OSCAL behavior for export, see the [OSCAL Model customization support \[KB1650397\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650397) article in the Now Support Knowledge Base.

    For more information on OSCAL import error, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.

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

**Parent Topic:**[Export OSCAL files from authorization package](../concept/export-oscal-files-from-authorization-package.md)

