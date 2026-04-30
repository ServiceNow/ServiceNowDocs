---
title: User Experience Analytics release notes
description: The ServiceNow User Experience Analytics application enables you to monitor usage analytics of Next Experience web applications as well as Virtual Agent, ServiceNow mobile, and Service Portal applications. User Experience Analytics was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [uxa, navigation, funnel, cohort]
---

# User Experience Analytics release notes

The ServiceNow® User Experience Analytics application enables you to monitor usage analytics of Next Experience web applications as well as Virtual Agent, ServiceNow mobile, and Service Portal applications. User Experience Analytics was enhanced and updated in the Yokohama release.

## User Experience Analytics highlights for the Yokohama release

-   Access analytics more quickly across tracked ServiceNow applications in the redesigned UI.
-   Add and use new custom user properties more easily in the application. This requires older custom properties to be reconfigured under the new setup.
-   Advanced querying capabilities including user segmentation across all usage data and filtering of events by event property.

See [User Experience Analytics](https://www.servicenow.com/docs/access?context=user-exp-analytics-landing&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) for more information.

## Important information for upgrading the User Experience Analytics to Yokohama

-   The User Experience Analytics module is moved under Platform Analytics.
-   Custom user properties must be reconfigured.
-   Default country and user consent policies are updated to No Consent Required.
-   The User Experience Analytics UI and navigation structure are reworked.

## New in the Yokohama release

-   **Added filtering capability to all analytics pages**

    Analytics pages have various filter options to help segment data including Date range, User type, and Country. Other filters appropriate to each page are available.

-   **Configurable user properties**

    Filter usage data by custom user groups across all User Experience Analytics pages. Custom user properties can also be added to User details pages. User roles and department are available by default. Other user-related fields can be added to User Experience Analytics.

-   **Granular event filtering**

    Filter event data using event properties to provide more specific and actionable insights into your data.

-   **User information added to events**

    The number of unique users who performed an action visible next to the total occurrences of the event.


## UI changes

-   **Primary User Experience Analytics navigation has moved under the __All__ menu.**
    -   User Experience Analytics experience moved under **Platform Analytics** module.
    -   User Experience Analytics administrative functions moved under the **Platform Analytics Administration** &gt; **UX Analytics settings** module.
-   **Updated navigation within User Experience Analytics**

    Navigation to Analytics pages simplified to **Analytics** and **Data Foundation** sections for each application.

-   **New layout**

    The previous navigation has been replaced with a more unified, cleaner look and feel which enables you to understand the usage, user experience, and user satisfaction with your application.

-   **Improved Funnels UI**

    The UI has improved readability and navigation.


## Changed in this release

-   **New custom user property configuration**

    An easy way to configure which user-related fields are available to use as filters and in user details. Configured user properties are available for all applications. Previously created custom user properties are no longer supported and must be recreated in the new UI.

-   **Country consent policies are set by default to No Consent Required**

    Default country consent policies are now set to No Consent Required. If you have previously updated your country consent policies, they will retain the custom setting. Existing users who have set their tracking preferences will retain their settings. New users will not require consent for tracking unless you update your country consent policies.

-   **Longer user history**

    Detailed data for users and sessions extended to two years.

-   **Optimized the way metrics are calculated**

    Percent time on app and Average duration per page calculations changed compared to the application view in Xanadu or prior releases. Percentage time on app was **Percentage time on site** in Xanadu or prior releases.

-   **Client page load and Full page load aggregated in the same visualization**

    All performance metrics associated with Client, Network, Page Load, and Server time are aggregated together.


## Removed in this release

-   Automatic actions in the mobile app, including tap and swap.
-   Filtering by crashed/offline sessions in mobile applications.
-   Option to tag/favorite for users/sessions.
-   Geographic map view of sessions.
-   Users flow
-   Insights

## Activation information

User Experience Analytics is a ServiceNow AI Platform feature that is activated by default.

## Additional requirements

Customer must use ADC v3 to access the new User Experience Analytics experience. Customers on ADC v2 will have access to the Xanadu version of User Experience Analytics.

## Accessibility information

User Experience Analytics supports the Web Content Accessibility Guidelines \(WCAG\) 2.1 AA accessibility standard except for these aspects:

-   Voiceover for navigation paths
-   Color patterns for time series and pie visualizations
-   Data table for time series and pie visualizations

## Related ServiceNow applications and features

-   **Platform Analytics experience**

    Distribute and consume Platform Analytics through data visualizations and dashboards with optional filters. Explore KPIs and receive insights into significant events in the data.


**Parent Topic:**[Platform Analytics release notes](analytics-intel-report-rn-landing.md)

