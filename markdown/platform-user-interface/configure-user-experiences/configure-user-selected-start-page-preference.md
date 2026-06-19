---
title: Configure a user-selected start page
description: Configure a user-selected start page to override the administrator‑configured default landing page to appear when you log in to ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/configure-user-selected-start-page-preference.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Landing pages, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configure a user-selected start page

Configure a user-selected start page to override the administrator‑configured default landing page to appear when you log in to ServiceNow.

## Before you begin

Ensure you have enabled the Next Experience prior to beginning this task. For more information, see [Considerations for activating Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/next-experience-adoption-paths.md).

Role required: none

## Procedure

1.  The admin must enable the **glide.next\_experience.user\_selected\_landing\_page\_enabled** system property.

    1.  Select **All** to open the navigation filter, enter `sys_properties.list`, and press Enter to view the System Property table in list view.

    2.  Locate and open the **glide.next\_experience.user\_selected\_landing\_page\_enabled** property.

    3.  Verify that **Value** is set to true.

2.  In your instance, select the user menu \[Omitted image "pol-user-menu.png"\] Alt text: Next Experience user menu in the unified navigation..

3.  In the user menu list, select **Preferences**.

4.  Select the **User Experience** tile.

5.  Select the **Current start page** list.

6.  Choose your start page from these options.

    |Field|Description|
    |-----|-----------|
    |Use the default|The default landing page as configured by the administrator.|
    |Use Dashboards|If using Core UI responsive dashboards, the start page is set to the last dashboard you visited.|
    |Use the page that I'm on now|Set the current page as your default start page.|
    |Continue where I last left off|Set the last page you visited in ServiceNow as the start page when you next log in.|


**Parent Topic:**[Next Experience landing pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/next-experience-landing-pages.md)

