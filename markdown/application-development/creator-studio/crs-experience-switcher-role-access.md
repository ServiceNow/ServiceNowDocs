---
title: Administering access to the experience switcher
description: The experience switcher can provide access to Creator Studio, ServiceNow Studio, ServiceNow IDE. However, whether you can see and select all of those depends on your role or access level.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Administering Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Administering access to the experience switcher

The experience switcher can provide access to Creator Studio, ServiceNow Studio, ServiceNow IDE. However, whether you can see and select all of those depends on your role or access level.

There are several factors that determine what you can choose from the experience switcher: your role, whether the selected studio is installed on the instance, and which version is installed.

## Roles determine access

What role you have, such as user group and security levels, enables access to products in the experience switcher.

The following describes default role access to the experience switcher:

-   Admins and delegated developers can use the experience switcher because they may need access to any product where they've been delegated to administer or develop an app.
-   Creator Studio users and Creator Studio restricted users don't generally have access to the experience switcher because administrators limit them to a more curated experience.

Admins can check the Experience Configurations table \[sn\_udc\_experience\_configuration\] to see which default roles have access to each of the products in the experience switcher. The table also shows which roles will see the discovery page that appears if Creator Studio isn't installed, or isn't the minimum version needed for the experience switcher.

If you want to give more roles access to products in the experience switcher, you must do so in the Experience Visibility Controls table \[sn\_udc\_experience\_visibility\_control\]. For more information, see [Edit a role's access to the experience switcher](../task/crs-edit-role-access-experience-switcher.md).

## Product installation determines access

You must have an application installed on the instance to select it from the experience switcher.

For example, if you're working in ServiceNow Studio or ServiceNow IDE but don't have Creator Studio installed, selecting Creator Studio in the experience switcher displays a page where you can find out more on using Creator Studio.

## Product version determines access

To appear in the experience switcher, all products must be on the Yokohama version at a minimum.

For example, if you choose Creator Studio in the experience switcher but have the Xanadu version of Creator Studio installed, selecting it displays a page directing you to update the version.

-   **[Edit a role's access to the experience switcher](../task/crs-edit-role-access-experience-switcher.md)**  
Add more roles to the Experience Visibility Controls table \[sn\_udc\_experience\_visibility\_control\] to give them access to other products in the experience switcher, such as ServiceNow Studio.

**Parent Topic:**[Administering Creator Studio](administering-creator-studio.md)

