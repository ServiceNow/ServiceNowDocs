---
title: View configuration items with vulnerabilities in the IT Remediation Workspace
description: The following enhancements were added to remediation tasks with version 16.1 of the Vulnerability Response application.
locale: en-US
release: zurich
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# View configuration items with vulnerabilities in the IT Remediation Workspace

The following enhancements were added to remediation tasks with version 16.1 of the Vulnerability Response application.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

The itil or cmdb\_read role is also required if you want to view CI data in the workspaces.

## About this task

See the configuration items \(CI\)s that are assigned to you that have vulnerabilities on them. Click **Impacted CIs** scorecard. Click the Filter list in the upper left to toggle between **Assigned to me** and **Assigned to my groups**. From the List view, click the links.

## Procedure

1.  Navigate to **All** &gt; **Vulnerability Response** &gt; **IT Remediation Workspace**.

    The Home landing page is displayed.

2.  Alternatively, you can view these lists from the links on the List view, or by navigating to their modules, for example, **All** &gt; **Vulnerability Response** &gt; **Remediation Tasks**.

3.  Choose one to continue.

    Depending on what is selected in the filter toggle, view the lists of the following records that are assigned to you or to you and your groups.

    |Option|Description|
    |------|-----------|
    |**Assigned remediation tasks**|Remediation tasks \(RT\). For more information about the actions you can take from an RT, see [Use remediation task records in the IT Remediation Workspace](vr-ws-remed-task.md).|
    |**Preferred solution on VIs**|Records \(VITs\) that have preferred solutions mapped to them. If the Vulnerability Solution Management application is installed, Preferred Solutions are the highest-superseding solutions that are applied to records. The list of solutions is based on the records in the remediation task record. To see what you can do from solution records, see [Use remediation task records in the IT Remediation Workspace](vr-ws-remed-task.md).|
    |**Impacted CIs**|\(CI\)s with vulnerabilities. After its initial population, this scorecard shows updated counts of your vulnerable CIs after new VIs that have vulnerabilities are added, or when there are state changes to existing VIs. See the following steps for how to view this record and what you can do from this list.|

4.  Click the **Impacted CIs** scorecard.

    The list of CI records is displayed.

5.  Click a configuration item to open its record.

    The record is displayed.

    The related lists permit you to view details and various associated records. New available data on this record with this release includes:

    -   A time line that shows the recent activity on this record.
    -   Any change requests that are associated with this CI.
    -   Easily navigate to scorecards and view the remediation tasks, vulnerable items, and preferred solutions associated with this CI.
    -   You can navigate to the scorecards and view the preferred patches associated with this CI. Preferred patches are the patches associated with the vulnerable items. The Patches tab in the Related list displays the installed and missing patches for the CIs.
    -   Information about the CI that includes Class, Location, Internet-facing, Environment, and Maintenance schedule.

