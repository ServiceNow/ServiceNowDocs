---
title: Configure per-user landing pages in Next Experience
description: Users on new Next Experience instances see the Next Experience landing page. Users on upgraded instances see the landing pages that they had before, in the Next Experience UI. You can also configure user-specific landing pages.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Next Experience landing pages, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configure per-user landing pages in Next Experience

Users on new Next Experience instances see the Next Experience landing page. Users on upgraded instances see the landing pages that they had before, in the Next Experience UI. You can also configure user-specific landing pages.

## Before you begin

Role required: admin

## About this task

Next Experience landing pages provide the information you need to start working. These landing pages typically present content specific to your role and tasks. Landing pages can include lists, Performance Analytics and Reporting \(PAR\) information, and other features to access your new and prioritized tasks from one location.

## Procedure

1.  Navigate to **User Administration** &gt; **User Preferences**.

2.  Select **New**.

3.  In the **Name** field, enter `my_home_navigation_page`.

4.  In the **User** field, select the Lookup using the list icon \(![Lookup using list icon.](../image/query-icon.png)\) and assign a user.

    You can have multiple entries of this preference for different users.

5.  Specify the value of the landing page.

    For example, to use the Visual Task Board overview as the landing page, you would enter `$vtb.do`. The value for any selected landing page is found within the URL. To assign a specific VTB, you would enter the portion of the URL from `$vtb.do` onward.

    **Note:** When you copy the URL information, be sure to replace any HTML entities with their decoded values. For example, replace the entity `%24` with `$`.

    ![User Preference my_home_navigation_page form with a VTB URL segment in the Value field](../image/set-indiv-ui16-landing.png)

6.  Select **Update**.


## Result

The user sees the specified landing page when they log on to ServiceNow® or when they select the company logo.

**Parent Topic:**[Next Experience landing pages](../concept/next-experience-landing-pages.md)

