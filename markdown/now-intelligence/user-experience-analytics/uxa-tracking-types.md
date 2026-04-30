---
title: Types of tracking consent policies in User Experience Analytics
description: There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to the country and even according to users or roles.
locale: en-US
release: zurich
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [User privacy, tracking, and consent, Configure, User Experience Analytics, Platform Analytics]
---

# Types of tracking consent policies in User Experience Analytics

There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to the country and even according to users or roles.

## Types of tracking consent policies

The default consent policies are set to No Consent Required for all countries/groups of users. However, admins can update a group or individual country’s consent policy to any of the following:

-   **Basic tracking**

    Users with the admin role can obtain usage metrics only. This consent policy tracks and processes user activity but only stores basic user data, including hashed user IDs, and stores only partial session details including the session time.

-   **Disabled**

    No tracking of users occurs in any of the User Experience Analytics tracked applications. Usage metrics aren't obtained from these users.

-   **Explicit opt-in**

    Users are presented with a message to select whether to opt in or decline to be tracked. This is a more advanced policy.

-   **Notice**

    Users are presented with a message explaining that their activity in the application will be tracked. This is a more advanced policy.

-   **No consent required**

    Users are automatically tracked and aren't presented with an opt-in/decline message. This is the default consent policy for all users. This is a more advanced policy.


**Note:**

-   Every country’s consent policy is set to **No Consent Required** by default. However, users can opt in or out of ServiceNow applications individually in application settings. If you want to provide opt-in messages or notices to users when they log in, you must configure tracking consent policies.
-   If a country’s tracking consent policy is set to **Disabled**, user metrics aren't tracked.
-   Counters in the User Experience Analytics application contain aggregated user numbers.
-   Analytics administrators can choose to store additional user properties. See [Add user properties as filters to User Experience Analytics](../task/uxa-add-filters-uxa-pages.md) for more information.
-   When Consent policies are updated to display a notice or require opt-ins, capturing detailed user and session data may be impacted due to individual opt-outs. Aggregated metrics will continue to reflect the total user base, including those who have opted out of individual session tracking.

-   **[View assigned consent policies](../task/uxa-define-consent-policy.md)**  
View the list of tracking consent policies and select a consent policy to see all countries which are assigned to it. Within the consent policies list, you can assign the same tracking consent policy for all countries or reset all countries to the default value of No Consent Required.
-   **[View and update an individual country’s consent policy](../task/uxa-view-policy-country.md)**  
View a list of all countries with their assigned consent policies and select a country to update its existing policy.
-   **[Define how to detect your user's location](../task/uxa-define-detect-location.md)**  
Detect your users' location by selecting and prioritizing a detection policy. You can also define the order in which these policies apply. There are predefined detection policies, but you can create custom scripts to give more flexibility to your definitions.

**Parent Topic:**[User privacy, tracking, and user consent management in User Experience Analytics](../concept/user-exp-analytics-track-options.md)

