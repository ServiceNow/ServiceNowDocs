---
title: Disable or enable risk reduction for a CVE or TPE
description: As a Vulnerability Manager and Analyst, you can disable or enable the risk reduction requests for the host vulnerabilities associated with a Common Vulnerability Entry \(CVE\) or Third-party Entry \(TPE\) in the Security Exposure Management Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-disable-risk-reduction.html
release: australia
topic_type: task
last_updated: "2026-03-12"
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

    The remediation owner can’t request risk reduction for the host vulnerable items related to this CVE or TPE. In other words, the [Request for Risk Reduction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/it-remediation-workspace/itr-ws-request-exception-form-rr.md) check box doesn’t appear when the **Reason** is selected as `Mitigating Control in Place` on the Request Exception modal.

3.  To enable the risk reduction requests for host vulnerable items, select **Enable risk reduction**.


**Parent Topic:**[Add a compensating control to the library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-create-compensatory-control.md)

**Related topics**  


[Understanding compensating controls for risk reduction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-manager-workspace/compensating-controls-overview.md)

[Add a compensating control to the library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-manager-workspace/create-compensatory-control.md)

[Associate compensating controls with CVEs or TPEs for risk reduction requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-manager-workspace/associate-controls-cve-risk-reduction.md)

[Impact of the compensating controls on risk score and expiration date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-manager-workspace/requesting-approving-risk-reduction.md)

