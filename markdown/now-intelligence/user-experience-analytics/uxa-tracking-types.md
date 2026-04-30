---
title: Types of tracking consent policies in User Experience Analytics
description: There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to the country and even according to users or roles.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [User privacy, tracking, and consent, Configuring User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Types of tracking consent policies in User Experience Analytics

There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to the country and even according to users or roles.

There are default settings for three different groups of users:

-   Users from the US
-   Users from EU, UK, and European Free Trade Association \(EFTA\) countries \(Iceland, Liechtenstein, Norway, and Switzerland\)
-   Users from all other countries.

The default consent policies are dependent on the end user's geolocation.

The preceding list details the tracking consent policies available and highlights the default settings for US users; EU, EFTA, and UK users; and users from all other locations.

-   **Explicit Opt-in**

    Users are presented with a message to select whether to opt in or decline to be tracked. This policy is the default consent policy for EU, EFTA, and UK users.

-   **Notice**

    Users are presented with a message explaining that their activity in the application will be tracked. This policy is the default consent policy for non-US and non-EU, EFTA, and UK users.

-   **No Consent Required**

    Users are automatically tracked and aren't presented with a message that asks if they want to opt in or decline to be tracked. This policy is the default consent policy for US users.

-   **Basic Tracking**

    The basic tracking consent policy enables users with the admin role to obtain usage metrics only. This consent policy tracks and processes user activity but only stores basic user data. This basic data includes hashed user IDs \(which is the process of hashing the end-user identifier before information is sent to the ServiceNow User Experience Analytics server\), and the storing of partial session details including the session time.

-   **Disabled**

    No tracking of users occurs in any of the User Experience Analytics tracked applications. Usage metrics aren't obtained from these users.


**Note:** Consent policies influence the numerical KPIs of the User Experience Analytics dashboard by updating the relevant counters. This process still enables you to view metrics for your entire user base. For example, aggregated data like the number of event counts relating to all users.

-   **[Defining consent policies according to country](../task/uxa-define-consent-policy.md)**  
Define the tracking consent policies for users within different countries. You can either select the same tracking consent policy for all countries, use the allocated default values, or define different consent policies for individual countries.
-   **[Defining texts for Notice and Explicit Opt-in user consent management policies](../task/uxa-define-text-policies.md)**  
Learn how to edit the texts for Notice and Explicit Opt-in consent policies from the default text provided.
-   **[Viewing users' consent management policies](../task/uxa-view-user-decision.md)**  
View and analyze details regarding users and their tracking selection preferences.

**Parent Topic:**[User privacy, tracking, and user consent management in User Experience Analytics](../concept/user-exp-analytics-track-options.md)

