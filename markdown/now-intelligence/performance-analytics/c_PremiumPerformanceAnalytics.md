---
title: Activating your Performance Analytics subscription
description: Without a paid Performance Analytics subscription, your use is limited to 180 days of data collection \(five months for monthly indicators\) and to specific indicators provided by ServiceNow. For unlimited access to all features, purchase a subscription to Performance Analytics.With a subscription to Performance Analytics, your features should be activated automatically.Confirm manually whether you are entitled to a Performance Analytics product line. If so, you are entitled to activate the corresponding plugin on production instances.When you have purchased a Performance Analytics subscription and identified the associated plugin, activate that plugin as follows.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Activating your Performance Analytics subscription

Without a paid Performance Analytics subscription, your use is limited to 180 days of data collection \(five months for monthly indicators\) and to specific indicators provided by ServiceNow. For unlimited access to all features, purchase a subscription to Performance Analytics.

After you purchase the subscription, you might need to activate the plugin associated with that subscription on production instances.

Performance Analytics subscriptions enable you to use the following functionality beyond what is available with the base system:

-   Custom Performance Analytics indicators, breakdowns, widgets, or other configuration records
-   Scores preserved for longer than 180 days \(Five full months for monthly indicators\)
-   Text analytics widgets \(Core UI only\)
-   [Proactive analytics insights on dashboards](../../par-for-workspace/concept/proactive-analytics.md)

If you have purchased Performance Analytics through a Professional or Enterprise offering, you may use it with no restrictions in these situations:

-   On the tables of the associated subscription, including associated ServiceNow store apps
-   With any platform and common apps, such as Knowledge Management, CMDB, or Catalog
-   With any paid-for Partner store apps

**Note:** The tables of free Partner store apps are considered custom tables and are mapped to ServiceNow subscriptions. Your right to use these tables with Performance Analytics depends on your entitlement to Performance Analytics for the mapped subscription.

If you try to perform these tasks on a production instance that doesn’t have a Performance Analytics subscription, you get a warning that a subscription is required.

![Warning that you cannot do what you are trying to do unless you subscribe to Performance Analytics](../image/complimentary-warning.png "Subscription-required warning")

The Performance Analytics Admin Console also warns you when an instance doesn’t have the full version of Performance Analytics activated.

![Performance Analytics admin console showing subscription version not activated](../image/admin-console-pa-not-activated.png)

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

## Subscription Management for Performance Analytics

With a subscription to Performance Analytics, your features should be activated automatically.

Starting in Tokyo, Subscription Management applies to Performance Analytics. If you use Subscription Management, you should not need to activate a Performance Analytics plugin manually. The remainder of this page describes the older, manual system of activating a subscription.

This feature is available only on hosted instances. On self-hosted and non-production instances, you still have to activate the appropriate Performance Analytics plugin manually. For more information, see [Subscription Management](https://www.servicenow.com/docs/access?context=subscription-management-landing-page-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Identify your entitlement to Performance Analytics on an on-premises instance

Confirm manually whether you are entitled to a Performance Analytics product line. If so, you are entitled to activate the corresponding plugin on production instances.

### Before you begin

Role required: admin

### About this task

On-premises instances do not have access to Subscription Management, so you must verify your entitlements manually. On other instances, this is not necessary.

### Procedure

1.  Navigate to **Subscriptions** &gt; **Application Entitlements** or directly open `subscription_entitlement_list.do`.

2.  In the Subscription Entitlements list, search for entitlements with a name that includes `Performance Analytics`.


### Result

On production instances, you may install Performance Analytics Premium plugins that correspond to these entitlements. You can install any Performance Analytics Premium plugin on non-production instances.

## Activate the plugin for your Performance Analytics subscription

When you have purchased a Performance Analytics subscription and identified the associated plugin, activate that plugin as follows.

### Before you begin

**Important:** Set up and test Performance Analytics on a non-production instance before you set it up on a production instance.

Role required: admin

### Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Under **Filters**, find the Listings section and select **Plugins**.

3.  Search for plugins with `performance analytics premium` in the name.

4.  Find and open the Performance Analytics premium plugin that matches your entitlement.

5.  Select **Install**.

    The Review Installation Details pane opens.![](../image/review-installation-details.png)

6.  Review the dependencies and install now or later.


### Result

A progress bar shows you the progress of the plugin activation, after which you have several options of what to view.

### What to do next

When the process is complete, consider installing Analytics Solutions, which include preconfigured dashboards and all necessary underlying components. For more information, see [Analytics solutions](../../dashboards/concept/content-packs-in-form-analytics.md).

Also consider activating Spotlight. Spotlight helps prioritize records by evaluating them against multiple weighted criteria. For more information, see [Ranking records with Spotlight](spotlight.md).

