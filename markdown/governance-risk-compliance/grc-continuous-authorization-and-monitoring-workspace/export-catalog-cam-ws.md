---
title: Export OSCAL catalog
description: Export selected control objectives from Continuous Authorization and Monitoring to Open Security Controls Assessment Language \(OSCAL\) JSON format for external system integration or catalog backup.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Export in OSCAL format, CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export OSCAL catalog

Export selected control objectives from Continuous Authorization and Monitoring to Open Security Controls Assessment Language \(OSCAL\) JSON format for external system integration or catalog backup.

## Before you begin

Role required: sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_manager,sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.system\_owner, or sn\_irm\_cont\_auth.reader

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Select Control objectives from the **Compliance** list.

4.  From the list view, select one or more control objectives records which need to be exported.

5.  Select **OSCAL Export**.

    ![Export OSCAL of control objectives.](../image/cam-export-oscal-control-objective.gif)

    **OSCAL Export** pop-window displays.

6.  In the pop-up window, enter the **Title** and **Version** and then select **Export**.

    **Important:** Verify that the pop-up blocker is turned off for the URL so that the Catalog JSON file is automatically downloaded to your local repository.

    The catalog JSON file is downloaded in your local repository.


**Parent Topic:**[Export in OSCAL format](../concept/oscal-support-cam.md)

