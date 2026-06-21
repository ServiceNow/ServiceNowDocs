---
title: User privacy, tracking, and user consent management in Usage Insights
description: Usage Insights relies on tracking user activity to measure the adoption, retention, and usage of KPIs \(key performance indicators\) to help you make better product and implementation decisions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/now-intelligence/usage-insights/user-exp-analytics-track-options.html
release: yokohama
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# User privacy, tracking, and user consent management in Usage Insights

Usage Insights relies on tracking user activity to measure the adoption, retention, and usage of KPIs \(key performance indicators\) to help you make better product and implementation decisions.

## Tracking users in Usage Insights

Usage Insights can be used to track user behavior across  ServiceNow Core UI, Next Experience, Portal, and Mobile applications.  Usage Insights used on web and mobile applications collects limited information about the users themselves.

Usage Insights doesn’t store the user ID. Instead, it uses a one-way SHA256 hash of the sys\_id, stored on the sys\_user\_table as “Hashed User ID”, to identify the same user consistently across multiple devices. This way, Usage Insights can anonymize users while retaining the ability to connect individual users to their session data consistently. This one-way hash also enables customers to reconnect their Usage Insights data to personally identifiable information available on the sys\_user table if they choose.

The hash isn’t salted intentionally. This way, customers can obtain the ID of a specific user they want to track, apply a SHA256 on that ID \(for example here: [SHA-256 hash calculator](https://xorbin.com/tools/sha256-hash-calculator)\), and then use the output to filter the data for a specific User ID.

By default, Usage Insights translates the end user's IP address to a city level location, which is stored. However, the IP address isn’t stored.

**Note:**

Geolocation information may be considered personally identifiable information \(PII\).

Administrators can configure analytics tracking preferences across all tracked applications via user consent management \(UCM\). This capability provides the flexibility to customize the consent policy for each country and to select how the location of the user is detected.

Some of the options available to you with user consent management are:

-   Applying different tracking consent policies to individual countries.
-   Tracking specific users or tracking users with specific roles.
-   Defining how to detect your users’ location.

-   **[How users consent to tracking in Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/user-exp-analytics-user-set.md)**  
An individual can select to opt in or opt out of Usage Insights advanced tracking at any time.
-   **[Types of tracking consent policies in Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/uxa-tracking-types.md)**  
There are five types of tracking consent policies that you can define for individual countries. This option provides you with the flexibility to define tracking policies according to your own compliance requirements, applicable country requirements, and even according to users or roles.
-   **[Define how to detect your user's location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/uxa-define-detect-location.md)**  
Detect your users by selecting and prioritizing a detection policy. You can also define the order in which these policies apply. There are predefined detection policies, but you can create custom scripts to give more flexibility to your definitions.
-   **[Tracked analytics fields and cookies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/uxa-tracked-fields-and-cookies.md)**  
Usage Insights tracks data from several sources, including web and mobile analytics fields, and client-side cookies.
-   **[Add user properties as filters to Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/uxa-add-filters-uxa-pages.md)**  
In addition to the default filters on the pages of the Usage Insights application, you can add filters based on user properties. This allows you to effectively segment your Usage Insights data to develop a deeper understanding of your users and their usage patterns. User properties-based filters are supported as global filters for all pages and objects in the Usage Insights application.

**Parent Topic:**[Configuring User Experience Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/usage-insights/configuring-user-exp-analytics.md)

