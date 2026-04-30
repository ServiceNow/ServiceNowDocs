---
title: Make UI pages public or private
description: You can make pages public if you want your users to see the pages without logging in.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Defining login scenarios, Local Authentication, Authentication, Access Management]
---

# Make UI pages public or private

You can make pages public if you want your users to see the pages without logging in.

## Before you begin

Role required: admin

## About this task

Most pages are only viewable by logged in users. A limited number of pages are public so that users do not have to log in to view them, such as the welcome page, the front page, and the login and logout pages.

**Warning:** Several base system public pages are required for the functionality of many features. Do not disable base system public pages.

## Procedure

1.  In the application navigator filter, type `sys_public.list`.

2.  Click **New**.

3.  In the sys\_public table, create a record with the following values.

    |Field|Description|
    |-----|-----------|
    |Page|The name of the page. For example: $sp|
    |Active|When selected, the page is publicly accessible. Deselect the Active option when you want the page to be private.|

4.  Click **Save**.

    By setting active to true, the page is public, so anyone visiting `<instance_name>/sp` or `<instance_name>/$sp.do` can access the page.


