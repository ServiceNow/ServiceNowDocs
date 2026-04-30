---
title: Upgrade search redirection to the new Now Mobile profile page
description: Upgrade to the new Now Mobile profile page for an enhanced user-navigational experience.
locale: en-US
release: zurich
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Employee profile for Now Mobile, Configuring Employee Center for mobile, Now Mobile experience for Employee Center, Now Mobile app, Unified Employee Experience, Employee Service Management]
---

# Upgrade search redirection to the new Now Mobile profile page

Upgrade to the new Now Mobile profile page for an enhanced user-navigational experience.

## Before you begin

Role required: admin

## About this task

Update the function instance manually to redirect ServiceNow® AI Search to the new Now Mobile profile page.

## Procedure

1.  Navigate to **System Mobile** &gt; **Now Mobile App** &gt; **Applet Launcher**.

2.  In the launcher screen list, select **Homepage**.

3.  Navigate to **Header** &gt; **Search config**.

4.  Select the **Preview this record** icon to open **Search config**.

5.  In the **Search config** page, go to the List Item Configuration list and select **People Genius Search Main Item**.

6.  In the People Genius Search Main Item list, go to **People genius result redirection**.

7.  Update the **Order** to **200** to prioritize search redirection to the Now Mobile profile page.

    **Note:** You can also update the **value** to **200** at `/sys_sg_button_instance.do?sys_id=510879044d0c2010f87749679b4774e8`


## Result

The search redirection takes you to the new Now Mobile profile page.

**Parent Topic:**[Employee profile for Now Mobile](../concept/my-team-widget-for-portal-and-mobile.md)

