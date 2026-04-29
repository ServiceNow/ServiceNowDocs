---
title: Rescan Rapid7 vulnerable items from the Vulnerability Response workspaces
description: Verify your vulnerable items have been remediated between scheduled scanning cycles. Initiate rescans in the Rapid7 product on-demand from the IT Remediation Workspace in your ServiceNow AI Platform instance.
locale: en-US
release: australia
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Rescan vulnerable items and remediation tasks in the IT Remediation Workspace, Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Rescan Rapid7 vulnerable items from the Vulnerability Response workspaces

Verify your vulnerable items have been remediated between scheduled scanning cycles. Initiate rescans in the Rapid7 product on-demand from the IT Remediation Workspace in your ServiceNow AI Platform instance.

## Before you begin

To initiate a rescan for the product from the classic environment, see [Initiate rescan for the Rapid7 Vulnerability Integration](vr-r7-rescan.md). This topic also includes information about how to schedule scans with the integration parameters on the Rapid7 integration instance.

The Rapid7 scanners are deactivated by default in the Vulnerability Response application. If you try to perform a rescan from the vulnerable items or remediation tasks that have Rapid7 application as a source, the **Rescan** button is not available.

To activate these scanners, as a user with the sn\_vul.vulnerability\_admin role:

1.  Navigate to **All** &gt; **Vulnerability Response** &gt; **Vulnerability Scanning** &gt; **Scanners**.
2.  Locate the scanner product you want to activate and click the record to open it.
3.  Select the Active check box.
4.  Click **Update**.

    The product you activated is displayed in the Source field on vulnerable item and remediation task records after the next import, and **Rescan** is available as a UI action.


-   You can initiate rescans on-demand for vulnerable items and remediation tasks that have the Rapid7 InsightVM product as the source from the IT Remediation Workspace in your ServiceNow AI Platform.
-   On a remediation task record, the record can be in any state other than **Closed**, and all the associated VIs must be from the Rapid7 product.
-   To initiate rescans in the IT Remediation workspace from vulnerable item and remediation task records, these records need to be assigned to you.

Roles required:

-   sn\_vul.remediation\_owner for the IT Remediation workspace
-   sn\_vul.vulnerability\_analyst or sn\_vul.vulnerability\_admin from the Vulnerability Manager Workspace

## Procedure

1.  Navigate to a vulnerable item or a remediation task that has been assigned to you and open it.

    **Note:** If you choose a remediation effort to initiate a rescan, all the VIs associated with that record are scanned.

2.  In the upper right of the record, click **Rescan**.

3.  In the Confirm rescan modal, click **Request rescan**.

    The message, `The scan request is being processed` is displayed.

4.  Click the **View status** link in the message to view the progress of the scan.

    The scan record \(VSCAN\#\) is displayed. Below the record header with the scan number, the related item lists display the following information:

    -   The Details list displays the scan number of the parent scan, the scanner source, and the state. View completed and failed scans under the Scan Summary section.
    -   The Scans list displays any child scans and their states. When all the child scans are completed, the state of the parent scan transitions to Complete.
    -   The Source list displays the vulnerable item used for the scan, the associated configuration item and vulnerability, the state of the VI, and its remediation status.
    Your ServiceNow AI Platform® instance tracks the rescan status until it successfully completes, or, until the set tracking period times out, whichever happens first.

    The time-out does not stop the scan. The time-out refers to when the ServiceNow AI Platform® stopped tracking your rescan status, not when the actual rescan stopped.

    All VIs that have transitioned, or will transition, to Closed/Fixed are imported with the next scheduled import of the Rapid7 integrations.


