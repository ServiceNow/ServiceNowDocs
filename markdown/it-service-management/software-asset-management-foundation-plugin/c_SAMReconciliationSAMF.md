---
title: Software Asset Management Foundation plugin software reconciliation for compliance
description: Automated license reconciliation keeps license positions accurate and up to date without manual calculations. Reconciliation runs weekly or on demand.
locale: en-US
release: yokohama
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Software Asset Management Foundation plugin, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Software Asset Management Foundation plugin software reconciliation for compliance

Automated license reconciliation keeps license positions accurate and up to date without manual calculations. Reconciliation runs weekly or on demand.

Reconciliation is a scheduled job that is run at a specified frequency \(default is weekly\). It can also be run on demand for specific or all publishers. For details on running software reconciliation in workspace, see [Run Software Asset Management Foundation plugin software reconciliation in workspace](../task/run-samf-software-recon-workspace.md). For details on running software reconciliation in the classic Software Asset Management Foundation plugin framework, see [Run Software Asset Management Foundation plugin software reconciliation in classic](../task/t_RunReconciliationSAMF.md).

When reconciliation is run, a list of reconciliation results is created that shows the compliance status of software products with respect to discovery and entitlements. Users with the sam\_user role can view reconciliation results.

Remediation options include rights not in use, rights not allocated, rights needed, reclaimable rights, and unlicensed rights.

**Parent Topic:**[Exploring Software Asset Management Foundation plugin](exploring-sam-foundation.md)

