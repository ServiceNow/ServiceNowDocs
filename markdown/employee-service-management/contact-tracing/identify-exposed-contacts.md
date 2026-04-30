---
title: Identify potentially exposed contacts
description: As a case manager, run the diagnostic request to identify other employees who might have come in contact with the affected employee.
locale: en-US
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Managing cases to follow up with potentially exposed contacts, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Identify potentially exposed contacts

As a case manager, run the diagnostic request to identify other employees who might have come in contact with the affected employee.

## Before you begin

The diagnostic request function is available in the Emergency Exposure Management application. Ensure that you have the Emergency Exposure Management application installed.

Role required: sn\_imt\_tracing.case\_manager

## About this task

**Note:** You cannot create or run a diagnostic request for affected employees who have not consented to use their data for contact tracing. For more information, see [User privacy consent for Contact Tracing](../concept/contact-tracing-user-privacy.md).

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Case Management** &gt; **Cases Assigned to Me**.

2.  Open a case from the list of assigned cases.

3.  If the case is newly assigned to you, click **Start Work**.

    The state of the case updates to Work in Progress.

4.  In the Diagnostic Requests related list, click **New**.

    The details of the affected user are pre-populated in the respective fields from the case record.

5.  On the Diagnostic Request form, run the diagnostic request on the affected employee to identify other potentially exposed employees, and add them to the case.

    1.  Select one or more tracing systems and a date range.

    2.  Click **Save**.

    3.  Click **Run Diagnostics**.

        The potentially exposed employees, based on the selected tracing systems, are listed in the All Impacted Users related list on the Diagnostic Request form.

    4.  Select users from the All Impacted Users related list and select the **Add Users to Case** option in the Actions on selected rows list.

    For more information on running a diagnostic request, see [Run a diagnostic request](../../business-continuity/task/use-emergency-exposure-mgnt.md).

6.  If you know of other employees in addition to employees identified from the diagnostics, click **New** in the Exposed Contacts list and add them as potentially exposed contacts.


## Result

The selected users from the All Impacted Users related list on the Diagnostic Request form are added to the Exposed Contacts related list on the Case form.

If automatic case task creation is enabled by the **sn\_imt\_tracing.auto\_create\_case\_tasks** system property setting, a case task is created for each potentially exposed contact added to the case. These automatically created case tasks are assigned to the case manager by default. From the Case Tasks related list, the case manager can assign them to a contact tracer.

**Note:** If a potentially exposed employee added to the case has an active case, the health status of the employee in the current exposed contact record is automatically set from the corresponding exposed contact record of the active case.

These potentially exposed contacts also appear in the exposed contacts visualization section. For more information, see [Working on a case through contact tracing visualization](../reference/contact-tracing-case-visualization.md).

If you have the [Employee Readiness Core](../../employee-readiness-core/concept/employee-readiness-core.md) application installed and a health and safety requirement for the potentially exposed contacts activated, a record is created with the requirement status as Not Cleared for these potentially exposed employees.

## What to do next

[Send notification to potentially exposed contacts in a case](send-notification-to-exposed-contact.md).

If the automatic case task creation is disabled, [create a case task for each exposed contact](create-task-exposed-contact.md).

**Parent Topic:**[Managing cases to follow up with potentially exposed contacts](../concept/exposure-case-management.md)

