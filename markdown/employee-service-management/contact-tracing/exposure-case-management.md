---
title: Managing cases to follow up with potentially exposed contacts
description: When an employee who returns to the workplace is classified as positive for a condition, such as COVID-19, the case manager creates a case to identify and follow up with potentially exposed contacts.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Managing cases to follow up with potentially exposed contacts

When an employee who returns to the workplace is classified as positive for a condition, such as COVID-19, the case manager creates a case to identify and follow up with potentially exposed contacts.

## Run the diagnostic request to identify potentially exposed contacts

The diagnostic request helps you generate a report of all on-site employees who might have been in contact with an affected employee.

If any employee is confirmed to be affected with an infectious disease, send the employee name to the case manager to create a case.

**Note:** To protect the privacy of the affected employee, you can mark a case as confidential.

## Case management process

The case manager sets up a case for an employee who might have been exposed to any infectious disease.

1.  Create a case for an affected employee.
2.  Run a diagnostic request to identify all potentially exposed contacts through various tracing systems such as workplace location, workplace shifts and reservations, meetings, employee badge swipe data, and Wi-Fi access data. For more information, see [Identify potentially exposed users](../../business-continuity/task/use-emergency-exposure-mgnt.md).
3.  Send an outreach notification to potentially exposed contacts to notify them of a potential exposure from an affected employee.
4.  Create case tasks to follow up with these potentially exposed contacts to assess their health status using predefined survey questions.

## Automated case creation

You must have the Emergency Self Report application installed for the automatic case creation to work. For more information, see [Set up Emergency Self Report](../../business-continuity/task/set-up-emergency-self-report.md#).

If an employee is reported as being in quarantine through the [self-reporting option](../../business-continuity/concept/emergency-self-report.md#section_tfx_xw5_1lb) in the Emergency Self Report application, a case is created automatically for the employee. The case is created automatically only if the employee doesn't have any active case at the time of self-reporting.

If the employee has an active case, a work note is added to the case for the case manager to take appropriate action, if needed.

The **Automated Case Creation from Employee Self Report** flow is installed with Contact Tracing. The contact tracing admin can review and configure the base system flow using the [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Automated case task creation on adding a potentially exposed contact

When a case manager adds a potentially exposed contact to a case, a case task is created automatically. By default, these case tasks are assigned to the case manager, and the case manager can assign it to a contact tracer to follow up with the employee.

**Note:** Case task creation occurs automatically only if the **sn\_imt\_tracing.auto\_create\_case\_tasks** property is set to **Yes**, the default setting.

The **Create case tasks for exposed contacts** workflow is installed with Contact Tracing. The contact tracing admin can review and modify the base system flow using the Flow Designer.

## Automated SMS outreach delivery to potentially exposed contacts

To take advantage of automatic SMS outreach delivery, you must have Virtual Agent installed and set up for use with SMS and Twilio. For more information on this feature, see [Virtual Agent conversations for Contact Tracing](contact-tracing-va-sms.md#).

When a user is added to a case task as a potentially exposed contact, they are automatically sent an SMS notification to answer questions for the Exposure Case Task Survey.

**Note:** SMS notifications are sent automatically only if the **sn\_imt\_tracing.enable\_sms\_exposure\_survey** is set to **Yes**. When disabled \(the default setting\), you can send an SMS survey while working on a case task by clicking the **Send SMS Survey** button.

## Potentially exposed contacts visualization

Contact Tracing provides interactive visualization to view the potentially exposed contacts in a case. The visualization enables case managers to quickly evaluate the contact tracing data on a single page. The potentially exposed contacts visualization includes the following options:

-   View potentially exposed contacts with the source of exposure graphically
-   Drill down to the next level of exposures to quickly identify the severity of the exposure from the affected employee
-   Create and view cases and tasks for potentially exposed contacts
-   Change the status of the investigation of potentially exposed contacts
-   Filter the view by status or source of exposure, or both

## View case metrics in ServiceNow Safe Workplace Dashboard

If you have the Safe Workplace Dashboard application installed, you can view the trends of the following data over a given time period for a campus or location:

-   Number of active cases
-   Number of potentially exposed contacts

For more information, see [Safe Workplace Dashboard](../../safe-workplace-dashboard/concept/safe-workplace-dashboard.md).

You can also configure the alert type to determine when the number of active cases is above the threshold in a particular campus or location. For more information, see [Alert types used with the Safe Workplace Dashboard](../../safe-workplace-dashboard/reference/safe-wkplc-dashboard-alert-types.md).

-   **[Create a case for an affected employee](../task/create-exposure-case.md)**  
As a case manager, create a case for an affected employee to identify and follow up with other employees who might have come in contact with the affected employee.
-   **[Identify potentially exposed contacts](../task/identify-exposed-contacts.md)**  
As a case manager, run the diagnostic request to identify other employees who might have come in contact with the affected employee.
-   **[Send notification to potentially exposed contacts in a case](../task/send-notification-to-exposed-contact.md)**  
As a case manager, send an outreach notification to potentially exposed employees to notify them of a potential exposure from an affected employee.
-   **[Create a case task to follow up with an exposed employee](../task/create-task-exposed-contact.md)**  
As a case manager, create case tasks for potentially exposed employees. Assign these tasks to contact tracers to follow up with them to evaluate their health status.
-   **[Follow up with potentially exposed contacts](../task/contact-exposed-contacts.md)**  
As a case task owner, contact potentially exposed users to follow up on their health status using the predefined instructions and survey questions.
-   **[Working on a case through contact tracing visualization](../reference/contact-tracing-case-visualization.md)**  
The contact tracing visualization in a case is a graphical representation of the affected user and potentially exposed contacts.

**Parent Topic:**[Contact Tracing](contact-tracing.md)

