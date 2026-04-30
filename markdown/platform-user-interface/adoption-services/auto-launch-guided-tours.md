---
title: Configure auto-launch for Guided Tours
description: Configure one or more tours to launch automatically when a user lands on a page.
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Configure auto-launch for Guided Tours

Configure one or more tours to launch automatically when a user lands on a page.

## Before you begin

Role required: guided\_tour\_admin and embedded\_help\_admin, or admin

**Note:** Guided tours are only available for logged-in users.

## About this task

You can set auto-launch for any guided tour starting page. Select this option if you want users to take the tour on their first visit.

## Procedure

1.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Configure Auto Launch**.

    The Configure Auto Launch page shows tiles for each page that has one or more configured tours. You can filter the tiles by part of or the entire page name, and sort them by name or by the most recently edited tours.

2.  Select a tile that represents the page where you want the tour to launch automatically.

    ![Configure the auto-launch page with filtered and sorted results](../image/configure-autolaunch-L.png)

    A list of tours available for the page is shown on the Configure Auto Launch screen.

    ![Show users a tour in draft status with auto-launch disabled](../image/configure-autolaunch-graydraft-L.png)

    You can enable or disable auto-launch on the tour whether it is in draft or published status. When you enable auto-launch:

    -   Tours in published status launch automatically when users access the starting page associated with the tour.
    -   Tours in draft status don’t launch automatically. When a tour in draft state is configured for auto-launch and is published later on, it starts to launch automatically.
3.  Select the **Auto Launch** toggle.

    ![Show users a tour in draft status with auto-launch enabled](../image/configure-autolaunch-greendraft-L.png)

    The toggle color changes to green, indicating auto-launch is enabled on the tour.

4.  Configure auto-launch for more than one tour on a page.

    If you have more than one tour enabled on a page, they appear as additional rows.

    ![Show users tours with auto-launch enabled, disabled, published, and in draft](../image/configure-autolaunch-draftnpub-L.png)

    1.  Repeat steps 2–3 for additional tours that you want to enable for auto-launch.

        The tours move to the top of the list in the order that you enable them.

    2.  Drag rows to reorder the tours so they appear in the order you want users to see when they visit the page successive times.

        For example, the first tour may provide an overview of a page while the second tour guides the user through a specific task.

    When users access a page that has a guided tour enabled for auto-launch, the tour begins immediately. If they stop the tour by selecting the **X** icon on a tour step, a message appears that provides them with the option to stop both the current tour and other tours from auto-launching the next time they access the page.

    ![Show how end users can stop a tour from launching on a page](../image/configure-autolaunch-stoptour-L.png)

    ![Show how end users can stop all tours from launching on a page](../image/configure-autolaunch-stopalltours-L.png)

5.  Reset an auto-launch tour for the page.

    After you’ve gone through a tour on a page, the tour doesn't get triggered automatically if you revisit the same page. Reset an auto-launch tour for the page by performing the following steps:

    1.  Navigate to **All** &gt; **Guided Tours**.

    2.  Open the tour that you want to reset.

    3.  Under **Related Links**, select **Override tour Auto Launch Preferences**.

        A list of records shows each user who has used the tour already.

    4.  Deselect the **Disable Autolaunch** check box to reset the tour.

    5.  Select **Submit**.


**Parent Topic:**[Configuring Guided Tours](configure-guided-tours.md)

