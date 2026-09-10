---
title: TRM technical debt states and transitions
description: A TRM technical debt record persists across scheduled job runs and moves between Active, Resolved, and Archived states instead of being deleted and re-created.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-trm-technical-debt-states.html
release: australia
topic_type: reference
last_updated: "2026-08-24"
reading_time_minutes: 2
keywords: [technical debt, state]
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# TRM technical debt states and transitions

A TRM technical debt record persists across scheduled job runs and moves between Active, Resolved, and Archived states instead of being deleted and re-created.

This functionality requires Enterprise Architecture Workspace version 10.0.0 or later and TPM plugin \(sn\_apm\_tpm\) version 1.12.0 or later.

## Technical debt states

Each TRM technical debt record has a **State** field that shows one of the following states.

|State|Description|
|-----|-----------|
|**Active**|Technical debt that is active and needs attention. This is the default state when a technical debt record is first created.|
|**Resolved**|Active technical debt that no longer applies because the underlying discovered technology is still in use but no longer violates a TRM standard.|
|**Archived**|Technical debt for which the underlying discovered technology no longer exists in the TPM Discovered Technology \[sn\_apm\_tpm\_discovered\_technology\] table \(typically because the server association was removed\). Alternatively, the reason associated with the active debt is disabled in the technical debt configuration.|

## State transitions

The **Populate TRM technical debts in the EA Workspace** scheduled job evaluates every technical debt record on each run and moves it to a new state based on the following rules. The record is never deleted; only its state, reason, and **Updated** timestamp change.

|From state|To state|Trigger|
|----------|--------|-------|
|**Active**|**Resolved**|The debt is resolved: the discovered technology still exists, but it no longer violates a TRM standard.|
|**Active**|**Archived**|The underlying discovered technology is removed, or the reason associated with the active debt is disabled in the technical debt configuration.|
|**Archived**|**Active**|The discovered technology is created again, or the reason associated with the archived debt is re-enabled in the technical debt configuration.|
|**Resolved**|No transition|A resolved technical debt record never moves to **Active** or **Archived**. If the same debt condition occurs again, the system creates a new technical debt record in the **Active** state instead of reopening the resolved one.|

**Note:**

A **Resolved** record is terminal. The **Created** timestamp on a new record reflects when that new record was created, not the original detection date of the resolved record it replaced.

**Parent Topic:**[Enterprise Architecture Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-reference.md)

**Related topics**  


[TRM technical debt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-manage-trm-technical-debt.md)

[Technical debt calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-calc.md)

[TRM technical debt form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-form.md)

[Update TRM technical debt data using scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-job-trm-tech-debts.md)

[Exploring the Technology Reference Model in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-managing-the-technology-portfolio.md)

