---
title: Using bulk edit in the Security Exposure Management Workspace
description: Bulk edit in the Security Exposure Management Workspace enables you to update the state, request exceptions and false positives, and assign multiple findings to an assignment group simultaneously.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/sem-using-bulk-edit.html
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
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

-   **[Update the state of records in bulk in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/sem-bulk-edit-update-state.md)**  
Update the state of multiple findings concurrently according to their remediation progress using the bulk edit feature in the Security Exposure Management Workspace.
-   **[Bulk edit host vulnerable items with patches and solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/sem-bulk-edit-patches-solutions.md)**  
Recommend a patch or solution for multiple host vulnerable items concurrently using the bulk edit feature in the Security Exposure Management Workspace.
-   **[Assign records to an assignment group in bulk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/sem-bulk-edit-assign.md)**  
Assign multiple records findings concurrently to an assignment group using the bulk edit feature in the Security Exposure Management Workspace.
-   **[Remove assignments for host vulnerable items in bulk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/sem-bulk-edit-unassign.md)**  
Remove yourself or your groups from the  **Assigned to ** and  **Assignment group ** fields on the findings if you determine that the records aren’t within your scope for remediation, or if you think that records have been incorrectly assigned to you or to your groups.
-   **[Request bulk exception in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/sem-bulk-edit-request-exception.md)**  
Request an exception for multiple findings concurrently using the bulk edit feature instead of manually selecting each record.
-   **[Bulk edit risk reduction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/bulk-edit-risk-reduction.md)**  
Use bulk edit risk reduction to request an adjusted risk rating and apply compensating controls across multiple vulnerable items that share a single vulnerability.
-   **[Bulk edit risk reduction restrictions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/bulk-edit-risk-restrictions.md)**  
Risk reduction in the Bulk Edit dialog is restricted in specific scenarios based on the vulnerabilities mapped to the selected items and the vulnerability configuration.
-   **[Request risk reduction for findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/reduce-risk-bulk-edit.md)**  
Create a risk reduction request for multiple vulnerable items at once by using the Bulk Edit dialog to specify a desired risk rating and compensating controls.
-   **[Bulk edit for false positive in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/sem-bulk-edit-request-false-positive.md)**  
Mark one or more records \(VITs, AVITs, CVITs, or TRs\) as false positive concurrently using the bulk edit feature from the Security Exposure Management Workspace instead of manually selecting each item.
-   **[Close records in bulk in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/sem-bulk-edit-close-records.md)**  
Close multiple records \(VITs, AVITs, or CVITs\) concurrently using the bulk edit feature in the Security Exposure Management Workspace.

**Parent Topic:**[Bulk edit in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/sem-workspace-bulk-edit-overview.md)

