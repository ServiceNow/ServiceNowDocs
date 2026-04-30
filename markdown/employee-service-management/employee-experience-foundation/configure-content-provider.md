---
title: Configure content provider and mapping
description: Connect a video hosting service to Content Publishing by configuring a content provider, then mapping the hosting service to specific content types, including rich content, news article, and styled content.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Video hosting integrations framework, Setup employee communications, Configure, Employee Center, Employee Service Management]
---

# Configure content provider and mapping

Connect a video hosting service to Content Publishing by configuring a content provider, then mapping the hosting service to specific content types, including rich content, news article, and styled content.

## Before you begin

Role required: sn\_cd.content\_admin

## Procedure

1.  Create a new content provider record to identify the hosting service.
2.  Navigate to **All** &gt; **Content Publishing** &gt; **Content Provider Configs** &gt; **Content Providers**.

3.  Click **New**.

    Fill in the form fields:

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name to identify the content provider when creating content in the Content Library|
    |Type|Select **Video** to connect to a video hosting service|
    |Active|Makes this content provider available for use in the Content Library|

4.  Click **Submit**.

    The system creates a new record for the content provider. You can view or edit it by navigating to **All** &gt; **Content Publishing** &gt; **Content Provider Configs** &gt; **Content Providers**.

5.  Add one or more content provider mappings to make videos available in specific content types.
6.  If you are already on the Content Providers page, click the Content Provider to add mappings.

    Otherwise, navigate to **All** &gt; **Content Publishing** &gt; **Content Provider Configs** &gt; **Content Provider Mapping**.

7.  Click **New**.

    Fill in the form fields:

<table id="table_hsx_z4p_lzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content provider

</td><td>

Select the name of the Content provider you defined in the previous steps

</td></tr><tr><td>

Content type

</td><td>

Select a content type to use the video content. Choose from:-   Rich content
-   News articles
-   Banner


</td></tr><tr><td>

Active

</td><td>

Makes this content provider available for use in the specific content type

</td></tr></tbody>
</table>8.  Click **Submit**.


## What to do next

-   Enable employees to view private videos without providing credentials: [Configure a video authorization](configure-content-processor.md)
-   To provide content managers with an interface where they can select a video, [Configure video content search](configure-content-search.md)
-   To add interface elements to the Content Library video picker, [Configure content rendering parameter](configure-content-rendering-parameter.md)

