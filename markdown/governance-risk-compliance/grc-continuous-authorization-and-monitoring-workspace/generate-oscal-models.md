---
title: Export OSCAL SSP
description: Generate and download Open Security Controls Assessment Language \(OSCAL\) JSON formatted System Security Plan \(SSP\) files containing authorization package data including controls, boundaries, and system implementation details from the Authorization package overview record page. The authorization package must be in Implement state or later to generate OSCAL System Security Plan \(SSP\) files.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Export OSCAL files from authorization package, Export in OSCAL format, CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export OSCAL SSP

Generate and download Open Security Controls Assessment Language \(OSCAL\) JSON formatted System Security Plan \(SSP\) files containing authorization package data including controls, boundaries, and system implementation details from the Authorization package overview record page. The authorization package must be in Implement state or later to generate OSCAL System Security Plan \(SSP\) files.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_manager, or sn\_irm\_cont\_auth.info\_system\_sec\_officer

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Select **Authorization packages** from the **RMF** list.

4.  From the list view, select the authorization package record for SSP generation.

    **Note:** The authorization package must be in the Implement, Assess, Authorize, or Monitor state to generate OSCAL SSP.

5.  To export OSCAL SSP, select **Generate OSCAL SSP** from the **Generate OSCAL** drop-down.

    **Note:** If you’re using the Xanadu version, start from Step 5 in [Export data in OSCAL format](https://www.servicenow.com/docs/bundle/xanadu-governance-risk-compliance/page/product/grc-cam-workspace/task/generate-oscal-models.html).

    A message appears indicating file generation is in progress. The system generates files containing JSON data and associated diagrams. Refresh the page before downloading the JSON files.

6.  To download the SSP zip file, select the **Download OSCAL SSP** from the **Download OSCAL** drop-down list.

    ![Dowloading OSCAL SSP.](../image/cam-oscal-ssp-without-zip.gif)

    **Important:** Verify that the pop-up blocker is disabled for the URL so that the SSP zip file is automatically downloaded to your local repository.

    The downloaded zip file contains catalog.json, overlay-catalog.json, profile.json, ssp.json, and poam.json files. If diagrams attach to relevant fields or link to the package boundary, they appear in the zip file contents. Available diagrams include dataflow diagrams, network architecture diagrams, authorization boundary diagrams, and enterprise architecture diagrams.

    **Note:**

    -   If no POA&amp;M is linked to the Authorization Package, the poam.json file will not be generated.
    -   The overlay-catalog.json file contains only the policies linked to the Authorization Package. If no catalog overlay is linked to the Authorization Package, the overlay-catalog.json file will not be generated. Multiple overlay-catalog files will be generated one for each overlay.
    -   To customize the OSCAL behavior for export, see the [OSCAL Model customization support \[KB1650397\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650397) article in the Now Support Knowledge Base.
    For more information on OSCAL import error, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.


**Parent Topic:**[Export OSCAL files from authorization package](../concept/export-oscal-files-from-authorization-package.md)

