---
title: Use ITSM Employee Slate for Moveworks
description: View active outages and degradations for your services using the Service Health Broadcast widget. Ask Otto for a summary of current issues. Use the Tech Lounge widget to check in for walk-in help or book appointments. You can also check in conversationally by chatting with Otto.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/use-employee-works-itsm.html
release: australia
topic_type: task
last_updated: "2026-08-13"
reading_time_minutes: 3
breadcrumb: [ITSM Employee Slate for Moveworks, IT Service Management]
---

# Use ITSM Employee Slate for Moveworks

View active outages and degradations for your services using the Service Health Broadcast widget. Ask Otto for a summary of current issues. Use the Tech Lounge widget to check in for walk-in help or book appointments. You can also check in conversationally by chatting with Otto.

## Before you begin

Role required: none

## Service health status values

The following status values classify entries in the Service Health Broadcast widget, the All services page, and the service detail page.

|Status|Description|
|------|-----------|
|Outage|The service is completely unavailable.|
|Degraded|The service is available but performing below normal.|
|Under maintenance|Maintenance is scheduled or in progress for the service.|
|Operational|The service has no active outage, degradation, or maintenance.|

## Procedure

1.  Navigate to the ITSM Employee Slate for Moveworks homepage.\[Omitted image "employeeworks-landing-page.png"\] Alt text: ITSM Employee Slate for Moveworks landing page

    The Service Health Broadcast banner shows active outages, active maintenance, and degradations at the highest business criticality tier and displays for all users. The banner only displays the three most recently updated events.

2.  Select **View details**.\[Omitted image "employeeworks-all-services.png"\] Alt text: All services for ITSM Employee Slate for Moveworks that has the Service health and Scheduled maintenance tabs

    The **All services** page displays the service status for outages, degradations, the ones under maintenance, and the operational status for the services.

3.  Select a service to drill down into the details for ITSM Employee Slate for Moveworks.

    \[Omitted image "employeeworks-service-details.png"\] Alt text: Drilldown into a service in ITSM Employee Slate for Moveworks

4.  From the Servicehealth banner in the ITSM Employee Slate for Moveworks homepage, select **Ask Otto** to open a chat that automatically summarizes active outages for services you can access.

    **Note:** Make sure the Outage lookup plugin is installed to view the Ask Otto conversations.

    \[Omitted image "employeeworks-ask-otto.png"\] Alt text: Ask Otto chat in ITSM Employee Slate for Moveworks

5.  Add the **Tech lounge** quick link to the ITSM Employee Slate for Moveworks homepage.

    For more information, see [Configure EmployeeWorks Web App](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/empworks-configure-employee-slate-moveworks.md).

6.  From the homepage, select the **Tech lounge** quick link.

    The Tech lounge page shows your selected location, its hours of operation, and the current walk-in queue.

7.  Select **Change location** to pick a different Tech lounge location.

    Hours of operation and the walk-in queue are specific to each location. The location you select is remembered for your next visit.

8.  To check in for walk-in help, select a reason for your visit and describe what you need help with, then select **Next**.

    A description of your issue is required before you can check in. As you type, Otto suggests knowledge articles and a generated answer that match your description — reviewing these may resolve your issue without a walk-in visit.

    **Note:** Otto is an AI agent. Answers it generates may not always be accurate. Review AI-generated content before acting on it.

9.  After you check in, view your position in the queue and your estimated wait time on the confirmation screen.

    The queue count and wait time update automatically as employees check in and are helped, without requiring a page refresh.

10. To schedule a visit instead of walking in, select **Book appointment**, choose an in-person or remote appointment, then select a date and an available time slot.

    Available time slots reflect the Tech lounge location's configured hours and existing appointment load. From the confirmation screen, you can add the appointment to your calendar, edit the appointment details, or cancel it.

11. To start a Tech lounge visit conversationally instead, use Otto to visit the tech lounge you need help with.

    \[Omitted image "employeeworks-visit-lounge.png"\] Alt text: EmployeeWorks Visit Lounge

    Otto routes the named request into the same walk-up flow.

12. Confirm your walk-in check-in within the conversation.

    \[Omitted image "employeeworks-confirm-booking.png"\] Alt text: EmployeeWorks Confirm Booking

    Otto checks you in to the walk-in queue for the tech lounge location without leaving the chat.

    **Note:** Using Otto, you can also conversationally check-in for walk-in help, book an appointment, and also get the current position in the queue and cancel them if needed.


