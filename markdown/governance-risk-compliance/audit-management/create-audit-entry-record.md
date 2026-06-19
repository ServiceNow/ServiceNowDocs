---
title: Create an audit entry record
description: Create audit entry records to track third-line audit objects in the Audit Workspace. Audit entry records are read-only after the first save and are hidden from second-line users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/create-audit-entry-record.html
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 1
keywords: [audit entry, third-line record, create]
breadcrumb: [Audit entry for GRC objects, Exploring Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# Create an audit entry record

Create audit entry records to track third-line audit objects in the Audit Workspace. Audit entry records are read-only after the first save and are hidden from second-line users.

## Before you begin

Role required: sn\_audit\_ws.third\_line\_manager

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Select the list icon \[Omitted image "list-icon-mrm.png"\] Alt text:.

3.  Navigate to the list for the object you're creating.

    The **Audit entry** field is available on Entity, Engagement, Control, Control objective, Risk, and Risk statement.

4.  Select **New**.

    The **Audit entry** check box is selected by default for all new records. \[Omitted image "audit-entry-checkbox.png"\] Alt text: Create new Risk form in Audit Workspace with the Audit entry check box selected.

5.  Clear the **Audit entry** check box before saving to create a second-line record instead.

    Clearing the check box also removes the third-line restrictions described in the validation rules.

6.  Complete the remaining required fields for the object.

    For risk statements and control objectives, the **Parent** field accepts both second-line and third-line records. A second-line record cannot have a third-line parent, and an error appears when you save.

    For risks, if the **Inherit from risk statement** check box is selected and both the risk statement and entity are second-line records, the record fails to save.

7.  Select **Save**.

    An informational message at the top of the form confirms that the record is a third-line record. The **Audit entry** field is set to read-only after this first save and cannot be changed.


## What to do next

Third-line records are hidden from second-line users. Third-line risks and their associated risk statements and entities are excluded from the risk and compliance score roll-up calculation.

**Parent Topic:**[Audit entry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/audit-entry-overview.md)

