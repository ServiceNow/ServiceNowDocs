---
title: Publishing news articles
description: News articles can be published via a publish plan or using Content templates to auto-generate publish plans. These auto-generated publish plans are inactive by default and must be activated for News articles to appear in the portal.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [News articles, Creating employee communications, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Publishing news articles

News articles can be published via a publish plan or using Content templates to auto-generate publish plans. These auto-generated publish plans are inactive by default and must be activated for News articles to appear in the portal.

## Before you begin

-   Role required: sn\_cd.content\_manager
-   Complete the steps to [Create a news article](ec-content-library-news-article.md)

## About this task

-   **Content templates**

    If you selected a Content template when you created the news article, the system generates the publish plans defined in the Content template. You can edit the auto-generated publish plans. The changes you make to publish plans do not impact the Content templates.

    **Note:** If the Content template is edited after the system auto-generated the publish plans, those changes are not reflected in existing publish plans.

-   **Content availability vs Publish plans**

    Content availability defines when the content is available and the core audience who can access it. These parameters are set at the content item level.

    Publish plans determine how and where content is displayed in widgets. Publish plans specify the widget location, audience visibility \(which can expand the audience defined in content availability\), and the timeframe for displaying the content.

    **Note:** Publish plans do not override content availability date settings. If a publish plan displays content outside of availability parameters \(for example, before it is available\), users attempting to access the content will encounter a message such as "Sorry, this isn't available".

    To avoid this, content managers must ensure that publish plan duration dates align with the content availability parameters.


## Procedure

1.  Navigate to the News article that you want to publish.

2.  Fill in the fields to define content availability:

    |Field|Description|
    |-----|-----------|
    |Content can be accessed starting|Determines the date and time when the content is available for viewing.|
    |Content cannot be accessed after|Determines the date and time after which the content is no longer available.|
    |Add audience|Define the users who can view the content.|

3.  Click **Save availability**.

4.  Review the auto-generated publish plans and edit as necessary, such as to change the audience or publishing dates, or create new publish plans: [Create a publish plan for your content](ec-content-library-publish2.md).

    **Note:** If you edit an auto-generated publish plan, ensure you select the **Active** option.

5.  Click **Activate generated plans**.


## What to do next

If you edit a news article after publishing it and want to change the publish start date, you must generate new publish plans.

