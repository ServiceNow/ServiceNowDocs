---
title: Types of tracking consent policies in User Experience Analytics
description: There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to the country and even according to users or roles.
locale: en-US
release: yokohama
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2025-05-22"
reading_time_minutes: 2
breadcrumb: [User privacy, tracking, and consent, Configuring User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Types of tracking consent policies in User Experience Analytics

There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to the country and even according to users or roles.

The default consent policies are set to No Consent Required for all countries/groups of users. However, admins can update a group or individual country’s consent policy to any of the following:

-   **Basic Tracking**

    Users with the admin role can obtain usage metrics only. This consent policy tracks and processes user activity but only stores basic user data, including hashed user IDs, and stores only partial session details including the session time.

-   **Disabled**

    No tracking of users occurs in any of the User Experience Analytics tracked applications. Usage metrics aren't obtained from these users.

-   **Explicit Opt-in**

    Users are presented with a message to select whether to opt in or decline to be tracked. This is a more advanced policy.

-   **Notice**

    Users are presented with a message explaining that their activity in the application will be tracked. This is a more advanced policy.

-   **No Consent Required**

    Users are automatically tracked and aren't presented with an opt-in/decline message. This is the default consent policy for all users. This is a more advanced policy.


**Note:**

-   “No consent required” is the default setting for all users. However, users can opt in or out of ServiceNow applications individually in application Settings. If you want to provide opt-in messages or notices to users when they log in, you must configure tracking consent policies.
-   When consent policies are updated to display a notice or require opt-ins, capturing detailed user and session data may be impacted due to individual opt-outs. Aggregated metrics will continue to reflect the total user base, including those who have opted out of individual session tracking.
-   Counters in the User Experience Analytics application contain aggregated user numbers.
-   If the tracking consent policy named **Disabled** is selected, user metrics aren't tracked.
-   If a country’s consent policy is set to **Explicit Opt-In** or **Notice**, individual users are asked for consent yearly. Their existing tracking preference expires every 365 days.
-   Analytics administrators can choose to store additional user properties. See Add user properties as filters to User Experience Analytics for more information.

-   **[Define consent policies according to country](../task/uxa-define-consent-policy.md)**  
Define the tracking consent policies for users within different countries. You can either select the same tracking consent policy for all countries, use the allocated default values, or define different consent policies for individual countries.
-   **[Define texts for Notice and Explicit Opt-in user consent management policies](../task/uxa-define-text-policies.md)**  
Edit the texts for Notice and Explicit Opt-in consent policies from the default text provided.
-   **[View users' consent management policies](../task/uxa-view-user-decision.md)**  
View and analyze details regarding users and their tracking selection preferences.
-   **[Configure link to your privacy policy](../task/uxa-config-link-privacy-policy.md)**  
The privacy policy link is shown when User Experience Analytics is enabled and users choose to enable or disable tracking.

**Parent Topic:**[User privacy, tracking, and user consent management in User Experience Analytics](../concept/user-exp-analytics-track-options.md)

