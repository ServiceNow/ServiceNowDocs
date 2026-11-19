---
title: Request risk modification for findings
description: Create a risk modification request for multiple vulnerable items at once by using the Bulk Edit dialog to specify a desired risk rating and optional compensating controls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/reduce-risk-bulk-edit.html
release: zurich
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 1
keywords: [bulk edit, risk modification, compensating controls, vulnerable items]
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Request risk modification for findings

Create a risk modification request for multiple vulnerable items at once by using the Bulk Edit dialog to specify a desired risk rating and optional compensating controls.

## Before you begin

Risk change must be enabled on the vulnerability before you can request it for the associated items.

Role required: sn\_vul.vulnerability\_admin, sn\_vul.vulnerability\_analyst or sn\_vul.remediation\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

    **Note:** The selected records must be in the **Open**, **Under Investigation**, or **Awaiting Implementation** state.

2.  On the **List** page, under Host Vulnerable items, open the **Active** or **All** list.

3.  In the list, select the check box for each vulnerable item to include in the risk modification request.

4.  Select **Bulk edit**.

5.  In the **Risk rating** field, select the target risk rating.

6.  If compensating controls apply, in the **Compensating controls** field, select the controls that mitigate the vulnerability.

7.  Select the **Modify risk until** date.

8.  In the **Work notes** field, enter a summary of the risk modification justification.

9.  Select **Submit request**.

    A Remediation Task is created for the selected items and enters an In review state. Approval requests are raised for the risk modification.


## Result

If you're a Vulnerability admin or an analyst, the state change approval \(CA\#\) is approved immediately, the risk rating updates on the selected findings right away and rolls up to the new Remediation Task.

If you're a Remediation Owner, the state change approval \(CA\#\) follows the configured approval process. After it's approved, the risk rating updates on the selected vulnerable items and rolls up to the new Remediation Task.

**Note:** The sn\_sec\_exception.modify\_risk\_approval\_required system property controls whether a Remediation Owner request requires approval. This property is set to true by default. If set to false, the change approval moves directly to **Approved** and the risk rating updates immediately for Remediation Owners too.

**Parent Topic:**[Using bulk edit in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-using-bulk-edit.md)

