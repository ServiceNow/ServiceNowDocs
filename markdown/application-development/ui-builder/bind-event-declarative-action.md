---
title: Bind an event to a declarative action
description: Bind data elements within UI Builder so that you can add event actions to a declarative action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/bind-event-declarative-action.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Bind events to add actions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Bind an event to a declarative action

Bind data elements within UI Builder so that you can add event actions to a declarative action.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Bind a handled event to a component so that an action is performed when a user selects the component.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-experiences.md).

3.  Open or create a page.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-page.md).

4.  Add a component to your page that can have a declarative action, such as an action bar or related list.

    For more information, see [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/add-components.md).

5.  To create a declarative action definition in a table in the ServiceNow AI Platform®, navigate to **Workspace Experience** &gt; **Actions &amp; Components** &gt; **List actions**.

    Choose a table where you want the declarative action to be available in. For example, you could create a Complete my work action in an incident table or you could use an existing declarative action definition record.

    \[Omitted image "UIB-declarative-action-definition.png"\] Alt text: Platform declarative action definition record.

6.  Select the **Active** check box, and then save or update the record.

7.  Return to the UI Builder.

8.  To invoke a handled event for the declarative action, go to the Configure panel and click **Configure declarative action event mapping**.

    \[Omitted image "declarative-action-event-mapping-link.png"\] Alt text: Arrow pointing to the configure declarative action event mappings option.

9.  Choose the declarative action that you created earlier.

    To continue with the example in step [5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/bind-event-declarative-action.md), the declarative action could be something like **Complete my work**.

10. To define what the declarative action does on your page, click **+ Add event handler**.

    1.  Give the event handler a name.

        The name should describe what action you want the event handler to perform.

    2.  Provide a description of the event handler.

    3.  Choose the handled event that you want to invoke.

    4.  Add payload values for your event handler.

    5.  Select **Save**.

11. Select **Done**.

12. Select **Save**, and then select \[Omitted image "preview-button.png"\] Alt text: Preview button that opens the page variant..

13. Test the declarative action on your page by clicking **Complete my work** to see if it works.

    \[Omitted image "UIB-complete-my-work-button.png"\] Alt text: Complete my work button in UI Builder.


**Parent Topic:**[Bind events to add actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/bind-events.md)

