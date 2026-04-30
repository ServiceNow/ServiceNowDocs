---
title: Configure a Core UI global landing page in Next Experience-enabled instances
description: Set a Core UI landing page for all users so users on instances with Next Experience enabled see the same landing page as users on upgraded instances. Upgraded users see the landing pages they had before in the Next Experience UI.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Next Experience landing pages, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configure a Core UI global landing page in Next Experience-enabled instances

Set a Core UI landing page for all users so users on instances with Next Experience enabled see the same landing page as users on upgraded instances. Upgraded users see the landing pages they had before in the Next Experience UI.

## Before you begin

Role required: admin

## About this task

Next Experience landing pages provide the information you need to start working. These landing pages typically present content specific to your role and tasks. Landing pages can include lists, Performance Analytics and Reporting \(PAR\) information, and other features to access your new and prioritized tasks from one location.

Values in the user preference **my\_home\_navigation\_page** override the value in the **glide.login.home** system property. If no user is specified in **my\_home\_navigation\_page**, the value in the preference overrides **glide.login.home** for all users.

## Procedure

1.  In the filter navigator field, enter `sys_properties.list`.

2.  Edit the value of the **glide.login.home** system property to set an instance-wide Core UI landing page.

    For example, to assign the Dashboards Overview as the landing page, you would enter `$pa_dashboard.do`. To assign a specific dashboard as the landing page, you would enter the portion of the URL from `$pa_dashboard.do` onward.

    **Note:** When you copy the URL information, be sure to replace HTML entities with their decoded values. For example, replace the entity `%24` with `$`.

    ![System Property glide.login.home form with a dashboard URL segment in the Value field](../image/set-ui16-landing.png)

3.  Select **Update**.

    You will not see the new landing page until you log out and log back in again.


## Result

When users log in, they see the selected landing page instead of the default.

**Parent Topic:**[Next Experience landing pages](../concept/next-experience-landing-pages.md)

