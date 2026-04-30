---
title: Export OSCAL POA&amp;M from list view
description: Export selected Plans of Action and Milestones \(POA&amp;M\) records from the CAM list to an Open Security Controls Assessment Language \(OSCAL\) format.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 1
breadcrumb: [Export in OSCAL format, CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export OSCAL POA&amp;M from list view

Export selected Plans of Action and Milestones \(POA&amp;M\) records from the CAM list to an Open Security Controls Assessment Language \(OSCAL\) format.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_manager, or sn\_irm\_cont\_auth.info\_system\_sec\_officer

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Select **All POA&amp;Ms** from the **Continuous monitoring** list.

4.  Select the POA&amp;Ms from the list that you want to export.

    ![Selecting individual POA&M files.](../image/cam-oscal-individual-export-poa-m1.png)

5.  Select **OSCAL Export** to export the selected POA&amp;M files.

    **Note:** Verify that the pop-up blocker is turned off for the URL so that the POA&amp;M zip file is automatically downloaded to your local repository.


## Result

-   OSCAL POA&amp;M export is a synchronous process. Once the file is generated, it downloads automatically as a zip file in your local repository.
-   When POA&amp;Ms are associated with different authorization packages, CAM generates a zip file containing individual JSON files for each authorization package.

**Parent Topic:**[Export in OSCAL format](../concept/oscal-support-cam.md)

