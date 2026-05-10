---
title: Subscription Management release notes
description: The ServiceNow Subscription Management application enables you to manage your subscriptions proactively and monitor subscription usage on your instances. Subscription Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Subscription Management release notes

The ServiceNow® Subscription Management application enables you to manage your subscriptions proactively and monitor subscription usage on your instances. Subscription Management was enhanced and updated in the Australia release.

## Subscription Management highlights for the Australia release

-   View and filter Now Assist usage by domain in domain-separated instances.
-   Monitor Workflow Data Fabric usage and view token use rate of each capability.

See [Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/subscription-management-landing-page-v2.md) for more information.

**Important:** Subscription Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Subscription Management to Australia

Subscription Management version 6.1 is active by default on all instances of the Australia release. Update to Subscription Management version 6.1 or later to use the latest features. For more information about updating Subscription Management, see [Update an application or plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/update-application-app-mgr.md).

## New in the Australia release

-   **[Support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/domain-separation-subscription-mgmt.md)**

    View and filter subscribers by domain for user-based subscriptions and view Now Assist usage by domain.

-   **[Monitor Workflow Data Fabric usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitoring-wdf-capability-use.md)**

    Monitor and track Workflow Data Fabric capability usage and view the relative token use rate of each capability.


## Changed in this release

-   **[Now Assist usage excludes demo data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Demonstration instances are excluded from the total Now Assist usage count to improve tracking of Assist consumption. The accrual time field displays when Now Assist data was last accrued.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Now Assist usage measurement is evolving. Update Subscription Management to version 6.1 or later on all instances to avoid mixed measurement states. For more information, see [Now Assist Usage - Overview &amp; New Measurement Logic: January 2026 \[KB2704710\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710) on the Now Support Knowledge Base.

-   **[Streamlined user-based subscription allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/managing-user-subscriptions-v2.md)**

    To simplify the Subscription Management experience, the manual allocation workflow for user-based subscriptions has been removed for administrators who have never used it. Administrators who have manually allocated user-based subscriptions before can still make manual allocations.

-   **[Hidden user-based subscription allocations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/subscriptions-overview-v2.md)**

    To help prevent inaccuracy when allocations aren't complete, allocation details for user-based subscriptions are now hidden from the Subscription Management overview. Contact your account executive for user-based subscription allocation details.


## Activation information

Subscription Management is a ServiceNow AI Platform feature that is active by default. Updates for Subscription Management are available through the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). For cumulative release notes information for applications available on the ServiceNow Store, see [ServiceNow Store release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

