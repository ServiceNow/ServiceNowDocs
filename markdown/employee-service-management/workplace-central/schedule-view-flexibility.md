---
title: Schedule view flexibility
description: Event planners and space planners can organize, view, and manage events across multiple spaces and time zones using the Event planner Schedule view tab.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/workplace-central/schedule-view-flexibility.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 2
breadcrumb: [Working with schedule view, Working with Event planner, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Schedule view flexibility

Event planners and space planners can organize, view, and manage events across multiple spaces and time zones using the Event planner **Schedule view** tab.

The following configuration options are available on the **Schedule view** tab:

-   **Time zone selection**

    View and manage events in different time zones. You can select the time zone based on the buildings returned by the filter. When you apply a filter, the **Schedule view** tab displays the relevant time zones for all qualified spaces. You can select a time zone, such as Europe/Amsterdam or VST, to view events in that time zone.\[Omitted image "wsd-time-zone-selection.png"\] Alt text: Time zone selection on the Schedule view tab.

-   **Row title configuration**

    Configure which fields from the space table are displayed as row titles in the Schedule view by setting the **sn\_wsd\_rsv.row\_title\_fields\_event\_planner\_schedule** system property.

-   **Event card configuration**

    Select which fields from the reservation table are shown on the event card by configuring the **sn\_wsd\_rsv.event\_body\_fields\_event\_planner\_schedule** system property.

-   **Additional details in the side panel**

    Configure which additional space details fields appear in the space details panel by using the **sn\_wsd\_rsv.additional\_space\_details\_fields** system property.

    **Note:** Images can’t be displayed directly in additional details. If you enter a field name for an image, the system shows the attachment ID instead of the actual image.

-   **Page size**

    The **sn\_wsd\_rsv.page\_size\_event\_planner\_schedule** system property determines the default page size for the event planner Schedule view. The default value is 20. Modifying this property can affect the page’s load performance.

-   **Zoom in and zoom out space details**

    Adjust the time scale and visual density of the schedule grid using the zoom in and zoom out feature. The default view is set to 100%.

-   **Multiple time zone settings**

    View reservation details in specific time zones alongside the default time zone. Select the settings icon \[Omitted image "system-settings-icon.png"\] Alt text: and choose a time zone from the available options to update all event times in the Schedule view accordingly.

-   **Event editing in the selected time zone**

    You can drag or stretch events to change their time or duration. Changes are applied according to the currently selected time zone. A Confirm reservation changes dialog box appears so that you can confirm the changes. You can also change the event time in the side panel, and the changes are applied according to the selected time zone.

-   **Multiple time zone display**

    You can view multiple time zones in the event planner’s Schedule view, with all times shown in a 24-hour format. To configure additional time zones:

    -   Select the settings icon in the Schedule view.
    -   Add up to three additional time zones alongside your default time zone.
    -   The selected time zones appear in the Schedule view, enabling you to coordinate events across different regions.\[Omitted image "wsd-timezone-settings.png"\] Alt text: Multiple time zone settings appear on the page when you select Settings.
-   **Group by filter**

    Organize event sections dynamically using the Group by filter in the Advanced filter dialog box. You can group by building and floor, and by other fields such as campus or space type. Applying a group by filter updates the Schedule view to show sections based on the selected attribute. For example, grouping by campus displays separate sections for each campus, while grouping by space type organizes sections according to room types.


**Parent Topic:**[Working with schedule view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-central/working-with-schedule-view.md)

