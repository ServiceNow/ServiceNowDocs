---
title: Domain separation and Subscription Management
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Subscription Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Subscription Management, Get started, Administer]
---

# Domain separation and Subscription Management

Domain separation is supported for Subscription Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic\*

The support level is Basic but has some exceptions or special conditions.

-   Business logic: Ensure that data goes into the proper domain for the application’s service provider \(SP\) use cases.
-   The user interface, cache keys, reporting, rollups, and aggregations all use the domain at production run time.
-   The owner of the instance must be able to set up the application to function across multiple tenants.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Overview of domain separation inSubscription Management

Subscription Management enables you to manage your subscriptions and monitor subscription usage on your instances. Domain separation is enabled for user-based subscriptionsand for monitoring Now Assist usage.

**Note:** This feature is only available in domain-separated instances. This feature isn't visible in instances without domain separation.

## How domain separation worksfor user-based subscriptions in Subscription Management

In domain-separated instances, Subscription Management provides information about the domain of each user that has been allocated a user-based subscription.

Users in the SP domain can view the domains that each of their tenant users is a part of from the **Subscribed users** tab of subscription details. The **Domain** column shows the domain hierarchy of all child and grandchild domains and enables you to filter subscribed users by domain.

Users in tenant domains can only view subscription allocations from the global domain and domains that their organization manages. Users in tenant domains can't see user subscription allocations from parent or sibling domains.

**Note:** User records created before domain separation is activated are in the global scope until manually assigned a domain. Subscription allocations to global users are visible in all domains.

The Allocation Summary section in the subscription details displays information based on the total number of subscription allocations available across all domains. Administrators can use this information to help avoid over-allocating user subscriptions in tenant domains.

If you make allocation changes that aren't reflected in the Allocation Summary or Allocation History, clear the cache.

## Monitoring Now Assist usage by domain

In domain-separated instances with Now Assist, Subscription Management provides information about assist usage by domain.

Users in the SP domain can view assist usage by domain by navigating to **Admin** &gt; **Subscription Management** &gt; **Subscriptions** &gt; **Account level entitlements** &gt; **NowAssist usage** and reviewing the current instance details.

Users in tenant domains can only view their own Now Assist usage. Users in tenant domains can't see the number of assists used in parent or sibling domains.

**Parent Topic:**[Subscription Management reference](subscription-management-reference-v2.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

