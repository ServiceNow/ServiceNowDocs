---
title: Rescan Qualys vulnerable items from the Vulnerability Response workspaces
description: Verify that your vulnerable items have been remediated between scheduled scanning cycles. Initiate rescans in the Qualys product on-demand from the IT Remediation Workspace in your ServiceNow AI Platform instance.
locale: en-US
release: australia
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Rescan vulnerable items and remediation tasks in the IT Remediation Workspace, Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Rescan Qualys vulnerable items from the Vulnerability Response workspaces

Verify that your vulnerable items have been remediated between scheduled scanning cycles. Initiate rescans in the Qualys product on-demand from the IT Remediation Workspace in your ServiceNow AI Platform instance.

## Before you begin

To initiate a rescan for the Qualys product from the classic environment, see [Initiate rescan for the Qualys Vulnerability Integration](../concept/advanced-modifications.md#).

The Qualys scanners are deactivated by default in the Vulnerability Response application. If you try to perform a rescan from the vulnerable items or remediation tasks that have these applications as a source, the **Rescan** button is not available.

To activate these scanners, as a user with the sn\_vul.vulnerability\_admin role:

1.  Navigate to **All** &gt; **Vulnerability Response** &gt; **Vulnerability Scanning** &gt; **Scanners**.
2.  Locate the scanner product you want to activate and click the record to open it.
3.  Select the Active check box.
4.  Click **Update**.

    The product you activated is displayed in the Source field on vulnerable item and remediation task records after the next import, and **Rescan** is available as a UI action.


For more information about setting up your Qualys scanner, see [Set up scanner appliances](../concept/advanced-modifications.md#) and [Advanced Qualys configurations and modifications](../concept/advanced-modifications.md#).

-   You can initiate rescans on-demand for vulnerable items and remediation tasks that have the Qualys product as the source from the IT Remediation Workspace in your ServiceNow AI Platform.
-   On a remediation task record, the record can be in any state other than **Closed**, and all the associated VIs must be from the Qualys product.
-   To initiate rescans in the IT Remediation workspace from vulnerable item and remediation task records, these records must be assigned to you.

Roles required:

-   sn\_vul.remediation\_owner for the IT Remediation Workspace.
-   sn\_vul.vulnerability\_analyst or sn\_vul.vulnerability\_admin from the Vulnerability Manager Workspace.

## Procedure

1.  Navigate to a vulnerable item or a remediation task that has been assigned to you and open it.

    **Note:** If you choose a remediation effort to initiate a rescan, all the VIs associated with that record are scanned.

2.  In the upper right of the record, click **Rescan**.

3.  In the Rescan modal, choose an option profile.

    An option profile is required when you initiate a Qualys scan from your ServiceNow AI Platform®. Option profiles contain Qualys scan settings.

<table id="choicetable_itr_bmq_yqb"><thead><tr><th align="left" id="d175429e260">

Option

</th><th align="left" id="d175429e263">

Description

</th></tr></thead><tbody><tr><td id="d175429e269">

**Use default option profile**

</td><td>

This is the option profile that is set as the default for the integration instance. You select this profile when you set up your Qualys scanner. See [Set up scanner appliances](../concept/advanced-modifications.md#) for more information.

</td></tr><tr><td id="d175429e292">

**Specify option profile**

</td><td>

From the Option profile list, choose a profile to use for the scan.You can select the option profile you want to use for scans for matching configuration items.

</td></tr></tbody>
</table>4.  In the Rescan modal, click **Request rescan**.

    The message, `The scan request is being processed` is displayed.

5.  Click the **View status** link in the message to view the progress of the scan.

    The scan record \(VSCAN\#\) displays. Below the record header with the scan number, the related item lists display the following information:

    -   The Details list displays the scan number of the parent scan, the scanner source, and the state. View completed and failed scans under the Scan Summary section.
    -   The Scans list displays any child scans and their states. When all the child scans are completed, the state of the parent scan transitions to Complete.
    -   The Source list displays the vulnerable item used for the scan, the associated configuration item and vulnerability, the state of the VI, and its remediation status.
    Your ServiceNow AI Platform® instance tracks the rescan status until it successfully completes, or, until the set tracking period times out, whichever happens first.

    The time-out does not stop the scan. The time-out refers to when the ServiceNow AI Platform® stopped tracking your rescan status, not when the actual rescan stopped.

    All VIs that have transitioned, or will transition, to Closed/Fixed are imported with the next scheduled import of the Qualys integrations.


