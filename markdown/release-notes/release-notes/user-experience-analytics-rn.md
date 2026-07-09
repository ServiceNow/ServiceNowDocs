---
title: Usage Insights release notes
description: The ServiceNow Usage Insights application enables you to monitor usage analytics of Next Experience web applications as well as Virtual Agent, ServiceNow mobile, and Service Portal applications. Usage Insights was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [uxa, navigation, funnel, cohort]
---

# Usage Insights release notes

The ServiceNow® Usage Insights application enables you to monitor usage analytics of Next Experience web applications as well as Virtual Agent, ServiceNow mobile, and Service Portal applications. Usage Insights was enhanced and updated in the Yokohama release.

## Usage Insights highlights for the Yokohama release

-   Access analytics more quickly across tracked ServiceNow applications in the redesigned UI.
-   Add and use new custom user properties more easily in the application. This requires older custom properties to be reconfigured under the new setup.
-   Advanced querying capabilities including user segmentation across all usage data and filtering of events by event property.

See [User Experience Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/user-exp-analytics-landing.md) for more information.

## Important information for upgrading the Usage Insights to Yokohama

-   The Usage Insights module is moved under Platform Analytics.
-   Custom user properties must be reconfigured.
-   Default country and user consent policies are updated to No Consent Required.
-   The Usage Insights UI and navigation structure are reworked.

## New in the Yokohama release

-   **[Added filtering capability to all analytics pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/filter-user-list.md)**

    Analytics pages have various filter options to help segment data including Date range, User type, and Country. Other filters appropriate to each page are available.

-   **[Configurable user properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/uxa-add-filters-uxa-pages.md)**

    Filter usage data by custom user groups across all Usage Insights pages. Custom user properties can also be added to User details pages. User roles and department are available by default. Other user-related fields can be added to Usage Insights.

-   **[Granular event filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/view-events.md)**

    Filter event data using event properties to provide more specific and actionable insights into your data.

-   **[User information added to events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/view-events.md)**

    The number of unique users who performed an action visible next to the total occurrences of the event.


## UI changes

-   **[Primary Usage Insights navigation has moved under the __All__ menu.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/user-exp-analytics-dashboard.md)**
    -   Usage Insights experience moved under **Platform Analytics** module.
    -   Usage Insights administrative functions moved under the **Platform Analytics Administration** &gt; **UX Analytics settings** module.
-   **[Updated navigation within Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/exploring-user-exp-analytics.md)**

    Navigation to Analytics pages simplified to **Analytics** and **Data Foundation** sections for each application.

-   **[New layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/exploring-user-exp-analytics.md)**

    The previous navigation has been replaced with a more unified, cleaner look and feel which enables you to understand the usage, user experience, and user satisfaction with your application.

-   **[Improved Funnels UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/funnel-reports-uxa.md)**

    The UI has improved readability and navigation.


## Changed in this release

-   **[New custom user property configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/uxa-add-filters-uxa-pages.md)**

    An easy way to configure which user-related fields are available to use as filters and in user details. Configured user properties are available for all applications. Previously created custom user properties are no longer supported and must be recreated in the new UI.

-   **[Country consent policies are set by default to No Consent Required](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/uxa-tracking-types.md)**

    Default country consent policies are now set to No Consent Required. If you have previously updated your country consent policies, they will retain the custom setting. Existing users who have set their tracking preferences will retain their settings. New users will not require consent for tracking unless you update your country consent policies.

-   **[Longer user history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/configuring-user-exp-analytics.md)**

    Detailed data for users and sessions extended to two years.

-   **[Optimized the way metrics are calculated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/uxa-duration-calculations.md)**

    Percent time on app and Average duration per page calculations changed compared to the application view in Xanadu or prior releases. Percentage time on app was **Percentage time on site** in Xanadu or prior releases.

-   **[Client page load and Full page load aggregated in the same visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/view-pages.md)**

    All performance metrics associated with Client, Network, Page Load, and Server time are aggregated together.


## Removed in this release

-   Automatic actions in the mobile app, including tap and swap.
-   Filtering by crashed/offline sessions in mobile applications.
-   Option to tag/favorite for users/sessions.
-   Geographic map view of sessions.
-   Users flow
-   Insights

## Deprecations

-   **[Usage Insights in Xanadu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/user-exp-analytics-landing.md)**

    Usage Insights is no longer supported in the Xanadu release. Upgrade to Yokohama, Zurich, or Australia to continue using Usage Insights.


## Activation information

Usage Insights is a ServiceNow AI Platform feature that is activated by default.

## Additional requirements

Customer must use ADC v3 to access the new Usage Insights experience. Customers on ADC v2 will have access to the Xanadu version of Usage Insights.

## Accessibility information

Usage Insights supports the Web Content Accessibility Guidelines \(WCAG\) 2.1 AA accessibility standard except for these aspects:

-   Voiceover for navigation paths
-   Color patterns for time series and pie visualizations
-   Data table for time series and pie visualizations

## Related ServiceNow applications and features

-   **[Platform Analytics experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/par-workspace.md)**

    Distribute and consume Platform Analytics through data visualizations and dashboards with optional filters. Explore KPIs and receive insights into significant events in the data.


**Parent Topic:**[Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/analytics-intel-report-rn-landing.md)

