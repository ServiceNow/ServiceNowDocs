---
title: Configure a list menu to display in the Learning tab in Workforce Optimization for Field Service
description: Add list or list categories to modify the list menu for Coaching with Learning in the Coaching application in Workforce Optimization for Field Service.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up coaching in Workforce Optimization for Field Service, Configuring Workforce Optimization for Field Service, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Configure a list menu to display in the Learning tab in Workforce Optimization for Field Service

Add list or list categories to modify the list menu for Coaching with Learning in the Coaching application in Workforce Optimization for Field Service.

## Before you begin

Set the map application scope to **Coaching With Learning**. For more information, see [Set map application scope](https://www.servicenow.com/docs/access?context=set-map-application-scope&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

Role required: admin

## Procedure

1.  In the application navigator, enter `sys_ux_list_menu_config.list`.

2.  Click the **Learning list** record.

3.  Under the UX list category, click **New**.

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


