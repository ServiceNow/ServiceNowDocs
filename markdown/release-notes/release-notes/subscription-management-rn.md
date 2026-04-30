---
title: Subscription Management release notes
description: The ServiceNow Subscription Management application enables you to manage your subscriptions proactively and monitor subscription usage on your instances. Subscription Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Subscription Management release notes

The ServiceNow® Subscription Management application enables you to manage your subscriptions proactively and monitor subscription usage on your instances. Subscription Management was enhanced and updated in the Yokohama release.

## Subscription Management highlights for the Yokohama release

-   View subscription allocations according to the number of active users.
-   Select all recommended groups when allocating subscriptions.
-   Manage subscriptions in an on-premise installation.
-   Manage custom application and table mapping through the platform, and learn why specific subscriptions are recommended when mapping custom tables and applications.
-   View subscribers by domain for user-based subscriptions.

See [Subscription Management](https://www.servicenow.com/docs/access?context=subscription-management-landing-page-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

**Important:** Subscription Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Subscription Management to Yokohama

Subscription Management version 4.1 is active by default on all instances of the Yokohama release. Update to Subscription Management version 6.0.2 or later to use the latest features. For more information about updating Subscription Management, see [Update an application or plugin](https://www.servicenow.com/docs/access?context=update-application-app-mgr&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## New in the Yokohama release

-   **[Subscription allocation counts according to active users](https://www.servicenow.com/docs/access?context=subscription-details-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    View the total number of active users in a product subscription. Only active users count toward the subscription allocation totals that appear throughout Subscription Management.

-   **[Allocate subscriptions to all recommended groups](https://www.servicenow.com/docs/access?context=allocate-subscriptions-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Select all recommended groups when allocating subscriptions.

-   **[Support for on-premises installation](https://www.servicenow.com/docs/access?context=configuring-subscription-management-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Manage subscription usage using Subscription Management on-premises.

-   **[Recommended subscription reasoning](https://www.servicenow.com/docs/access?context=addressing-issues-subscription-management-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Determine why Subscription Management displays a subscription recommendation when mapping custom tables or custom applications.

-   **[Manage custom applications and table mapping through the platform](https://www.servicenow.com/docs/access?context=allocating-custom-tables-subscr-apps-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Map any missing custom applications and tables in Subscription Management to a subscription directly from the Custom Applications list or Custom Table Inventory list.

-   **[Support for domain separation](https://www.servicenow.com/docs/access?context=domain-separation-subscription-mgmt&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    View and filter subscribers by domain for user-based subscriptions.


## Changed in this release

-   **[Allocation charts reflect only active users](https://www.servicenow.com/docs/access?context=subscription-details-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The Allocation summary and Allocation history charts on the subscription details page reflect only the subscriptions allocated to active users for each month following the upgrade.

-   **[Auditing App Engine V1 usage](https://www.servicenow.com/docs/access?context=allocating-custom-tables-subscr-apps-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The App Engine Usage dashboard has been restored. For details on auditing App Engine V1 usage, see the [Auditing App Engine v1 \[KB0999383\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0999383) article in the Now Support Knowledge Base.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Now Assist usage measurement is evolving. If your instances are below Yokohama Patch 12, update Subscription Management to version 6.0.2 or later on all instances to avoid mixed measurement types. For more information, see [Now Assist Usage - Overview &amp; New Measurement Logic \[KB2704710\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Hidden user-based subscription allocations](https://www.servicenow.com/docs/access?context=subscriptions-overview-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    To help prevent inaccuracy when allocations aren't complete, allocation details for user-based subscriptions are now hidden from the Subscription Management overview. Contact your account executive for user-based subscription allocation details.


## Removed in this release

The Custom tables chart has been removed from the subscription details page.

## Activation information

Subscription Management is a ServiceNow AI Platform feature that is active by default. Updates for Subscription Management are available through the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). For cumulative release notes information for applications available on the ServiceNow Store, see [ServiceNow Store release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

