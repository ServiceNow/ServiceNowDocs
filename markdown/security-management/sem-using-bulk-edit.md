---
title: Using bulk edit in the Security Exposure Management Workspace
description: Bulk edit in the Security Exposure Management Workspace enables you to update the state, request exceptions and false positives, and assign multiple findings to an assignment group simultaneously.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-using-bulk-edit.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Using bulk edit in the Security Exposure Management Workspace

Bulk edit in the Security Exposure Management Workspace enables you to update the state, request exceptions and false positives, and assign multiple findings to an assignment group simultaneously.

The bulk edit feature is available for:

-   Host vulnerable items \(VITs\) starting with v21.0 of Vulnerability Response.
-   Application vulnerable items \(AVITs\) and Container vulnerable items \(CVITs\) starting with v22.0 of Vulnerability Response.
-   Test results starting with v23.0 of Vulnerability Response.

When you run a bulk edit job, not every selected record is updated. A record is excluded if it meets any of the following conditions.

|Condition|Applies to|Reason|
|---------|----------|------|
|No matched CI|VIT, AVIT, CVIT, Test results|Record is not associated with a valid CI.|
|CI is **Retired**|All record types|Applies only when Auto close is enabled. Retired CIs aren't modified.|
|Substate = **Invalid**|VIT, Test results|Records with an invalid substate aren't processed.|
|Substate = **CI Decommissioned**|VIT, Test results|Applies only when Auto close is enabled.|

