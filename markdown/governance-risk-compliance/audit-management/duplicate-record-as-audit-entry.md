---
title: Duplicate a second-line record as an audit entry
description: Use the Duplicate as audit entry action to copy a second-line control, control objective, risk, or risk statement into a new third-line record. Each source record can be duplicated only once.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/duplicate-record-as-audit-entry.html
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 1
keywords: [duplicate, audit entry, audit entry source]
breadcrumb: [Audit entry for GRC objects, Exploring Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# Duplicate a second-line record as an audit entry

Use the **Duplicate as audit entry** action to copy a second-line control, control objective, risk, or risk statement into a new third-line record. Each source record can be duplicated only once.

## Before you begin

The source record must be a second-line record. The action is hidden on third-line records. The action is available on the following four objects only:

-   Control objective
-   Control
-   Risk statement
-   Risk

**Note:** If a third-line manager opens the original second-line record and selects **Duplicate as audit entry**, an error indicates that the record cannot be duplicated again. A source record can be duplicated only once and cannot be converted again to second line.

Role required: sn\_audit\_ws.third\_line\_manager

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Select the list icon \[Omitted image "list-icon-mrm.png"\] Alt text:.

3.  Open the second-line record to duplicate.

4.  From the More actions \[Omitted image "more-actions-new.png"\] Alt text: menu, select **Duplicate as audit entry**.

    A new record opens with the same field values as the source record. The **Name** field is prefixed with Copy followed by the source record name. For example, a copy of Loss of Confidentiality opens as Copy Loss of Confidentiality.\[Omitted image "duplicate-as-audit-entry.png"\] Alt text: Duplicate as audit entry option on the record page.

5.  Adjust any field values that should differ from the source record.

6.  Select **Save**.

    The new record is created as a third-line record and is stored as a copy of the source record. It retains a reference to the original record in the **Audit entry source** field, located under the **Audit entry** check box.


**Parent Topic:**[Audit entry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/audit-entry-overview.md)

