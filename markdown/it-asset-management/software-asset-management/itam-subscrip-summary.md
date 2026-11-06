---
title: Subscription summary for IT Asset Management
description: The IT Asset Management Subscription Summary dashboard tracks purchased and consumed subscriptions, so you can monitor usage, plan renewals, and stay within your license entitlements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/itam-subscrip-summary.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Subscriptions for Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Subscription summary for IT Asset Management

The IT Asset Management Subscription Summary dashboard tracks purchased and consumed subscriptions, so you can monitor usage, plan renewals, and stay within your license entitlements.

## Access the subscription summary

Navigate to **&gt;All** &gt; **ITAM Licensing** &gt; **ITAM Subscription Summary** to view your organization's purchased and allocated subscriptions. The **Subscription Entitlements** page opens.

View the following statistics on subscriptions purchased a la carte and by bundles:

<table id="table_mgl_gbs_1lc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of either subscription bundle or IT Asset Management application, if your organization purchased subscriptions per application separately \(a la carte\).

</td></tr><tr><td>

Purchased

</td><td>

The number of purchased subscriptions per bundle or application \(a la carte\).

</td></tr><tr><td>

Allocated

</td><td>

The number of consumed subscriptions from a bundle or application \(a la carte\). For bundles, this field shows the highest number of consumed subscriptions by applications that are part of the bundle. For example, if IT Asset Management consumed 300 subscriptions and Hardware Asset Management consumed 200 subscriptions, this field shows 300 for the bundle covering these applications.The color code indicates the percentage of the subscriptions that your organization consumed. By default, the color code threshold is 90%.

-   Green: Your organization has used less than 90% of purchased subscriptions.
-   Yellow: Your organization has used 90% or more, but less than 100%, of purchased subscriptions.
-   Red: Your organization has used 100% or more of purchased subscriptions. Purchased subscriptions are overdrawn.

</td></tr><tr><td>

Start date/End date

</td><td>

The dates for which this subscription is valid.

</td></tr></tbody>
</table>The licensing module calculates and displays subscription consumption as follows:

<table id="table_f1q_qbs_1lc"><thead><tr><th>

Model

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subscriptions by bundle only

</td><td>

When you purchase subscriptions in bundles, you get the same number of subscriptions for all IT Asset Management applications covered by the bundle. For example, for a bundle of 500 that covers IT Asset Management and Hardware Asset Management, your organization receives 500 subscriptions for IT Asset Management and 500 subscriptions for Hardware Asset Management.

 The licensing module subtracts the number of consumed subscriptions from the bundle subscriptions for the relevant application. Bundle subscriptions cover specific applications. You can't use bundle subscriptions for other applications, even if these other applications are part of the same bundle. For example, you purchased a bundle of 500 covering IT Asset Management and Hardware Asset Management, and you used up all 500 IT Asset Management subscriptions. You can't use the spare Hardware Asset Management subscriptions for IT Asset Management.

 If your organization exceeds the number of purchased subscriptions, the bundle size is automatically adjusted to the number of consumed subscriptions. When that happens, the licensing module recalculates levels of consumption for all applications covered by the same bundle.

 The Subscriptions window displays the actual number of consumed subscriptions under **Allocated**. The red color dot in **Allocated** indicates that the bundle is overdrawn.

</td></tr><tr><td>

Subscriptions a la carte only

</td><td>

The licensing module subtracts the number of consumed subscriptions from the a la carte subscriptions for the relevant application. The Subscriptions window displays the information for purchased and allocated subscriptions for IT Asset Management applications.

 If your organization exceeds the number of purchased subscriptions for an IT Asset Management application, you can't use unconsumed subscriptions for another application.

 If your organization exceeds the number of subscriptions, the Subscriptions window shows the relevant a la carte subscription is overdrawn.

</td></tr><tr><td>

Subscriptions for the same applications both in bundle and a la carte

</td><td>

If you purchased IT Asset Management subscriptions both in bundle and a la carte, the licensing module always subtracts consumed subscriptions from the bundle first. It then deducts them from the subscriptions purchased a la carte.

 For example, there is a bundle of 500 subscriptions covering IT Asset Management and Hardware Asset Management. In addition, there are 250 subscriptions for IT Asset Management purchased a la carte. The first 500 subscriptions consumed by IT Asset Management are consumed by the bundle. Only when IT Asset Management exceeds the number of subscriptions in the bundle does the licensing module start deducting from subscriptions purchased a la carte. It then shows those subscriptions as allocated to IT Asset Management.

 If your organization exceeds the number of subscriptions purchased in bundle and a la carte, the licensing module considers it as overdrawn from the a la carte subscriptions. In this case, the Subscriptions window indicates that the a la carte subscriptions are overdrawn.

</td></tr></tbody>
</table>**Parent Topic:**[Subscriptions for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/sam-subscription.md)

