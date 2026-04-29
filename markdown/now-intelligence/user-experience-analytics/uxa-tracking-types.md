---
title: Types of tracking consent policies in Usage Insights
description: There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to the country and even according to users or roles.
locale: en-US
release: australia
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [User privacy, tracking, and consent, Configuring Usage Insights, Usage Insights, Platform Analytics]
---

# Types of tracking consent policies in Usage Insights

There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to the country and even according to users or roles.

The default consent policies are set to No Consent Required for all countries/groups of users. However, admins can update a group or individual country’s consent policy to any of the following:

-   **Basic tracking**

    Users with the admin role can obtain usage metrics only. This consent policy tracks and processes user activity but only stores basic user data, including hashed user IDs, and stores only partial session details including the session time.

-   **Disabled**

    No tracking of users occurs in any of the Usage Insights tracked applications. Usage metrics aren't obtained from these users.

-   **Explicit opt-in**

    Users are presented with a message to select whether to opt in or decline to be tracked. This is a more advanced policy.

-   **Notice**

    Users are presented with a message explaining that their activity in the application will be tracked. This is a more advanced policy.

-   **No consent required**

    Users are automatically tracked and aren't presented with an opt-in/decline message. This is a more advanced policy. This is the default consent policy for all users.


**Note:**

-   Every country’s consent policy is set to **No Consent Required** by default. However, users can opt in or out of ServiceNow applications individually in application Settings. If you want to provide opt-in messages or notices to users when they log in, you must configure tracking consent policies.
-   If a country’s consent policy is set to **Explicit Opt-In** or **Notice**, individual users are asked for consent yearly. Their existing tracking preference expires every 365 days.
-   If a country’s tracking consent policy is set to **Disabled**, user metrics aren't tracked.
-   Counters in the Usage Insights application contain aggregated user numbers.
-   Analytics administrators can choose to store additional user properties. See [Add user properties as filters to Usage Insights](../task/uxa-add-filters-uxa-pages.md) for more information.
-   When Consent policies are updated to display a notice or require opt-ins, capturing detailed user and session data may be impacted due to individual opt-outs. Aggregated metrics will continue to reflect the total user base, including those who have opted out of individual session tracking.

-   **[Define consent policies according to country](../task/uxa-define-consent-policy.md)**  
Define the tracking consent policies for users within different countries. You can either select the same tracking consent policy for all countries, use the allocated default values, or define different consent policies for individual countries.
-   **[View and update an individual country’s consent policy](../task/uxa-view-policy-country.md)**  
View a list of all countries with their assigned consent policies and select a country to update its existing policy.
-   **[Define how to detect your user's location](../task/uxa-define-detect-location.md)**  
Detect your users' location by selecting and prioritizing a detection policy. You can also define the order in which these policies apply. There are predefined detection policies, but you can create custom scripts to give more flexibility to your definitions.

**Parent Topic:**[User privacy, tracking, and user consent management in Usage Insights](../concept/user-exp-analytics-track-options.md)

