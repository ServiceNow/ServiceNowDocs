---
title: Audit entry
description: The audit entry field marks a record as third-line, restricting its visibility to users who hold the third-line manager role. Third-line records are excluded from the views and calculations that second-line users rely on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/audit-entry-overview.html
release: australia
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2026-05-29"
reading_time_minutes: 2
keywords: [audit entry, third line, second line, audit workspace]
breadcrumb: [Exploring Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# Audit entry

The audit entry field marks a record as third-line, restricting its visibility to users who hold the third-line manager role. Third-line records are excluded from the views and calculations that second-line users rely on.

Audit entry is a field added to six GRC objects that enables third-line managers to distinguish audit-only records that other GRC users work with daily. Selecting the audit entry check box marks the record as third-line and hides it from second-line users.

## Objects where the audit entry field appears

The audit entry field is available on the following objects.

|Object|Source application|
|------|------------------|
|Control|Policy and Compliance Management|
|Control objective|Policy and Compliance Management|
|Entity|GRC Core|
|Engagement|Audit Management|
|Risk|Risk Management|
|Risk statement|Risk Management|

The state of the audit entry check box determines whether a record is treated as third-line or second-line.

-   When audit entry is selected, the record is a third-line record. Only users with the sn\_audit\_ws.third\_line\_manager role can view or modify the record from the Audit Workspace.
-   When audit entry is cleared, the record is a second-line record. The record behaves the same as records created before this feature was introduced, and is visible to second-line users with the corresponding compliance or risk role.

After a record is saved, the audit entry field is locked and can't be changed.

## Impact on risk score roll-up

Third-line entities, third-line risk statements, and third-line risks are excluded from the risk score roll-up calculation. This exclusion helps avoid third-line records from changing the assessment scores that second-line users see on second-line risks.

## Impact on compliance score roll-up

Third-line control objectives and third-line controls are excluded from the compliance score roll-up calculation. This exclusion helps avoid third-line records from changing the compliance scores that second-line users see on second-line controls.

-   **[Create an audit entry record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/create-audit-entry-record.md)**  
Create audit entry records to track third-line audit objects in the Audit Workspace. Audit entry records are read-only after the first save and are hidden from second-line users.
-   **[Duplicate a second-line record as an audit entry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/duplicate-record-as-audit-entry.md)**  
Use the **Duplicate as audit entry** action to copy a second-line control, control objective, risk, or risk statement into a new third-line record. Each source record can be duplicated only once.

**Parent Topic:**[Exploring Audit Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/audit-management.md)

