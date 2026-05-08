---
title: Domain separation for Platform Analytics dashboards
description: Domain separation is supported throughout Platform Analytics. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Domain separation for Platform Analytics dashboards

Domain separation is supported throughout Platform Analytics. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see Application support for domain separation.

## Overview of domain separation

 To activate the domain separation plugin, see Request domain separation.

**Important:** For users in child domains to view dashboards in parent domains, both domain separation and delegated administration must be enabled.

Users in child domains cannot overwrite dashboards. Child domain users only have read access to dashboards.

## How domain separation works in Dashboards

Assumptions:

-   Only dashboards that have been shared are visible to other users. See [Share a responsive dashboard](../task/t_ControlAccessToADashboard.md).
-   Users granted edit permissions on a dashboard can only edit that dashboard if they are in the same domain as the dashboard. For example, a user who is in the HR domain cannot edit a dashboard created in the parent of the HR domain.

Dashboard data that is domain separated includes dashboard records, dashboard tabs, and widget containers. Widget content is governed by the domain separation that applies to the content itself. For example, an admin adds a report created in the HR domain to a dashboard in the IT domain. This report is not visible to users in the IT domain, although they can see the widget container.

A dashboard defined at the global level is visible to all users with whom it has been shared. A shared dashboard created in a parent domain is visible to users in the parent and all its child domains. For example, a dashboard created in the TOP company is visible to users in:

-   Joe's company
-   Other companies in the TOP company
-   All HR, CS, and IT child domains in those companies if it is shared with those users.

In the following figure, dashboards created in the IT, CS, and HR domains are not visible to users in the other child domains or in the parent domain.

![List of company departments in separate domains including IT, CS, and HR](../../reporting/image/domains-list-example.png "Domains list example")

**Important:** Administrators should not edit a domain-separated dashboard from the global domain, because additions made to the dashboard are not visible to users within the separated domain. When editing dashboards, make sure that you are logged in to the correct domain.

**Related topics**  


[bundle-psec.c_DomainSeparation]

[bundle-psec.bp-domain-sep-recommended]

