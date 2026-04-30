---
title: Define how to detect your user's location
description: Detect your users' location by selecting and prioritizing a detection policy. You can also define the order in which these policies apply. There are predefined detection policies, but you can create custom scripts to give more flexibility to your definitions.
locale: en-US
release: zurich
product: User Experience Analytics
classification: user-experience-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Types of tracking consent policies, User privacy, tracking, and consent, Configure, User Experience Analytics, Platform Analytics]
---

# Define how to detect your user's location

Detect your users' location by selecting and prioritizing a detection policy. You can also define the order in which these policies apply. There are predefined detection policies, but you can create custom scripts to give more flexibility to your definitions.

## Before you begin

Role required: analytics\_admin

## About this task

There are four methods by which you can detect a user's location. Prioritize the method by using the **Order** field and select if the policy should be active or not.

**Note:** If a detection provider isn't active or a script doesn’t return a response, the system default policy of Explicit Opt-in is implemented.

The available detection policy providers are:

-   **User country**

    Uses the Country code \[country\] column stored in the User table \[sys\_user\].

-   **Country Customer script**

    A custom script that can be loaded onto the ServiceNow Platform to determine the user's location and returns the country's ISO 3166-2 code.

    **Note:** If a customer script is defined but the Active field isn't selected, the next priority in the Order table will be activated.

-   **Policy Customer Script**

    A custom script that can be loaded onto the ServiceNow Platform to determine the user’s consent policy and return one of the policy names from the User Experience Analytics Consent Policy table \[sys\_analytics\_detection\_policy\_provider\].

    **Note:** If a customer script is defined but the Active field isn't selected, the next priority in the Order table is activated.

-   **GeoIP**

    An IP-based detection provider that identifies a user's geographical location using an internal service. This provider is the default option if no detection policies are selected.


## Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **UX Analytics settings** &gt; **Detection Policy Providers**.

    The User Experience Analytics Detection Policy Providers page displays.

2.  Select any of the detection policy providers to update its Active status and change the order in which the policy is enforced.

    **Note:** To enforce a policy, it must be active.

3.  Select either **Country Customer Script** or **Policy Customer Script** and enter a script to determine either the user’s location or the user’s consent policy, and to return a value.

    **Note:** You can use the system property **glide.analytics.consent.script\_timeout** to define the run time of the script. For more information, see [User Experience Analytics related properties](../reference/all-analytics-properties.md).

    For more information on using scripts, see [JavaScript syntax editor](https://www.servicenow.com/docs/access?context=c_SyntaxEditor&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).


**Parent Topic:**[Types of tracking consent policies in User Experience Analytics](../reference/uxa-tracking-types.md)

