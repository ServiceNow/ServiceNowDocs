---
title: Configure a list menu to display in the Learning tab in Workforce Optimization for Customer Service
description: Add list or list categories to modify the list menu for Coaching with Learning in the Coaching application in Workforce Optimization for Customer Service.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Workforce Optimization Coaching, Configure, Workforce Optimization for Customer Service, Customer Service Management]
---

# Configure a list menu to display in the Learning tab in Workforce Optimization for Customer Service

Add list or list categories to modify the list menu for Coaching with Learning in the Coaching application in Workforce Optimization for Customer Service.

## Before you begin

**Important:** This feature is available with the Workforce Optimization for CSM Configurable Workspace \(sn\_csm\_wfo\_workspa\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](request-configurable-wfo-cs.md).

Set the map application scope to **Coaching With Learning**. For information on how to set the scope, see [Set map application scope](https://www.servicenow.com/docs/access?context=set-map-application-scope&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Role required: admin

## Procedure

1.  In the application navigator, enter `sys_ux_list_menu_config.list`.

2.  Click **Learning list** record.

3.  Under UX list category, click **New**.

4.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |Title|Enter the name of the list category.|
    |Description|Enter a short description about the list category.|
    |Order|Enter a value to set the position of the list category in the current list.|
    |Active|Select the check box to make the list category visible.|

5.  Click **Submit**.

6.  Under UX Lists, click **New** to create lists under that list category.

7.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |Title|Enter the name of the list.|
    |Table|Select the table for the data that you want to display in the list.|
    |Configuration|Select **Learning List**.|
    |Columns|Select the columns that you want to display for the table.|

8.  Click **Submit**.

9.  Click **Update**.


**Parent Topic:**[Setting up Coaching in Workforce Optimization for Customer Service](../concept/setup-coaching-configurable-wfo-cs.md)

