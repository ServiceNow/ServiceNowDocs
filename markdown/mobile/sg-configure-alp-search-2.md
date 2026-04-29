---
title: Configure global search options for your screen launcher
description: Configure global search options, using the Zing search engine, to control how your app presents search results to your users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enable global search, Global search, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure global search options for your screen launcher

Configure global search options, using the Zing search engine, to control how your app presents search results to your users.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** menu and then search for the launcher screen where you want to add search functionality.

4.  In the Launcher Screen form, scroll down to the **Search configuration** section:

    1.  Select **Choose**.
    2.  In the Choose an item dialog box, select a search configuration, and then select **Apply**.

        If you aren't certain about which search configuration to choose, select **Preview** to view the configuration.

    3.  Select the search configuration that you chose, which launches the Search Config form.
    4.  In the Search Config form, locate the **Placeholder** section under **Properties**.
    5.  In the Placeholder text box, enter the text that you want to appear in the search bar before a user enters a value into the field, and then press Tab.

        ![Placeholder text box in Mobile App Builder](../image/global-search-placeholder-txt.png)

5.  In the **Settings** section, select **Interleave result** to display interleaved search results.

    If the option is not selected, search results are separated by the search source.

6.  Select **Save** in Mobile App Builder.

7.  To configure the maximum number of search suggestions that can be returned, navigate to the ServiceNow® instance web interface an follow the instructions in [Set the maximum number of search suggestions Zing displays](https://www.servicenow.com/docs/access?context=set-max-num-of-suggestions&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


## What to do next

Enable voice search so that your users can search using native speech recognition. For more details, see [Turn on voice search](../../mobile-employee/task/turn-on-voice-search.md)

