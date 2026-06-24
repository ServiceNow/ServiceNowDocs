---
title: Bulk edit risk reduction
description: Use bulk edit risk reduction to request an adjusted risk rating and apply compensating controls across multiple vulnerable items that share a single vulnerability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/bulk-edit-risk-reduction.html
release: zurich
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 1
keywords: [bulk edit, risk reduction, compensating controls, vulnerable items, Security Exposure Management]
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Bulk edit risk reduction

Use bulk edit risk reduction to request an adjusted risk rating and apply compensating controls across multiple vulnerable items that share a single vulnerability.

When you select multiple findings in the Unified Security Exposure Management, the **Bulk Edit** dialog lets you submit a risk reduction request alongside a deferral request. Selecting **Mitigating Control in Place** as the reason exposes the **Request for Risk Reduction** option, where you specify the desired risk rating and the compensating controls to apply.

## Risk reduction workflow overview

Submitting a bulk risk reduction request creates a single Remediation Task for the selected items. The task enters an **In review** state and generates approval requests for both the deferral and the risk reduction at each configured approval level. After all approvals are granted, the Remediation Task transitions to **Deferred** state and the risk ratings on the affected vulnerable items are updated to the approved desired rating.

Work notes added during the bulk edit are recorded on the Remediation Task and reflect the compensating controls and risk adjustments applied.

## Eligible item states

The bulk edit action applies only to items in an **Open**, **Under Investigation**, or **Awaiting Review** state. Items in other states are excluded from the update regardless of their selection status.

**Parent Topic:**[Using bulk edit in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-using-bulk-edit.md)

