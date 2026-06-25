---
title: Configure calendar sections on the Presence dashboard
description: As an admin, add or remove calendar sections from the Presence dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-concierge/configure-presence-dashboard-sections.html
release: australia
product: Workplace Concierge
classification: workplace-concierge
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Workplace Concierge, Workplace Service Delivery, Employee Service Management]
---

# Configure calendar sections on the Presence dashboard

As an admin, add or remove calendar sections from the Presence dashboard.

## Before you begin

Role required: sn\_wsd\_concierge.admin

## Procedure

1.  Navigate to **All** &gt; **Employee Presence** &gt; **Calendar Sections**.

    The default calendar sections are as follows:

    -   WSD Presence Collaboration Section
    -   WSD Presence Exception Section
    -   WSD Presence Insights Section
    -   WSD Presence Reservation Section
    **Note:**

    -   The WSD Insights Section is available if you've installed [Proactive Prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/proactive-prompts/proactive-prompts-for-hrsd.md).
    -   The WSD Presence Reservation Section is available if you've installed [Workplace Reservation Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/workplace-rsv-mgmt-feat.md).
2.  Change the section order of appearance by editing the values in the Order column.

3.  Add a section to the calendar.

    **Important:** Adding a widget that is not optimized for the Presence Dashboard can lead to unexpected results in the UI. If you want to create a widget, make sure that you copy and modify a default widget.

    1.  From the Employee Presence Calendar Widgets table, select **New**.

    2.  On the Employee Presence Calendar Widget form, fill in the fields.

        For a description of the field values, see [Employee Presence Calendar Widget form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-concierge/presence-calendar-widget-frm.md).

    3.  Select **Submit**.


**Parent Topic:**[Configure Workplace Concierge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-concierge/configure-workplace-concierge.md)

**Related topics**  


[Install Workplace Concierge]()

[Configure workplace space suggestions for employees]()

