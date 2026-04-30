---
title: Approval workflow configurations for unassign request
description: You can design the approval workflow for the removal of assignments from vulnerable items \(VIs, VITs\), remediation tasks, application vulnerable items \(AVITs\), and container vulnerable items \(CVITs\) for you and your group.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Approval workflow configurations for unassign request

You can design the approval workflow for the removal of assignments from vulnerable items \(VIs, VITs\), remediation tasks, application vulnerable items \(AVITs\), and container vulnerable items \(CVITs\) for you and your group.

VIT, remediation task, AVIT, and CVIT have a default approval rule each. Each approval rule has a default approval configuration. Each approval configuration has a default approver level. The approval rules for VITs, remediation task, AVIT, and CVIT are enabled by default. As an admin, you can perform the following actions by navigating to **All** &gt; **Vulnerability Response** &gt; **My Approvals** &gt; **Approval Rules** and selecting the appropriate approval rule.

-   enable or disable an approval rule.
-   create and update an approval configuration.
-   define conditions for vulnerable items and remediation tasks for which the approval rules apply.
-   create and update multiple approver levels.

The following table shows the default approval rules, approval configurations, and approver levels for a VIT, remediation task, AVIT, and CVIT which are shipped with the base system.

|Type|Approval Rule|Approval configuration|Approver levels|
|----|-------------|----------------------|---------------|
|VIT or VI|Vulnerable item field change request|Vulnerable item field change request|Level-1 Unassign Request for VI|
|Remediation task|Vulnerability Group field change request|Vulnerability field change request|Level 1 - Unassign Request for VG|
|AVIT|Application vulnerable item field change request|Application vulnerability field change request|Unassign app vulnerability item|
|CVIT|Approval for container management|Default Configuration Unassign CVIT|CVIT unassign approval level - 1|

For more information on how to approve unassign requests, see [Approve or reject an unassign request in Vulnerability Response](../../vulnerability-response/task/vr-approve-unassign-requests.md).

