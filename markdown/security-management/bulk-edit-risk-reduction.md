---
title: Bulk edit risk modification
description: Use bulk edit risk reduction to request an adjusted risk rating, and optionally apply compensating controls, across multiple vulnerable items that share a single vulnerability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/bulk-edit-risk-reduction.html
release: brazil
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [bulk edit, risk reduction, compensating controls, vulnerable items, Security Exposure Management]
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Bulk edit risk modification

Use bulk edit risk reduction to request an adjusted risk rating, and optionally apply compensating controls, across multiple vulnerable items that share a single vulnerability.

When you select multiple findings in the Unified Security Exposure Management, the **Bulk Edit** dialog lets you submit a risk modification request. You can change only one of the **State** or **Risk rating** fields in a single bulk edit action.

## Risk modification workflow overview

Submitting a bulk risk modification request creates a single Remediation Task for the selected items. The task enters an **In review** state and generates approval requests for risk reduction at each configured approval level. After all approvals are granted, the risk rating on the affected vulnerable items updates to the approved desired rating, and the Remediation Task transitions back to **Open** state.

If you're a Vulnerability Admin/Analyst, the change approval moves to **Approved** state immediately, and the risk rating updates and rolls up to the Remediation Task right away. If you're a Remediation Owner, the change approval request follows the configured approval process; the risk rating updates and rolls up to the Remediation Task after it's approved.

Work notes added during the bulk edit reflect the compensating controls and risk adjustments applied.

## Eligible item states

The bulk edit action applies only to items in an **Open**, **Under Investigation**, or **Awaiting Review** state. Items in other states are excluded from the update regardless of their selection status.

