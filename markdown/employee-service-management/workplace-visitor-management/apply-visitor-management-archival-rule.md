---
title: Apply visitor management archive policy
description: Apply the archival policy for Workplace Visitor Management. The archival policy will archive old visitor records and visitor registration records that are more than one year old.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-visitor-management/apply-visitor-management-archival-rule.html
release: australia
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Apply visitor management archive policy

Apply the archival policy for Workplace Visitor Management. The archival policy will archive old visitor records and visitor registration records that are more than one year old.

## Before you begin

The archival policy improves performance and controls table size growth by archiving old data.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.

2.  In the Archival Rules search box, filter by **WSD**.

    WSD \(Workplace Service Delivery\).

3.  Select and click open the following visitor management archival rules in edit mode as required:

    -   **WSD: Archive 1 year old Visit record**: Archives one-year old visitor records for the past one year in Workplace Visitor Management.
    -   **WSD: Archive 1 year old Visit registration**: Archives one-year old visitor registration records in Workplace Visitor Management.
4.  Select the **Active** check box to activate the archival policy for a selected table.

5.  Apply the required filter conditions.

6.  Select **Recalculate Estimate** to know the records eligible for archiving.

7.  Select **Run Archive Now** under related links to run the archival rule.


**Parent Topic:**[Managing visitor registrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-visitor-management/manage-visitor-registrations.md)

**Related topics**  


[Use the receptionist portal]()

[Update a visitor registration]()

[View visitor registrations]()

[View visitor policy confirmations]()

[Visitor registration states]()

[Anonymize a visitor]()

