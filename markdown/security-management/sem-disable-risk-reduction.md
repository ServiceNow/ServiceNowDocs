---
title: Disable or enable risk reduction for a CVE or TPE
description: As a Vulnerability Manager and Analyst, you can disable or enable the risk reduction requests for the host vulnerabilities associated with a Common Vulnerability Entry \(CVE\) or Third-party Entry \(TPE\) in the Security Exposure Management Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Add a compensating control to the library, Use, Unified Security Exposure Management, Security Operations]
---

# Disable or enable risk reduction for a CVE or TPE

As a Vulnerability Manager and Analyst, you can disable or enable the risk reduction requests for the host vulnerabilities associated with a Common Vulnerability Entry \(CVE\) or Third-party Entry \(TPE\) in the Security Exposure Management Workspace.

## Before you begin

Role required: admin

## About this task

The risk reduction for a CVE and TPE is enabled by default.

**Note:** The compensating controls feature is available for host vulnerabilities only.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

    On the Lists page, under Libraries, open one of the following for which you want to disable the risk reduction requests:

    -   **CVE** from the CVEs list.
    -   **TPEs** from the TPEs list.
2.  Select **Disable risk reduction**.

    The remediation owner can’t request risk reduction for the host vulnerable items related to this CVE or TPE. In other words, the [Request for Risk Reduction](../../vr-it-remediation-workspace/reference/itr-ws-request-exception-form-rr.md#entry-risk-reduction) check box doesn’t appear when the **Reason** is selected as `Mitigating Control in Place` on the Request Exception modal.

3.  To enable the risk reduction requests for host vulnerable items, select **Enable risk reduction**.


**Related topics**  


[Understanding compensating controls for risk change](../../vr-vulnerability-manager-workspace/concept/compensating-controls-overview.md)

[Add a compensating control to the library](../../vr-vulnerability-manager-workspace/task/create-compensatory-control.md)

[Associate compensating controls with CVEs or TPEs for risk change requests](../../vr-vulnerability-manager-workspace/task/associate-controls-cve-risk-reduction.md)

[Impact of the compensating controls on risk score and expiration date](../../vr-vulnerability-manager-workspace/concept/requesting-approving-risk-reduction.md)

