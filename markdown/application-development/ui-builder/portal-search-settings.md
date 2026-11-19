---
title: Show or hide the search settings for your portal experience
description: Show or hide the global search functionality on the public or private pages for your custom portal experience in UI Builder so that your users can search on the portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/portal-search-settings.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure UI Builder portal experiences, Configure how users interact with your applications in UI Builder, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Show or hide the search settings for your portal experience

Show or hide the global search functionality on the public or private pages for your custom portal experience in UI Builder so that your users can search on the portal.

## Before you begin

Role required: ui\_builder\_admin

You can control whether the global search functionality is visible to users of your portal experience. You can enable or disable the global search for either public or private pages.

You must be in the correct application scope to edit the experience settings. If you are in a different scope, the experience settings are read-only. To change your application scope, in the main header, select the application picker \(\[Omitted image "application-picker.png"\] Alt text: Application picker\), and then select the application scope. For more information about the application scope, see [Learn about security and roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/security-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open a portal experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md).

3.  Select **Experience settings** in the UI Builder header.

    \[Omitted image "portal-settings-toggle.png"\] Alt text: Arrow pointing to the settings toggle on the experience view page.

4.  Scroll down to **Global search**.

5.  Select the **Enable for public pages** or **Enable for private pages** to show or hide the global search in public or private pages.

    \[Omitted image "portal-settings-search.png"\] Alt text: Portal experience search settings.

6.  Click **Advanced settings** to go to the ServiceNow AI Platform to make changes to the application record on the ServiceNow AI Platform®.

    To enable or disable the search for a page, you must create a separate UX Page property. The UX Page property overrides the global search setting.

7.  Click **Save**.


**Parent Topic:**[Configure UI Builder portal experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/ui-builder-portal-settings.md)

