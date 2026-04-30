---
title: Schedule the Build Search Suggestions script
description: Specify when to run the script that builds auto-complete suggestions and search suggestions from user search strings.
locale: en-US
release: xanadu
product: Search Suggestions
classification: search-suggestions
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Search Suggestions, Search Suggestions, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Schedule the Build Search Suggestions script

Specify when to run the script that builds auto-complete suggestions and search suggestions from user search strings.

## Before you begin

Role required: admin

## About this task

Search Suggestions stores search strings entered by users in the Search Event \[sys\_search\_event\] table. The **Build Search Suggestions** script turns those search strings into auto-complete suggestions and search suggestions and stores them in the Search Suggestion \[sys\_search\_suggestion\] table.

By default, this script runs daily. You can customize how often and at what time the script runs. How often you run the script depends on how frequently you want to update suggestions for users. When you run the script might depend on performance considerations.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and select **Build Search Suggestions**.

2.  In the Scheduled Search Execution form, edit how often the script runs in the **Run** field.

3.  Edit the time of day the script runs in the **Time** field.

4.  Select **Update**.

5.  Select **Execute Now** to run the script immediately.


