---
title: Specify a login landing page
description: By default, users see their homepage upon login. You can specify a different login landing page by using a system property or the content management system.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Defining login scenarios, Local Authentication, Authentication, Access Management]
---

# Specify a login landing page

By default, users see their homepage upon login. You can specify a different login landing page by using a system property or the content management system.

## Before you begin

Role required: admin

## About this task

To specify a login landing page for all users, change the property value on the sys\_properties table.

## Procedure

1.  Type `sys_properties.list` in the navigation filter.

2.  Locate the **glide.login.home** system property.

3.  In the **Value** field, enter the name of the page that all users see upon login.

    Use `<page name>.do`; you may omit the `http://''instance''.service-now.com/` portion of the URL. To determine the page name or the URL of a page in the system, you can point to a link. Some possible pages are `welcome.do` and `incident.do`.

    To specify a dashboard landing page, set the property to `$dashboards.do?dashboard=<SYS_ID>`. Replace &lt;SYS\_ID&gt; with the sys\_id of the dashboard.

    To direct users to service portal, set the property to `/sp`

    **Note:** This property is system-wide, so setting it affects all users. To set a login specifically for users with no roles, you can apply these same steps and use the **glide.entry.loggedin.page\_ess** property.

    You can also specify a login landing page with the content management system.


