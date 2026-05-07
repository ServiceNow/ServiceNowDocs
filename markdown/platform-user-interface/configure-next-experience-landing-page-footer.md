---
title: Configure a Next Experience landing page footer
description: Display useful links in the footer of your Next Experience landing pages. The footer contains two fully configurable link set components.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Landing pages, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
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

2.  From the UI Builder home page, select **Experiences**.

3.  In the search experiences field, enter `Unified Navigation App`.

4.  In the Variants section, select the More options icon ![](../../ui-builder/image/three-dot-icon.png) for the Next Experience Landing Page - Admin Role and select **Duplicate**.

    The main variant of the landing page is read-only. To edit, you work in a copy.

    ![UI Builder Next Experience landing page more options menu with Duplicate highlighted](../image/duplicate-unified-nav-landing.png)

5.  In the variant creation modal, keep all fields as-is and select **Create**.

6.  In the Next Experience Landing Page - Admin Role Copy Content Body outline, select **Client State Parameters**.

7.  In the Client state parameters section, clear the **hideResourcesSection** initial value check box.

    This action enables the landing page footer.

    ![](../image/disable-hideresourcessection-param.png)

8.  Select the **Apply**.

    The default footer is visible with two link sets: Frequent visits and Learn more.

9.  To configure the links in the footer, select Link set 1 or Link set 2 under Container 5.

10. In the Config section, edit the links.

    For more information, see [Link set UIB Setup](https://developer.servicenow.com/dev.do#!/reference/now-experience/rome/shared-components/now-link-set/uib-setup) in the ServiceNow Developer documentation.


**Parent Topic:**[Next Experience landing pages](../concept/next-experience-landing-pages.md)

