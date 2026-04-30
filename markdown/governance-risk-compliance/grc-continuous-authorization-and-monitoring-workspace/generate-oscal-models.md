---
title: Export OSCAL SSP
description: From the Authorization package overview record page in the CAM Workspace, generate ZIP files and export the mapped content details for the record in OSCAL format. To generate OSCAL System Security Plan Model \(SSP\), the selected authorization package must be in the implemented state or further.
locale: en-US
release: yokohama
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exporting in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export OSCAL SSP

From the Authorization package overview record page in the CAM Workspace, generate ZIP files and export the mapped content details for the record in OSCAL format. To generate OSCAL System Security Plan Model \(SSP\), the selected authorization package must be in the implemented state or further.

## Before you begin

Role required: The users with the following roles can export OSCAL SSP sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, and sn\_irm\_cont\_auth.admin.

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the primary navigation, select the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  In the RMF list, select **Authorization packages**.

4.  From the list view, select the authorization package record for which you want to generate SSP files.

    **Note:** The authorization package must be in the Implement, Assess, Authorize, or Monitor state to generate OSCAL SSP.

5.  Export OSCAL SSP by selecting **Generate OSCAL SSP**.

6.  In the pop-up window, select **Proceed**.

    A message appears stating that the word file is being generated. A ZIP file is generated that contains JSON files along with some diagrams. You must refresh the page before you download the JSON files.

7.  From the Generate OSCAL SSP drop-down list, download the SSP ZIP file by selecting **Download OSCAL SSP** f.

    **Important:** Verify that the pop-up blocker is turned off for the URL so the SSP ZIP file downloads to your local repository automatically.

    You can view the `catalog.json`, `overlay-catalog.json`, `profile.json`, `ssp.json` files. If any diagrams attached to the respective fields and boundaries are linked to the authorization package, then they’re also available in the contents of the ZIP file. The diagrams, which can be a catalog dataflow diagram, network architecture diagram, or an authorization boundary diagram, are available as PNG files in the ZIP file.

    **Note:**

    -   The `overlay-catalog.json` file contains only the policies linked to the authorization package. If no catalog overlay is linked to the authorization package, the `overlay-catalog.json` file isn't generated.
    -   To customize the OSCAL behavior for export, see the [OSCAL Model customization support \[KB1650397\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650397) article in the Now Support Knowledge Base.

For more information on OSCAL import error, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.

**Parent Topic:**[Exporting in OSCAL format](../concept/oscal-support-cam.md)

