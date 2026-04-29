---
title: Enable the page route map
description: If you have upgraded your instance, redirect your HR ticket pages to the Standard Ticket page in Portal. View your HR requests in the Standard Ticket Page view.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Standard Ticket Page view for HR Service Delivery, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Enable the page route map

If you have upgraded your instance, redirect your HR ticket pages to the Standard Ticket page in Portal. View your HR requests in the Standard Ticket Page view.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Page Route Maps**.

2.  Create the page route map from **hrm\_ticket\_page** to **standard\_ticket**.

    **Note:** **hrm\_ticket\_page** is available only when you have the Employee Center \[com.sn\_hr\_service\_portal\] plugin.

    ![Page route mapping](enable-page-route-hr.png)

3.  Create the page route map from **hrsp\_ticket** to **standard\_ticket**.

    **Note:** **hrsp\_ticket** is available only when you have Human Resources Scoped App: Core \[com.sn\_hr\_core\] plugin, without the Employee Service Center \[com.sn\_hr\_service\_portal\] plugin.

    ![Page route mapping](enable-page-route-hr2.png)

4.  Create the page route map from **ticket** to **standard\_ticket**.

    **Note:** **ticket** is available only Non-HR catalog items.

    ![Page route mapping](enable-page-route-hr3.png)


**Parent Topic:**[Standard Ticket Page view for HR Service Delivery](../concept/ur-hr-standard-ticket-page.md)

