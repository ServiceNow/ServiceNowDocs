---
title: Configure Microsoft Teams Message Extension
description: Configure Microsoft Teams Message Extension to enable users to use AI Search to find content \(Knowledge articles and catalog items\), and share information in a one-on-one or group chat. For the base system Virtual Agent integration with Microsoft Teams, this feature is enabled by default.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure Microsoft Teams Message Extension

Configure Microsoft Teams Message Extension to enable users to use AI Search to find content \(Knowledge articles and catalog items\), and share information in a one-on-one or group chat. For the base system Virtual Agent integration with Microsoft Teams, this feature is enabled by default.

## Before you begin

Role required: admin

## About this task

Administrators have the option to configure the number of search results that appear in Message Extension and control the access level of a Guest user.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications** to configure the number of search results that appear in Message Extension.

2.  In the **Search Results Limit** field, adjust the number of search results that you want to appear in Messages Extension, and then select **Update**.

    Message Extension then generates the new results limit when a user performs a search if AI Search is able to find that number of results. For example, a limit may be set to 8 but if AI Search only finds 6 results, then 6 items are shown.

3.  Navigate to **All****&gt; System Properties****&gt; All Properties** and select **message\_extension\_guest\_access\_only** to control the access of the Guest user.

    When the flag is set to true, Message Extension returns the results that are only visible to the Guest users. Only the items that are publicly available are returned while the property is set to true. By default, this value is set to false, which means that a user can see all search results that they have access to. However, if you set the system property value to true, a user can only access the search results that are publicly available. This system property is useful if you want to avoid having a user accidentally sharing something that they shouldn't be sharing. You don't typically have to change the value. For self-configured bots, see the procedure in [Auto-generate the manifest file for uploading on Microsoft Teams](generate-manifest-file-msteams.md) for more information.


