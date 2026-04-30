---
title: User privacy, tracking, and user consent management in User Experience Analytics
description: User Experience Analytics relies on tracking user activity to measure the adoption, retention, and usage of KPIs to help you make better product and implementation decisions.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: concept
last_updated: "2024-12-09"
reading_time_minutes: 2
breadcrumb: [Configuring User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# User privacy, tracking, and user consent management in User Experience Analytics

User Experience Analytics relies on tracking user activity to measure the adoption, retention, and usage of KPIs to help you make better product and implementation decisions.

## Tracking users in User Experience Analytics

User Experience Analytics can be used to track user behavior across Platform Analytics, Core UI, ServiceNow Mobile Platform, Service Portal, and the Conversational Analytics area of the Virtual Agent. User Experience Analytics used on web applications or mobile applications collects limited information, including individually the assigned User Experience Analytics user ID, the hashed system user ID, session start time and duration, and city-level location.

Tracking users in User Experience Analytics utilizes the user consent management \(UCM\) capability, enabling administrators to configure their analytics tracking preferences across all tracked applications. This capability provides the flexibility to customize the consent policy for each country and to select how the location of the user is detected.

Some of the options available to you with user consent management are:

-   Applying different tracking consent policies to individual countries.
-   Tracking specific users or tracking users with specific roles.
-   Defining how to detect your users’ location.

Counters in the User Experience Analytics application contain aggregated user numbers.

**Note:** If the tracking consent policy named **Disabled** is selected, user metrics aren't tracked.

## Types of tracking consent policies

-   **Basic tracking**

    Users with the admin role can obtain usage metrics only. This consent policy tracks and processes user activity but only stores basic user data, including hashed user IDs, and stores only partial session details including the session time.

-   **Explicit opt-in**

    Users are presented with a message to select whether to opt in or decline to be tracked. This policy is the default consent policy for EU, EFTA, and UK users.

-   **Notice**

    Users are presented with a message explaining that their activity in the application will be tracked. This policy is the default consent policy for non-US and non-EU, EFTA, and UK users.

-   **No consent required**

    Users are automatically tracked and aren't presented with an opt-in/decline message. This policy is the default consent policy for United States users.

-   **Disabled**

    No tracking of users occurs in any of the User Experience Analytics tracked applications. Usage metrics aren't obtained from these users.


-   **[User tracking preferences for User Experience Analytics](../task/user-exp-analytics-user-set.md)**  
You can select to opt in or opt out of User Experience Analytics advanced tracking at any point.
-   **[Enable or disable User Experience Analytics tracking](../task/disable-tracking-mobile-app.md)**  
You can turn off or turn on tracking for Platform Analytics, ServiceNow Mobile Platform, Service Portal, and the Conversational Analytics area of Virtual Agent by updating the User Experience Analytics settings.
-   **[Types of tracking consent policies in User Experience Analytics](../reference/uxa-tracking-types.md)**  
There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to the country and even according to users or roles.
-   **[Define how to detect your user's location](../task/uxa-define-detect-location.md)**  
Detect your users by selecting and prioritizing a detection policy. You can also define the order in which these policies apply. There are predefined detection policies, but you can create custom scripts to give more flexibility to your definitions.
-   **[Tracked analytics fields and cookies](uxa-tracked-fields-and-cookies.md)**  
User Experience Analytics tracks data from several sources, including web and mobile analytics fields, and client-side cookies.

**Parent Topic:**[Configuring User Experience Analytics](../content-framework/create/configuring-user-exp-analytics.md)

