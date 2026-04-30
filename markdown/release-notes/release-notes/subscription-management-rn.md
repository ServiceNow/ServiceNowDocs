---
title: Subscription Management release notes
description: The ServiceNow Subscription Management application enables you to manage your subscriptions proactively and monitor subscription usage on your instances. Subscription Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Subscription Management release notes

The ServiceNow® Subscription Management application enables you to manage your subscriptions proactively and monitor subscription usage on your instances. Subscription Management was enhanced and updated in the Zurich release.

## Subscription Management highlights for the Zurich release

-   Manage custom applications and table mapping through the custom application list and custom table inventory list.
-   View and filter subscribers by domain for user-based subscriptions in domain-separated instances.
-   View and filter Now Assist usage by domain in domain-separated instances.
-   Monitor Workflow Data Fabric usage and view token use rate of each capability.

See [Subscription Management](https://www.servicenow.com/docs/access?context=subscription-management-landing-page-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

**Important:** Subscription Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Subscription Management to Zurich

Subscription Management version 5.0 is active by default on all instances of the Zurich release. Update to Subscription Management version 6.1 or later to use the latest features. For more information about updating Subscription Management, see [Update an application or plugin](https://www.servicenow.com/docs/access?context=update-application-app-mgr&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## New in the Zurich release

-   **[Manage custom applications and table mapping through the platform](https://www.servicenow.com/docs/access?context=allocating-custom-tables-subscr-apps-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Map any missing custom application and tables in Subscription Management to a subscription directly from the Custom Applications list or Custom Table Inventory list.

-   **[Support for domain separation](https://www.servicenow.com/docs/access?context=domain-separation-subscription-mgmt&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    View and filter subscribers by domain for user-based subscriptionsand view Now Assist usage by domain.

-   **[Monitor Workflow Data Fabric usage](https://www.servicenow.com/docs/access?context=monitoring-wdf-capability-use&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Monitor and track Workflow Data Fabric capability usage and view the relative token use rate of each capability.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Assist usage excludes demo data](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Demonstration instances are excluded from the total Assist usage count to improve tracking of Assist consumption.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Now Assist usage measurement is evolving. If your instances are below Zurich Patch 6, update Subscription Management to version 6.0.2 or later on all instances to avoid mixed measurement states. For more information, see [Now Assist Usage - Overview &amp; New Measurement Logic \[KB2704710\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Hidden user-based subscription allocations](https://www.servicenow.com/docs/access?context=subscriptions-overview-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    To help prevent inaccuracy when allocations aren't complete, allocation details for user-based subscriptions are now hidden from the Subscription Management overview. Contact your account executive for user-based subscription allocation details.


## Activation information

Subscription Management is a ServiceNow AI Platform feature that is active by default.Updates for Subscription Management are available through the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). For cumulative release notes information for applications available on the ServiceNow Store, see [ServiceNow Store release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

