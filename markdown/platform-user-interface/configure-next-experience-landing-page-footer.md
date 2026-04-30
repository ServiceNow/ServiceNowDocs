---
title: Configure a Next Experience landing page footer
description: Display useful links in the footer of your Next Experience landing pages. The footer contains two fully configurable link set components.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Next Experience landing pages, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configure a Next Experience landing page footer

Display useful links in the footer of your Next Experience landing pages. The footer contains two fully configurable link set components.

## Before you begin

Role required: admin

## About this task

Next Experience landing pages provide the information you need to start working. These landing pages typically present content specific to your role and tasks. Landing pages can include lists, Performance Analytics and Reporting \(PAR\) information, and other features to access your new and prioritized tasks from one location.

The footer is hidden by default. To configure the footer, you enable it in UI Builder and then edit the link set components.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select **Unified Navigation App**.

3.  In the Variants section, select the More options icon \(![More options icon](../../ui-builder/image/three-dot-icon.png)\) for the Unified Navigation Landing Page - Admin Role and select **Duplicate**.

    The main variant of the landing page is read-only. To edit, you work in a copy.

    ![UI Builder unified navigation landing page more options menu with Duplicate highlighted](../image/duplicate-unified-nav-landing.png)

4.  In the Unified Navigation Landing Page - Admin Role Copy Content Body outline, select Container 5 and select the Client State Parameters icon \(![UI Builder client state icon](../../ui-builder/image/uib-client-state-icon.png)\).

5.  In the Client state parameters section, toggle the **hideResourcesSection** value off.

    This action enables the landing page footer.

    ![Animated gif of the Client state parameters dialogue section with the hideResourcesSection Initial value toggled on and then toggled off.](../image/disable-hideresourcessection-param.gif)

6.  Select the **X** to close the Client state parameters section.

    The default footer is visible with two link sets: Frequent visits and Learn more.

7.  To configure the links in the footer, select Link set 1 or Link set 2 under Container 5.

8.  In the Config section, edit the links.

    For more information, see [Link set UIB Setup](https://developer.servicenow.com/dev.do#!/reference/now-experience/rome/shared-components/now-link-set/uib-setup) in the ServiceNow Developer documentation.


**Parent Topic:**[Next Experience landing pages](../concept/next-experience-landing-pages.md)

