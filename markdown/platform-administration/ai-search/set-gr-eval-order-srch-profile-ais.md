---
title: Set the evaluation order for Genius Result configurations in a search profile
description: Change the order in which AI Search evaluates Genius Result configurations linked to a search profile.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Genius Results, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set the evaluation order for Genius Result configurations in a search profile

Change the order in which AI Search evaluates Genius Result configurations linked to a search profile.

## Before you begin

Role required: ais\_admin

## About this task

AI Search evaluates active Genius Result configurations for a search profile in an order determined by their numeric **Order** field values, as defined in the search profile's Genius Results related list. Genius Result configurations with lower **Order** field values are evaluated before those with higher field values. As an example, a Genius Result configuration with **Order** 100 is evaluated before one with **Order** 200.

**Note:** **Order** field values for linked Genius Result configurations are set separately for each search profile. A Genius Result configuration that's linked to multiple search profiles can have a different **Order** field value in each profile. For instance, you might set an **Order** value of 100 for the Q&amp;A Genius Result configuration in one search profile but set a value of 750 for the same Genius Result configuration in a second search profile that it's linked to.

A search application configuration's **Genius Results Limit** field value specifies the maximum number of Genius Result cards the application can display. For more details on search application configuration settings, see [Search Application Configuration form](../reference/search-app-config-form-ais.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to set the Genius Result configuration evaluation order for.

3.  In the Genius Results related list, edit the **Order** field values for Genius Result configurations linked to the search profile.

    For details on editing field values in the related list, see [Use the list editor](https://www.servicenow.com/docs/access?context=t_UseTheListEditor&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).


## What to do next

To make changes in the **Order** field values take effect, publish the search profile. For more information on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).

**Parent Topic:**[Genius Results](../concept/genius-results-ais.md)

