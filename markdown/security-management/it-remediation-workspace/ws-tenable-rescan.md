---
title: Rescan Tenable.io and Tenable.sc vulnerable items from the Vulnerability Response workspaces
description: Verify your vulnerable items have been remediated between scheduled scanning cycles. Initiate rescans in the Tenable.io and Tenable.sc products on-demand from the IT Remediation Workspace in your ServiceNow AI Platform instance.
locale: en-US
release: xanadu
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Rescan vulnerable items and remediation tasks in the IT Remediation Workspace, Using the IT Remediation Workspace, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Rescan Tenable.io and Tenable.sc vulnerable items from the Vulnerability Response workspaces

Verify your vulnerable items have been remediated between scheduled scanning cycles. Initiate rescans in the Tenable.io and Tenable.sc products on-demand from the IT Remediation Workspace in your ServiceNow AI Platform instance.

## Before you begin

To initiate a rescan for the Tenable.io and Tenable.sc products from the classic environment of Vulnerability Response, see [Initiate rescan for the Tenable.sc integration](vr-tenable-rescan.md) and [Initiate rescan for the Tenable.io integration](vr-tenable-rescan-tenable-io.md).

To perform rescans from your ServiceNow AI Platform, you need your Tenable credentials. For more information about setting up your Tenable.io and Tenable.sc scanners and importing your credentials from Tenable, see [Configure the Tenable Vulnerability Integration using Setup Assistant](vr-tenable-config-in-SA.md).

-   You can initiate rescans on-demand for vulnerable items and remediation tasks that have the Tenable.io or Tenable.sc product as the source from the IT Remediation Workspace in your ServiceNow AI Platform.
-   On a remediation task record, the record can be in any state other than **Closed**, and all the associated VIs must be from the Tenable.io or the Tenable.sc product.
-   To initiate rescans in the IT Remediation Workspace from vulnerable item and remediation task records, these records must be assigned to you.

Roles required:

-   sn\_vul.remediation\_owner for the IT Remediation Workspace
-   sn\_vul.vulnerability\_analyst or sn\_vul.vulnerability\_admin from the Vulnerability Manager Workspace

## Procedure

1.  Navigate to a vulnerable item or a remediation task that has been assigned to you and open it.

    **Note:** If you choose a remediation effort to initiate a rescan, all the VIs associated with that record are scanned.

2.  In the upper right of a record, click **Rescan**.

    You are prompted to choose the instance or instances for the rescan and the scanner credentials you want to use to access the scanner. The displayed credentials are those imported by the Tenable.io and Tenable.sc Scan Credential Integrations.

3.  In the modal, click the search icon.

    In the Select a scan credential modal that displays, use the filters in the column headings to select the name, instance and or instances, and the credential types that you want to use.

    See the following table for more information.

<table id="choicetable_em4_cxs_xqb"><thead><tr><th align="left" id="d436405e231">

Column

</th><th align="left" id="d436405e234">

Description

</th></tr></thead><tbody><tr><td id="d436405e240">

**Name**

</td><td>

Choose the name of the credential\(s\) you want. Roll over the column title. Use the vertical three dots menu in the column title to filter the names of your credentials.

</td></tr><tr><td id="d436405e249">

**Integration instance**

</td><td>

Choose a Tenable.io or, if for Tenable.sc, the Tenable.sc integration instance that you want to initiate the rescan from.

 All your integration instances for Tenable.io or Tenable.sc are displayed. If a VI exists in more than one integration instance, you can use this filter to limit or expand the instances you want to scan.

 **Note:** If you choose to rescan VIs from a remediation task record for a single integration instance, only the active VIs that are associated with that remediation task, for that instance, using the credential\(s\) that you select are scanned.

</td></tr><tr><td id="d436405e282">

**Type**

</td><td>

These are the available scanner credentials imported from the Tenable.io or Tenable.sc products.Roll over the column title. Use the vertical three dots menu in the column title to open the modal and select the credential types you want.

</td></tr></tbody>
</table>4.  In the updated Rescan modal, click **Request rescan**.

    The message, `The scan request is being processed` is displayed.

5.  Click the **View status** link in the message to view the progress of the scan.

    The scan record \(VSCAN\#\) is displayed. Below the record header with the scan number, the related item lists display the following information:

    -   The Details list displays the scan number of the parent scan, the scanner source, and the state. View completed and failed scans under the Scan Summary section.
    -   The Scans list displays any child scans and their states. When all the child scans complete, the state of the parent scan transitions to Complete.
    -   The Source list displays the vulnerable item used for the scan, the associated configuration item and vulnerability, the state of the VI, and its remediation status.
    Your ServiceNow AI Platform® instance tracks the rescan status until it successfully completes, or, until the set tracking period times out, whichever happens first.

    The time-out does not stop the scan. The time-out refers to when the ServiceNow AI Platform® stopped tracking your rescan status, not when the actual rescan stopped.

    All VIs that have transitioned, or will transition, to Closed/Fixed are imported with the next scheduled import of the Tenable.io or Tenable.sc integrations.


