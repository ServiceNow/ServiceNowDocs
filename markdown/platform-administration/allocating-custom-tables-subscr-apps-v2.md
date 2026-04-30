---
title: Managing custom tables and applications in Subscription Management
description: Keep your custom table entitlements updated by mapping all of your custom applications and tables to valid subscriptions in Subscription Management.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Managing custom tables and applications in Subscription Management

Keep your custom table entitlements updated by mapping all of your custom applications and tables to valid subscriptions in Subscription Management.

## Overview of managing custom tables and applications

To successfully manage your custom tables and applications, follow the process in this infographic.

![The instance administrator maps custom applications and custom tables to subscriptions, and monitors end dates prior to renewal.](../image/MMASSET0020637-subscription-management-workflow-manage-tables-and-apps-landing.png "Managing custom tables and applications")

-   [Map a custom application to a product subscription in Subscription Management](../task/map-custom-applications-v2.md)

    Map a custom application to a product subscription so that when developers add more tables to the application, they're automatically mapped to the subscription. Track your custom table usage to ensure that your organization doesn't run out of custom table entitlements.

-   [Map custom tables to a product subscription in Subscription Management](../task/allocate-custom-table-subsc-app-v2.md)

    Map custom applications and custom tables on your production instance to a valid subscription. On non-production instances, mapping is recommended but not required.

-   [Maintain custom table and application mappings at renewal in Subscription Management](../task/maintain-mappings-renewal.md)

    When a subscription renews, a new product SKU might be added to your account. Maintain your current custom table mappings during the renewal process by documenting your mappings before the renewal date.


## Custom tables

A custom table is defined as a table that you create on the ServiceNow AI Platform that isn't provided by ServiceNow. Some tables are exempted from being classified as a custom table.

**Note:** For more information on custom tables on the ServiceNow AI Platform, see [Table administration](../../table-administration/concept/c_TableAdministration.md). For a detailed description of custom table use rights and exempt tables, see the Custom Table Guide on [http://www.servicenow.com/upgrade-schedules.html](http://www.servicenow.com/upgrade-schedules.html)

Subscriptions come with custom table entitlements that dictate the number of custom tables that you can map to a subscription. The number of custom table entitlements depends on the subscription.

## Custom applications

A custom application is defined as an application that you create on the ServiceNow AI Platform that isn't provided by ServiceNow. If your organization purchased App Engine, you can use Subscription Management to manage your custom application subscriptions.

## App Engine usage

App Engine subscriptions entitle you to develop applications and deploy custom tables in production instances. Based on your App Engine version, you monitor the subscription usage of your App Engine applications differently.

-   You can view and manage App Engine V2 subscriptions in Subscription Management just like any other product subscription. You can map your applications and custom tables to an App Engine V2 subscription and allocate per-user subscriptions by adding groups with measured roles to an App Engine V2 subscription.
-   You can't view App Engine V1 subscription details on the details page like other subscriptions. Users with the usage\_admin or admin roles can view App Engine V1 subscription details and usage information by navigating to the **App Engine usage** module from the filter navigator. This module only appears if you have App Engine V1.

    For details on auditing App Engine V1 usage, see [KB0999383](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0999383).


-   **[Map a custom application to a product subscription in Subscription Management](../task/map-custom-applications-v2.md)**  
Maintain accurate entitlement for custom tables in a scoped application by mapping the application to a product subscription in Subscription Management. To stay in compliance, you must map custom tables to a product subscription.
-   **[Map custom tables to a product subscription in Subscription Management](../task/allocate-custom-table-subsc-app-v2.md)**  
Maintain accurate entitlement for custom tables in the global scope and stay in compliance by mapping the tables to a product subscription in Subscription Management. Mapping your custom tables keeps your custom table allotment updated and helps you avoid running out of custom table entitlements.
-   **[Maintain custom table and application mappings at renewal in Subscription Management](../task/maintain-mappings-renewal.md)**  
Ensure custom table and application mappings remain consistent throughout the renewal process.
-   **[Grandfathered and exempted tables](../reference/grandfathered-and-exempt-tables-v2.md)**  
Grandfathered and exempted custom tables are treated differently than other custom tables on your instance. Please refer to your organization’s ServiceNow® contract for additional information.

**Parent Topic:**[Subscription Management](../reference/subscription-management-landing-page-v2.md)

