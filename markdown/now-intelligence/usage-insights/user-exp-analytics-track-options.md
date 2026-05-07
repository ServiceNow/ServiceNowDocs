---
title: User privacy, tracking, and user consent management in Usage Insights
description: Usage Insights relies on tracking user activity to measure the adoption, retention, and usage of KPIs to help you make better product and implementation decisions.
locale: en-US
release: australia
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Usage Insights, Usage Insights, Platform Analytics]
---

# User privacy, tracking, and user consent management in Usage Insights

Usage Insights relies on tracking user activity to measure the adoption, retention, and usage of KPIs to help you make better product and implementation decisions.

## Tracking users in Usage Insights

Usage Insights can be used to track user behavior across  ServiceNow Core UI, Next Experience, Portal, and Mobile applications.  Usage Insights used on web and mobile applications collects limited information about the users themselves.

Usage Insights doesn’t store the user ID. Instead, it uses a one-way SHA256 hash of the sys\_id, stored on the sys\_user\_table as “Hashed User ID”, to identify the same user consistently across multiple devices. This way, Usage Insights can anonymize users while retaining the ability to connect individual users to their session data consistently. This one-way hash also enables customers to reconnect their Usage Insights data to personally identifiable information available on the sys\_user table if they choose.

The hash isn’t salted intentionally. This way, customers can obtain the ID of a specific user they want to track, apply a SHA256 on that ID \(for example, here: [SHA256 calculator](https://xorbin.com/tools/sha256-hash-calculator)\), and then use the output to filter the data for a specific User ID.

By default, Usage Insights translates the end user's IP address to a city level location, which is stored. However, the IP address isn’t stored.

**Note:**

Geolocation information may be considered personally identifiable information \(PII\).

Administrators can configure analytics tracking preferences across all tracked applications via user consent management \(UCM\). This capability provides the flexibility to customize the consent policy for each country and to select how the location of the user is detected.

Some of the options available to you with user consent management are:

-   Applying different tracking consent policies to individual countries.
-   Tracking specific users or tracking users with specific roles.
-   Defining how to detect your users’ location.

-   **[How users consent to tracking in Usage Insights](../task/user-exp-analytics-user-set.md)**  
An individual can select to opt in or opt out of Usage Insights advanced tracking at any time.
-   **[Types of tracking consent policies in Usage Insights](../reference/uxa-tracking-types.md)**  
There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to your own compliance requirements, applicable country requirements, and even according to users or roles.
-   **[Tracked analytics fields and cookies](uxa-tracked-fields-and-cookies.md)**  
Usage Insights tracks data from several sources, including web and mobile analytics fields and client-side cookies.

**Parent Topic:**[Configuring Usage Insights](../content-framework/create/configuring-user-exp-analytics.md)

