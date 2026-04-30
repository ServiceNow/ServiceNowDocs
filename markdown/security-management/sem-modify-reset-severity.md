---
title: Modify the severity for a CVE or TPE
description: As a vulnerability manager or analyst, you can modify the severity level of Common Vulnerability Entry \(CVE\) or Third-party Entry \(TPE\) in the Security Exposure Management Workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Modify the severity for a CVE or TPE

As a vulnerability manager or analyst, you can modify the severity level of Common Vulnerability Entry \(CVE\) or Third-party Entry \(TPE\) in the Security Exposure Management Workspace.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management** &gt; **Lists** &gt; **Libraries**.

2.  Open the appropriate entry:

    -   **CVEs \(NVD\)**: To modify the severity of a CVE.
    -   **TPEs**: To modify the severity of a TPE.
3.  Select **Modify severity** from the **More Actions** icon ![ellipsis_icon](../../secops-analyst-workspace/image/ellipsis-icon-workspace.png)

4.  Select the new severity level from the drop-down.

5.  Provide a justification for your update.

6.  Select **Submit**.

    **Note:**

    -   You can revert to the original source severity using the **Reset Severity** option from the **More Actions** menu. This option appears only after you modify the severity.
    -   The **Modified severity** field appears only when you change the source severity. If you reset it to the original value, the field is removed.
    -   The system will use the **Modified severity** for risk calculations starting from the next scheduled job onwards. If the severity is reset, the original source severity will be applied instead.

**Parent Topic:**[Using Unified Security Exposure Management](../concept/using-unified-security-exposure-management.md)

