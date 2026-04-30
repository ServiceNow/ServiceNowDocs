---
title: Subscription summary for IT Asset Management application
description: You can view how many subscriptions for IT Asset Management applications your organization purchased and allocated.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Licensing for IT Asset Management, IT Asset Management]
---

# Subscription summary for IT Asset Management application

You can view how many subscriptions for IT Asset Management applications your organization purchased and allocated.

Review the configuration item \(CI\) allocation and allocation level to see how your organization uses IT Asset Management application subscriptions and plan upcoming subscription needs.

Navigate to **ITAM Licensing** &gt; **ITAM Subscription Summary** to view the subscription summary.

View the following statistics on subscriptions purchased a la carte and by bundles:

-   **Name**

    The name of either subscription bundle or IT Asset Management application, if your organization purchased subscriptions per application separately \(a la carte\).

-   **Purchased**

    The number of purchased subscriptions per bundle or application \(a la carte\).

-   **Allocated**

    The number of consumed subscriptions from a bundle or application \(a la carte\). For bundles, this field shows the highest number of consumed subscriptions by applications that are part of the bundle. For example, if Software Asset Management consumed 300 subscriptions and Hardware Asset Management consumed 200 subscriptions, this field shows 300 for the bundle covering these applications.

    The color code indicates the percentage of the subscriptions that your organization consumed. By default, the color code threshold is 90%.

    -   Green — Your organization has used less than 90% of purchased subscriptions.
    -   Yellow — Your organization has used more than 90%, but less than 100% of purchased subscriptions.
    -   Red — Your organization has used 100% or more and exceeded the number of purchased subscriptions. Purchased subscriptions are overdrawn.
-   **Start date/End date**

    The dates for which this subscription is valid.


The licensing module calculates and displays subscription consumption as follows:

-   **Subscriptions by bundle only**

    When you purchase subscriptions in bundles, you get the same number of subscriptions for all IT Asset Management applications covered by the bundle. For example, for a bundle of 500 that covers Software Asset Management and Hardware Asset Management, your organization receives 500 subscriptions for Software Asset Management and 500 subscriptions for Hardware Asset Management.

    The licensing module subtracts the number of consumed subscriptions from the bundle subscriptions for the relevant application. Bundle subscriptions cover specific applications. You cannot use bundle subscriptions for other applications, even if these other applications are part of the same bundle. For example, you purchased a bundle of 500 covering Software Asset Management and Hardware Asset Management, and you used up all 500 Software Asset Management subscriptions. You cannot use the spare Hardware Asset Management subscriptions for Software Asset Management.

    If your organization exceeds the number of purchased subscriptions, the bundle size is automatically adjusted to the number of consumed subscriptions. When that happens, the licensing module recalculates levels of consumption for all applications covered by the same bundle.

    The Subscriptions window displays the actual number of consumed subscriptions under **Allocated**. The red color dot in **Allocated** indicates that the bundle is overdrawn.

-   **Subscriptions a la carte only**

    The licensing module subtracts the number of consumed subscriptions from the a la carte subscriptions for the relevant application. The Subscriptions window displays the information for purchased and allocated subscriptions for IT Asset Management applications.

    If your organization exceeds the number of purchased subscriptions for an IT Asset Management application, you cannot use unconsumed subscriptions for another application.

    If your organization exceeds the number of subscriptions, the Subscriptions window shows the relevant a la carte subscription is overdrawn.

-   **Subscriptions for the same applications both in bundle and a la carte**

    If you purchased IT Asset Management subscriptions both in bundle and a la carte, the licensing module always subtracts the number of consumed subscriptions from the bundle before deducting from the number of subscriptions purchased a la carte. For example, there is a bundle of 500 subscriptions covering Software Asset Management and Hardware Asset Management. In addition, there are 250 subscriptions for Software Asset Management purchased a la carte. The first 500 subscriptions consumed by Software Asset Management are consumed by the bundle. Only when Software Asset Management exceeds the number of subscriptions in the bundle, the licensing module starts deducting from subscriptions purchased a la carte and shows them as subscriptions allocated to Software Asset Management.

    If your organization exceeds the number of subscriptions purchased in bundle and a la carte, the licensing module considers it as overdrawn from the a la carte subscriptions. In this case, the Subscriptions window indicates that the a la carte subscriptions are overdrawn.


