---
title: Configure the app route to use an existing subpage
description: Create an app route to make an existing page a part of the page collection. For example, the dynamic related record is a global subpage that you can use at any application level.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook pages, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure the app route to use an existing subpage

Create an app route to make an existing page a part of the page collection. For example, the dynamic related record is a global subpage that you can use at any application level.

## Before you begin

Role required: admin

## About this task

Configuring an app route enables you to utilize an existing page in a page collection. This is applicable to both page templates and page variants.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **Page collection** tab and then select **CSM default record pre-tabs** from the Page Collections list.

3.  In the CSM default record pre-tabs page, select **View page collection settings** in the upper right corner.

4.  In the General section, select **Open page collection**.

    The system opens the UX Extension Point page for CSM default record pre-tabs.

5.  Navigate to the **UX App Routes** related list.

6.  Select **New** to create an app route.

7.  Enter a name In the **Name** field, a route in the **Route** field, and then select the **Screen Collection** that you want to reuse.

    The route is the path that the system uses to reach the page collection. For example, some common routes in CSM Configurable Workspace include record, list, and create\_case\_type for the Create Case modal.

    You can also create a screen collection by selecting **New** on the UX Screen Collections pop-up window and entering the name, route, and screen collection.

    ![Select a UX Screen Collections name or create a new one by selecting New.](../image/app-route-ux-screen-collection.png "UX Screen Collections pop-up window")

8.  Select **Submit** to create the app route.


## Result

The system adds the subpage to the page collection.

