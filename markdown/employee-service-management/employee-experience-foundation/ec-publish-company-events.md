---
title: Publishing company events
description: Company events can be published via a publish plan or using Content templates to auto-generate publish plans. These auto-generated publish plans are inactive by default and must be activated for company events to appear in the portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/ec-publish-company-events.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 2
breadcrumb: [Company events, Creating employee communications, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Publishing company events

Company events can be published via a publish plan or using Content templates to auto-generate publish plans. These auto-generated publish plans are inactive by default and must be activated for company events to appear in the portal.

## Before you begin

-   Role required: sn\_cd.content\_manager
-   Complete the steps to [Create a company event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/create-company-event.md)

## About this task

-   **Content templates**

    If you selected a Content template when you created the company event, the system generates the publish plans defined in the Content template. You can edit the auto-generated publish plans. The changes you make to publish plans don't impact the Content templates.

    **Note:** If the Content template is edited after the system auto-generated the publish plans, those changes aren't reflected in existing publish plans.

-   **Content availability vs Publish plans**

    Content availability defines when the content is available and the core audience who can access it. These parameters are set at the content item level.

    Publish plans determine how and where content is displayed in widgets. Publish plans specify the widget location, audience visibility \(which can expand the audience defined in content availability\), and the time-frame for displaying the content.

    **Note:** Publish plans don't override content availability date settings. If a publish plan displays content outside of availability parameters \(for example, before it is available\), users attempting to access the content will encounter a message such as "Sorry, this isn't available".

    To avoid this, content managers must verify that publish plan duration dates align with the content availability parameters.


## Procedure

1.  Navigate to the company event that you want to publish.

2.  Fill in the fields to define content availability:

    |Field|Description|
    |-----|-----------|
    |Content can be accessed starting|Determines the date and time when the content is available for viewing.|
    |Content cannot be accessed after|Determines the date and time after which the content is no longer available.|
    |Add audience|Define the users who can view the content.|

<table id="table_sg5_1k2_hkc"><thead><tr><th>

Tags

</th><th>

Tables

</th></tr></thead><tbody><tr><td>

sn\_kg\_tag

</td><td>

-   sn\_cd\_content\_base
-   sn\_cd\_content\_portal
-   sn\_cd\_content\_news
-   sn\_cd\_company\_event


</td></tr></tbody>
</table>3.  Select **Save availability**.

4.  Review the auto-generated publish plans and edit as necessary, such as to change the audience or publishing dates, or create publish plans: [Create a publish plan for your content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-publish2.md).

    **Note:** If you edit an auto-generated publish plan, ensure you select the **Active** option.

5.  Select **Activate generated plans**.


**Parent Topic:**[Company events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-company-events.md)

