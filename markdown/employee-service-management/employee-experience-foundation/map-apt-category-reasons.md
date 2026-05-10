---
title: Map category and reasons to a location
description: Use the Unified Taxonomy for Employee Center to create appointment categories to group appointment reasons and map them to location queues.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Appointment Booking, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Map category and reasons to a location

Use the Unified Taxonomy for Employee Center to create appointment categories to group appointment reasons and map them to location queues.

## Before you begin

Ensure that you have created the following records:

-   Unified Taxonomy topic for Employee Center. For more information about Unified Taxonomy, see [Unified Taxonomy for Employee Center](../concept/config-taxonomy.md).
-   Walk-up location queue record that you want to map the reasons to. For more information about creating a walk-up location queue, see [Create or modify Walk-up Experience locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/walk-up-experience/configure-walkup-location.md).
-   Appointment reasons that you want to link to the location queue. For more information about creating reasons, see [Create an appointment reason](create-apt-reason.md).
-   Location consent \(communication configuration\) record that you want to link to the walk-up location queue. For more information about configuring location consent \(communication configuration\), see [Configure appointment communication](configure-appt-comms.md).

Role required: sn\_hr\_core.walkup\_admin, sn\_walkup.walkup\_manager

## Procedure

1.  Navigate to **All** &gt; **Walk-up Experience** &gt; **Administration** &gt; **Walk-up Locations**.

2.  On the Walk-up Location Queues list, select the record that you want to add the category to.

    **Note:** To display the Topic and Location consent fields, change the view to **Appointment Booking**.

    ![View options for the Walk-up Location Queue form. The Walk-up option is currently selected and the Appointment Booking option is highlighted.](../images/appt-booking-view.png)

3.  In the **Topic** field, select the taxonomy topic that you want to set as the category.

    **Note:** As an admin, you can disable the category field on the schedule appointment page by using the instance options.

4.  In the **Location consent** field, select the location consent record that you want to set for the location.

5.  Save the record.

    **Note:** The category and reasons are displayed in the application that is selected for the walk-up location record.

    The taxonomy topic and location consent are linked to the walk-up location. The topic is displayed as a category when a user wants to book an appointment.

6.  On the Reasons for Visit related list, select **New**.

    The Walk-up Reason form opens. The **Location Queue** field is automatically set to the record that you navigated from.

7.  In the **Reason** field, select the appointment reason that you want to link to the location queue.

    You can fill in the remaining fields based on your preference.

8.  Save the record.

    The reason record is created and linked to the walk-up location.


