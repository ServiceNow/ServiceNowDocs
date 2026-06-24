---
title: Request risk reduction for findings
description: Create a risk reduction request for multiple vulnerable items at once by using the Bulk Edit dialog to specify a desired risk rating and compensating controls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/reduce-risk-bulk-edit.html
release: zurich
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 1
keywords: [bulk edit, risk reduction, compensating controls, vulnerable items]
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Request risk reduction for findings

Create a risk reduction request for multiple vulnerable items at once by using the Bulk Edit dialog to specify a desired risk rating and compensating controls.

## Before you begin

All vulnerable items you plan to select must map to the same vulnerability. Risk reduction is not available when items from multiple different vulnerabilities are selected.

Risk reduction must be enabled on the vulnerability before you can request it for the associated items.

Role required:

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

    **Note:** The selected records must be in the **Open**, **Under Investigation**, or **Awaiting Implementation** state.

2.  On the List page, under Host Vulnerable items, open the **Active** or **All** list.

3.  In the list, select the check box for each vulnerable item to include in the risk reduction request.

4.  Select **Bulk edit**.

5.  In the Bulk Edit dialog, in the **Deferred** section, select **Mitigating Control in Place** as the reason.

6.  Select the **Request for Risk Reduction** check box.

7.  Select the **Request for Deferral** check box to also submit a deferral alongside the risk reduction request.

8.  In the **Desired risk rating** field, select the target risk rating.

9.  In the **Compensating controls** field, select the controls that mitigate the vulnerability.

10. In the **Short description** field, enter a summary of the risk reduction justification.

11. In the **Work notes** field, enter supporting details.

12. Select **Update**.

    A Remediation Task is created for the selected items and enters an **In review** state. Approval requests are raised for the risk reduction and, if selected, for the deferral.


## What to do next

Approvers at each configured level must approve the risk reduction and deferral requests. After all approvals are complete, the Remediation Task transitions to **Deferred** state and the risk ratings on the affected items are updated to reflect the approved desired rating.

**Parent Topic:**[Using bulk edit in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-using-bulk-edit.md)

