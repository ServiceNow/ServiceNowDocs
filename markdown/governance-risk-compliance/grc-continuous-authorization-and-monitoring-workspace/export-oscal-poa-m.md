---
title: Export OSCAL POA&amp;M
description: Generate zip files Plan of Action and Milestones \(POA&amp;M\) data in Open Security Controls Assessment Language \(OSCAL\) JSON format from the Authorization package overview record page. The authorization package must be in Implement state or later, and a POA&amp;M file must link to the selected authorization package.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 1
breadcrumb: [Export OSCAL files from authorization package, Export in OSCAL format, CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export OSCAL POA&amp;M

Generate zip files Plan of Action and Milestones \(POA&amp;M\) data in Open Security Controls Assessment Language \(OSCAL\) JSON format from the Authorization package overview record page. The authorization package must be in Implement state or later, and a POA&amp;M file must link to the selected authorization package.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_manager, or sn\_irm\_cont\_auth.info\_system\_sec\_officer

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Select **Authorization packages** from the **RMF** list.

4.  From the list view, select the authorization package record for which you want to generate a POA&amp;M file.

    **Note:** The authorization package must be in the Implement, Assess, Authorize, or Monitor state to generate OSCAL POA&amp;M.

5.  To export OSCAL POA&amp;M, select **Generate OSCAL POAM** from the **Generate OSCAL** drop-down.

    **Note:** To generate the OSCAL POA&amp;M, the POA&amp;M file must be linked to the selected Authorization package.

    A message appears to indicate that file generation is in progress. Refresh the page before downloading the JSON files.

    ![Generating OSCAL POA&M.](../image/cam-oscal-export-poa-m1.png)

6.  To download the POA&amp;M zip file, select **Download OSCAL POAM** from the **Download OSCAL** drop-down list.

    **Note:**

    -   If there’s POA&amp;M linked to the authorization package, the POA&amp;M files are generated.
    -   Verify that the pop-up blocker is turned off for the URL so that the POA&amp;M zip file is automatically downloaded to your local repository.
    To customize the OSCAL behavior for export, see the [OSCAL Model customization support \[KB1650397\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650397) article in the Now Support Knowledge Base.

    For more information on OSCAL import error, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.


**Parent Topic:**[Export OSCAL files from authorization package](../concept/export-oscal-files-from-authorization-package.md)

