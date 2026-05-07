---
title: Types of tracking consent policies in Usage Insights
description: There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to your own compliance requirements, applicable country requirements, and even according to users or roles.
locale: en-US
release: australia
product: Usage Insights
classification: usage-insights
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [User privacy, tracking, and consent, Configuring Usage Insights, Usage Insights, Platform Analytics]
---

# Types of tracking consent policies in Usage Insights

There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to your own compliance requirements, applicable country requirements, and even according to users or roles.

The default consent policies are set to No Consent Required for all countries/groups of users. However, your admins should review and update a group or individual country’s consent policy in line with compliance requirements to any of the following:

-   **Basic tracking**

    Users with the admin role can obtain usage metrics only. Their hashed user ID and session data continue to be collected and included in aggregate metrics \(such as Active Users, Sessions, and Average Session Duration\) so that these counts remain accurate for the Customer.

-   **Disabled**

    Selecting **Disabled** as the user consent policy has the same effect as an end user opting out: individual-level tracking is not displayed in Usage Insights tracked applications and usage metrics aren't obtained from these users. Aggregate data collection continues.

-   **Explicit opt-in**

    Users are presented with a message to select whether to opt in or decline to be tracked.

-   **Notice**

    Users are presented with a message explaining that their activity in the application will be tracked.

-   **No consent required**

    Users are automatically tracked and aren't presented with an opt-in/decline message. This is the default consent policy for all users. However, you should review and amend this policy in accordance with internal policies.


**Note:**

-   Every country’s consent policy is set to **No Consent Required** by default. However, users can opt in or out of ServiceNow applications individually in application settings. If you want to provide opt-in messages or notices to users when they log in, you must configure tracking consent policies.
-   If a country’s consent policy is set to **Explicit Opt-In** or **Notice**, individual users are asked for consent yearly. Their existing tracking preference expires every 365 days.
-   If a country’s tracking consent policy is set to **Disabled**, user metrics aren't tracked and aggregate data collection continues.
-   The distinction between **Basic** and full tracking is in how data is presented, not in what is collected.
-   Counters in the Usage Insights application contain aggregated user numbers.
-   Analytics administrators can choose to store additional user properties. See [Add user properties as filters to Usage Insights](../task/uxa-add-filters-uxa-pages.md) for more information.
-   When Consent policies are updated to display a notice or require opt-ins, capturing detailed user and session data may be impacted due to individual opt-outs. Aggregated metrics will continue to reflect the total user base, including those who have opted out of individual session tracking.

-   **[Define consent policies according to country](../task/uxa-define-consent-policy.md)**  
Define the tracking consent policies for users within different countries. You can either select the same tracking consent policy for all countries, use the allocated default values, or define different consent policies for individual countries.
-   **[View and update an individual country’s consent policy](../task/uxa-view-policy-country.md)**  
View a list of all countries with their assigned consent policies and select a country to update its existing policy.
-   **[Define how to detect your user's location](../task/uxa-define-detect-location.md)**  
Detect your users' location by selecting and prioritizing a detection policy. You can also define the order in which these policies apply. There are predefined detection policies, but you can create custom scripts to give more flexibility to your definitions.
-   **[Tracking controls and data collection behavior](../task/uxa-tracking-controls-and-data-collection-behavior.md)**  
Understand what happens when you opt out of the consent pop-up in the Usage Insights UI

**Parent Topic:**[User privacy, tracking, and user consent management in Usage Insights](../concept/user-exp-analytics-track-options.md)

