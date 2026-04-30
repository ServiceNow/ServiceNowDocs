---
title: Add a compensating control to the library
description: As a Vulnerability Manager or Analyst, add a list of compensatory controls to the Compensating Controls library in the Security Exposure Management Workspace, which can be applied for the risk reduction of host vulnerable items and remediation tasks.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Add a compensating control to the library

As a Vulnerability Manager or Analyst, add a list of compensatory controls to the Compensating Controls library in the Security Exposure Management Workspace, which can be applied for the risk reduction of host vulnerable items and remediation tasks.

## Before you begin

Role required: sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin

## About this task

Some commonly used compensating controls are shipped with the base system. You can view these compensating controls by navigating to **Workspaces** &gt; **Security Exposure Management Workspace** &gt; **Lists** &gt; **Libraries** &gt; **Compensating controls**. You can activate or deactivate these compensating controls as per your requirement.

**Note:** The compensating controls feature is available for host vulnerabilities only.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  On the List page under Libraries, select **Compensating Controls**.

3.  Click **New**.

4.  On the Create Compensating Controls form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the compensating control, which appears as an option in the **Compensating controls** drop-down of the Request exception modal.|
    |Description|Brief information that provides details about the Compensating Control.|
    |Active|Status of the compensating control. Only active controls appear in the **Compensating controls** drop-down of the Request exception modal.|

5.  Select **Save**.

6.  On the Compensating Controls list under Libraries, select the desired compensating control and select **Edit**, activate or deactivate a compensating control and click **Save** to modify the compensating controls.

    All the active compensating controls appear as an option in the **Compensating controls** drop-down of the Request exception modal for risk reduction requests.


## What to do next

Starting from v21.0 of Vulnerability Response, you can associate compensating controls with CVEs or TPEs after adding a compensating controls to the library. For more information on how to associate compensating controls, see [Associate compensating controls with CVEs or TPEs for risk reduction requests](../../vr-vulnerability-manager-workspace/task/associate-controls-cve-risk-reduction.md).

-   **[Associate compensating controls with CVEs or TPEs for risk reduction requests](sem-associate-controls-cve-risk-reduction.md)**  
As a Vulnerability Manager or Analyst, you can associate relevant compensating controls with a Common Vulnerability Entry \(CVE\) or Third-party Entry \(TPE\) in the Security Exposure Management Workspace, which can be used for reducing the risk posed by a vulnerability.
-   **[Disable or enable risk reduction for a CVE or TPE](sem-disable-risk-reduction.md)**  
As a Vulnerability Manager and Analyst, you can disable or enable the risk reduction requests for the host vulnerabilities associated with a Common Vulnerability Entry \(CVE\) or Third-party Entry \(TPE\) in the Security Exposure Management Workspace.

**Parent Topic:**[Using Unified Security Exposure Management](../concept/using-unified-security-exposure-management.md)

**Related topics**  


[Understanding compensating controls for risk reduction](../../vr-vulnerability-manager-workspace/concept/compensating-controls-overview.md)

[Disable or enable risk reduction for a CVE or TPE](../../vr-vulnerability-manager-workspace/task/disable-risk-reduction.md)

[Associate compensating controls with CVEs or TPEs for risk reduction requests](../../vr-vulnerability-manager-workspace/task/associate-controls-cve-risk-reduction.md)

[Impact of the compensating controls on risk score and expiration date](../../vr-vulnerability-manager-workspace/concept/requesting-approving-risk-reduction.md)

