---
title: Configure non-default access to the experience switcher
description: Grant non-default roles access to the experience switcher so users can switch between development environments in ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/configure-access-experience-switcher.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Managing access to the experience switcher, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Configure non-default access to the experience switcher

Grant non-default roles access to the experience switcher so users can switch between development environments in ServiceNow Studio.

## Before you begin

Role required: admin

## About this task

By default, the Experience Configurations table \[sn\_udc\_experience\_configuration\] grants admins and delegated developers access to the experience switcher. To grant non-default roles access, add them to the Experience Visibility Controls table \[sn\_udc\_experience\_visibility\_control\]. For more information about default roles, see [Roles and access in app development tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-roles-and-access.md).

-   Admins and delegated developers can use the experience switcher because they may need access to any product where they've been delegated to administer or develop an app.
-   Creator Studio users and Creator Studio restricted users don't generally have access to the experience switcher because administrators limit them to a more curated experience.

## Procedure

1.  Navigate to **All** &gt; **sn\_udc\_experience\_visibility\_control.list**.

2.  Select **New**.

3.  Enter the experience you are configuring roles for.

    For example, enter `Serv` to select ServiceNow Studio.

4.  Specify the roles that should get access to the experience.

    1.  Unlock the **Available for roles** field by selecting the lock icon \[Omitted image "crs-purple-lock.png"\] Alt text:.

    2.  Start typing and then select the name of the role you're giving access to.

    3.  Lock the **Available for roles** field by selecting the unlock icon \[Omitted image "crs-purple-unlock.png"\] Alt text:.

5.  Specify the roles that should not have access to the experience.

    1.  Unlock the **Not available for roles** field by selecting the lock icon \[Omitted image "crs-purple-lock.png"\] Alt text:.

    2.  Start typing and then select the name of the role you're restricting access for.

    3.  Lock the **Not available for roles** field by selecting the unlock icon \[Omitted image "crs-purple-unlock.png"\] Alt text:.

6.  Select **Submit**.

    The role is added to the Experience Visibility Controls table and the specified users can now access the experience switcher.


**Parent Topic:**[Managing access to the experience switcher](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/managing-access-experience-switcher.md)

