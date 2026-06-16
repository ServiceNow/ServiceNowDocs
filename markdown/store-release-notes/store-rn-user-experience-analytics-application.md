---
title: Usage Insights application release notes
description: Version history for the Usage Insights application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-user-experience-analytics-application.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Usage Insights application release notes

Version history for the Usage Insights application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.2.2 - June 2026**
    -   Added AI Native Experience channel with metric support and a dedicated Conversations page.
    -   Custom dashboard creation extended to Zurich customers
    -   Events editing enabled on Zurich
    -   Conversation analytics surfaced for Zurich and Australia; data populates after upgrade to Zurich Patch 9 or Australia Patch 3.
    -   User Experience Analytics dashboard renamed to Usage Insights dashboard on Zurich.
-   **Version 6.1.12 - March 2026**
    -   User Experience Analytics has been renamed to Usage Insights. Usage insights can be accessed via the navigation menu by searching for Usage Insights as opposed to User Experience Analytics.
    -   The Usage Insights dashboard has been updated to meet A11Y accessibility standards. Screen readers, keyboard navigation, and contrast requirements are now fully supported, ensuring the dashboard experience is accessible to all users in compliance with WCAG guidelines.
        -   Tag and create new events, and update event descriptions. Increase the visibility and clarity of your created events
        -   Track events directly in the Usage Insights UI with no coding necessary. Create custom events without code directly in your application.
        -   View funnels you create in Usage Insights directly in Platform Analytics.
        -   Create dashboards for Platform Analytics directly in Usage Insights.
-   **Version 5.1.2 - February 2026**

    Not needed.

-   **Version 5.0.8 - August 2025**
    -   Fixed:
        -   Advanced filters - Delete a saved filter in advanced filters is not working
        -   Events Details Page - if no data \(score cards showing 0, the trends charts load\) the even properties charts keep loading endlessly
        -   Customer are not able to see all the event property values when exporting event property data
    -   Users and Sessions Page
        -   The export icon in the Users and Sessions Breakdown Analysis chart is displaying an orange dot notification icon
        -   User property filters should be available even when MTLS is disabled
        -   Customers are seeing incorrect dates \(often one day earlier\) in trend chart visualizations, leading to inconsistencies with the selected date range filter
        -   Cross-App overview - Usage per application table is loading infinitely
        -   Customers are seeing unselected columns appear in the Events table when an error occurs during column selection
        -   \[UXA Dashboard\]Export in Retention for Average weekly sessions per user and Average time between sessions \| In Pages for Prev Page and Next Page is not working
-   **Version 4.0.22 - July 2025 \(Yokohama\)**
    -   Fix for:
        -   App version filter is throwing error for mobile applications
        -   Customer are not able to see all the event property values when exporting event property data
        -   Customer are not able see Usage Data on the dashboard due to date format issue
        -   Customer is presented with incorrect "Total Page views by users" value on the UXA Dashboard
        -   The exported file from the Session's Page Groupby chart shows inconsistent column names that don't match the labels seen in the dashboard
        -   Customers are seeing unselected columns appear in the Events table when an error occurs during column selection
        -   Exported page names in Pages table are not consistent with display names shown in the UI
        -   Sorting the "Name" column in the Pages table doesn't sort the data as expected
        -   Page names shown in funnel/cohort visualizations are inconsistent with those shown during steps creation
-   **Version 4.0.17 - March 2025**
    -   Changed:
        -   Pages section on NextGen dashboard-&gt;performance:
            -   Grouped by NavigationType of performance data
            -   Message presented on Page Performance Data Graph Since it is not does not support filter by different properties
    -   Fixed:
        -   EventProperty Name will not be displayed when event property is not applicable for given filter - it will present that no data available
        -   Session Analysis breakdown of Hourly Usage
        -   Filters values
-   **Version 4.0.16 - February 2025**

    User Experience Analytics application provides an easy way to monitor usage analytics of your ServiceNow applications.


**Parent Topic:**[ServiceNow Store - Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-air.md)

