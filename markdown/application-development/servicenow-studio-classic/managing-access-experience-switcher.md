---
title: Managing access to the experience switcher
description: The experience switcher can provide access to Creator Studio, ServiceNow Studio, ServiceNow IDE. However, whether you can see and select all of those depends on your role or access level.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/managing-access-experience-switcher.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Managing access to the experience switcher

The experience switcher can provide access to Creator Studio, ServiceNow Studio, ServiceNow IDE. However, whether you can see and select all of those depends on your role or access level.

There are several factors that determine what you can choose from the experience switcher: your role, whether the selected studio is installed on the instance, and which version is installed.

## How do roles control access to the experience switcher?

Your role — including user group and security level — determines which products are accessible in the experience switcher.

The following describes default role access to the experience switcher:

-   Admins and delegated developers can use the experience switcher because they may need access to any product where they've been delegated to administer or develop an app.
-   Creator Studio users and Creator Studio restricted users don't generally have access to the experience switcher because administrators limit them to a more curated experience.

Admins can check the Experience Configurations table \[sn\_udc\_experience\_configuration\] to see which default roles have access to each product in the experience switcher. The table also shows which roles see the discovery page that appears if Creator Studio is not installed or is below the minimum version required for the experience switcher.

**Important:** Regardless of your role — including admin and delegated developer roles — if you have a Creator Studio role, you cannot access ServiceNow Studio or ServiceNow IDE.

To grant non-default roles access to products in the experience switcher, update the Experience Visibility Controls table \[sn\_udc\_experience\_visibility\_control\]. For more information, see [Configure non-default access to the experience switcher](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/configure-access-experience-switcher.md).

## Product installation determines access

You must have an application installed on the instance to select it from the experience switcher.

For example, if you're working in ServiceNow Studio or ServiceNow IDE but don't have Creator Studio installed, selecting Creator Studio in the experience switcher displays a page where you can find out more on using Creator Studio.

## Product version determines access

To appear in the experience switcher, all products must be on the Yokohama version at a minimum.

For example, if you choose Creator Studio in the experience switcher but have the Xanadu version of Creator Studio installed, selecting it displays a page directing you to update the version.

-   **[Configure non-default access to the experience switcher](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/configure-access-experience-switcher.md)**  
Grant non-default roles access to the experience switcher so users can switch between development environments in ServiceNow Studio.

**Parent Topic:**[Configuring ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/configuring-servicenow-studio.md)

