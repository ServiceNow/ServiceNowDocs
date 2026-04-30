---
title: Create a case for an affected employee
description: As a case manager, create a case for an affected employee to identify and follow up with other employees who might have come in contact with the affected employee.
locale: en-US
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Managing cases to follow up with potentially exposed contacts, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create a case for an affected employee

As a case manager, create a case for an affected employee to identify and follow up with other employees who might have come in contact with the affected employee.

## Before you begin

Role required: sn\_imt\_tracing.case\_manager

## About this task

**Important:** There can be only one active case for an affected employee. You can create a new case for the same employee only if the active case is closed or cancelled.

If the [Emergency Self Report](../../business-continuity/task/set-up-emergency-self-report.md#) application is installed and an employee is reported being in quarantine through the [self-reporting option](../../business-continuity/concept/emergency-self-report.md#section_tfx_xw5_1lb), the system automatically creates a case. If an active case exists for the employee at the time of reporting, a work note is added to that case.

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Case Management** &gt; **Create New Case**.

2.  On the form, fill in the fields.

<table id="table_k4m_3mp_ylb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reported person

</td><td>

Name of the affected employee.

</td></tr><tr><td>

Location

</td><td>

Location of the affected employee.

</td></tr><tr><td>

Date reported

</td><td>

The date on which the person was reported to be affected.

</td></tr><tr><td>

Reported source

</td><td>

Source from which the employee was reported to be affected, such as through health screening, self-reporting, or location.

</td></tr><tr><td>

Case manager

</td><td>

User assigned to work on the case. Users who have the sn\_imt\_tracing.case\_manager role are listed.

**Note:** If a case was automatically created when the employee self-reported as being in quarantine, the case manager field is empty. Case managers can assign the case to themselves or to any other case manager. Only the assigned case manager can work on the case.

</td></tr><tr><td>

Case state

</td><td>

Current state of the case.

</td></tr><tr><td>

Case start date

</td><td>

The date on which the case is created.

</td></tr><tr><td>

Case end date

</td><td>

The date on which the case is closed.

</td></tr><tr><td>

Watch list

</td><td>

Other users who need to know about the status of the case.

</td></tr><tr><td>

Confidential

</td><td>

Option for keeping the case confidential to protect the privacy of the affected user.A confidential case can be accessed only by the case manager and users added in the **Watch list** field.

</td></tr></tbody>
</table>3.  Click **Submit**.


## Result

A case for the affected employee is created. If notifications are enabled, the case manager assigned to the case is notified via email.

An exposed contact record is created for the reported person with the default health status set to Infected.

The Exposed contacts visualization section appears.

The following related lists appear in the case:

-   Diagnostics Requests: Used to request a diagnostic report to identify all impacted employees.
-   Exposed Contacts: Potentially exposed contacts to follow up with about their health status.
-   Case Tasks: The tasks created for each potentially exposed contact to track the follow-up.
-   Notes: Notes containing the names of individuals submitted in the daily contact logs by the affected employee during the period specified for the case. If the end date is not specified in the case, all daily log notes submitted by the affected employee after the case start date are listed.

## What to do next

[Run the diagnostic request](identify-exposed-contacts.md) to identify all potentially exposed employees and add them to the case for follow-ups.

You can also add potentially exposed contacts to the case manually from the Exposed Contacts related list.

If you have the [Safe Workplace Dashboard](../../safe-workplace-dashboard/concept/using-safe-wkplc-dashboard.md) application installed, you can view a trend of active cases and potentially exposed contacts over a given time period for a campus or location on the dashboard.

**Parent Topic:**[Managing cases to follow up with potentially exposed contacts](../concept/exposure-case-management.md)

