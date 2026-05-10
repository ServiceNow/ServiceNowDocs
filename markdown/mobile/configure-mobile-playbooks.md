---
title: Configure mobile web screens with Mobile App Bridge
description: Configure mobile web screens with Mobile App Bridge to enable seismic pages, classic web pages, or service portal pages that are hosted within embedded web views. Using this feature, you can access native mobile functionality on ServiceNow mobile apps.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile App Bridge, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile web screens with Mobile App Bridge

Configure mobile web screens with Mobile App Bridge to enable seismic pages, classic web pages, or service portal pages that are hosted within embedded web views. Using this feature, you can access native mobile functionality on ServiceNow® mobile apps.

## Before you begin

Role required: admin

## About this task

This task is an example of embedding a seismic page, which contains the playbook experience, within a mobile app by using Mobile App Bridge.

Configure mobile web screens to leverage the ServiceNow platform playbook feature on mobile devices. A playbook guides technicians when troubleshooting issues or helps them learn to install new parts. For more information about the playbook feature, see [About Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-ui.md).

Configuring seismic pages with Mobile App Bridge involves the following tools and tasks:

-   Create a Now Experience Framework page in [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md) by leveraging the Mobile App Bridge.
-   Create a mobile web screen using Mobile App Builder \(MAB\).
-   Add the Now Experience Framework page to mobile devices by specifying the page URL in the **URL** field of the MAB mobile web screen configuration form.

For detailed information about adding a playbook to Mobile App Bridge so that you can configure a playbook on mobile devices on the ServiceNow Mobile Platform, see [Embed a playbook in ServiceNow® mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/embed-playbook-mobile.md).

**Important:** The Cabrillo JS API support that leverages Mobile App Bridge exists for classic web pages, service portal pages, and seismic pages. For more information about the Cabrillo JS APIs, see [Client mobile API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/api-client-mobile.md)+

## Procedure

1.  Create the Now Experience Framework page in UI Builder.

    For instructions about how to create the page, see [Create a Now Experience Framework page in UI Builder](mob-playbk-create-playbk-pg.md).

2.  Create the mobile web screen in MAB.

    For information about configuring a mobile web screen, see [Configure a mobile web screen](sg-configure-url-screen.md).

3.  Navigate back to the Now Experience Framework page you configured in UI Builder in Step 1 and in the upper right corner of the page, select **Preview** &gt; **Open URL path**.

    ![UI Builder user interface showing how to navigate to 'Preview > Open URL path' so you can copy the URL of the Now Experience Framework page.](../image/mob-playbk-config.png)

4.  Copy the URL that displays in your browser in UI Builder and then paste the URL into the **URL** field in the MAB Mobile Web Screen form.

    ![Mobile App Builder user interface showing the URL field in the Mobile Web Screen form.](../image/mob-playbk-paste-url.png)

5.  In MAB, select **Save**.


-   **[Create a Now Experience Framework page in UI Builder](mob-playbk-create-playbk-pg.md)**  
To configure mobile web screens that use Mobile App Bridge to leverage a playbook on mobile devices, the first step is to create a Now Experience Framework page in UI Builder.

**Parent Topic:**[Mobile App Bridge](../concept/mobile-playbooks.md)

