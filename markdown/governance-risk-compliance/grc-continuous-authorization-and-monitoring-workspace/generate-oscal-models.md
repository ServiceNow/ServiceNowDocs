---
title: Export OSCAL SSP
description: From the Authorization package overview record page, generate zip files and export the record's mapped content details in OSCAL format. To generate OSCAL SSP, the selected Authorization package must be in implemented state or after that. This action enables you to export your authorization package from CAM.
locale: en-US
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Export in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export OSCAL SSP

From the Authorization package overview record page, generate zip files and export the record's mapped content details in OSCAL format. To generate OSCAL SSP, the selected Authorization package must be in implemented state or after that. This action enables you to export your authorization package from CAM.

## Before you begin

Role required:

-   sn\_irm\_cont\_auth.admin
-   sn\_irm\_cont\_auth.system\_owner
-   sn\_irm\_cont\_auth.authorization\_official
-   sn\_irm\_cont\_auth.info\_system\_sec\_manager
-   sn\_irm\_cont\_auth.info\_system\_sec\_officer

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the List icon \(![List](../image/ws-list-icon.png)\).

3.  Select Authorization packages from the **RMF** list.

4.  From the list view, select the authorization package record for which to generate SSP files.

    **Note:** The authorization package must be in the Implement, Assess, Authorize, or Monitor state to generate OSCAL SSP.

5.  Navigate to the Controls tab.

6.  On the Controls tab, from the Generate OSCAL dropdown list, select **Generate OSCAL SSP**.

    A message appears stating that the word file is being generated. A zip is generated which contains JSON files along with some diagrams. You’ll have to refresh the page before you download the JSON files.

7.  Select More icon and then select **Download OSCAL SSP** from the **Generate OSCAL SSP** drop-down list to download the SSP zip file.![Dowload oscal-ssp-zip.](../image/cam-oscal-ssp-without-zip.png)

    **Important:** Verify that the pop-up blocker is turned off for the URL so that the SSP zip file is automatically downloaded to your local repository.

    You can view the catalog.json, overlay-catalog.json, profile.json, ssp.json files. Additionally, if any diagrams attached to the respective fields and boundary for the package are linked to it, then they’re also available in the contents of the zip. The diagrams can be a catalog dataflow diagram, network architecture diagram, or an authorization boundary diagram, available as png files in the zip.

    **Note:**

    -   The overlay-catalog.json file contains only the policies linked to the Authorization Package. If no catalog overlay is linked to the Authorization Package, the overlay-catalog.json file won’t be generated.
    -   To customize the OSCAL behavior for export, see the [OSCAL Model customization support \[KB1650397\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650397) article in the Now Support Knowledge Base.
    For more information on OSCAL import error, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.


**Parent Topic:**[Export in OSCAL format](../concept/oscal-support-cam.md)

