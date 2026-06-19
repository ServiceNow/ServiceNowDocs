---
title: Display global search in a workspace experience
description: Show or hide the search functionality in your workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/workspace-global-search.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure UI Builder workspace experiences, Configure how users interact with your applications in UI Builder, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Display global search in a workspace experience

Show or hide the search functionality in your workspace.

## Before you begin

Role required: ui\_builder\_admin

## About this task

You can control whether the search functionality is visible to the users of your workspace experience. If you choose to display a search option, you can define what search results are returned by choosing a source for the search.

\[Omitted image "experience-utilities-settings.png"\] Alt text: Workspace experience utility settings.

Before you can edit the experience settings, you must be in the correct application scope. If you're in a different scope, the experience settings are read-only. To change your application scope, go to the main header, select the application picker \(\[Omitted image "application-picker.png"\] Alt text: Application picker.\), and then select the application scope that you want. For more information about the application scope, see [Learn about security and roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/security-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-experiences.md).

3.  Open or create a page in your workspace experience.

4.  Select **Experience settings** in the upper-right.

    \[Omitted image "experience-settings-navigation.png"\] Alt text: Arrow pointing to the Experience settings link on the experience view page.

5.  Scroll down to **Global search**.

    \[Omitted image "uib-settings-search.png"\] Alt text: Global search settings for workspace experiences.

6.  Select the **Show global search** option.

7.  Click **Save**.

8.  Click **Advanced settings** to go to the ServiceNow AI Platform® and edit the JSON values of the record.


**Parent Topic:**[Configure UI Builder workspace experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-workspace-settings.md)

