---
title: Integrate Live Feed with CMS
description: You can provide access to Live Feed from pages built in the Content Management System \(CMS\). For example, allow an end user to access your company feed via the ESS portal.
locale: en-US
release: xanadu
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure iFrames, Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Integrate Live Feed with CMS

You can provide access to Live Feed from pages built in the Content Management System \(CMS\). For example, allow an end user to access your company feed via the ESS portal.

## Before you begin

Role required: content\_admin or admin

## About this task

The ESS Portal template includes the **Portal - Live page** and **Live Feed** dynamic block \(requires the Live Feed plugin\). To provide access to Live Feed from CMS pages, [add the Live Feed dynamic block](t_AddContentToAPage.md) to a CMS page or include the **Portal - Live page** in a site.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Specialty Content** &gt; **iFrames**.

2.  Click **New**.

3.  Complete the iFrame block form with the following values.

    |Field|Input value|
    |-----|-----------|
    |Name|Type a unique name: `Live Frame`|
    |Frame name|Type a frame name: `live_frame`|
    |URL|Enter `https://instance name/live_feed.do?sysparm_doctype=true`. Replace instance name with your instance URL, for example, `<myinstance>.service-now.com`.|
    |Sizing|Select **Fixed Size** and enter height and width pixel dimensions according to the page on which you plan to display the feed. For example, enter a width of 1024 and height of 768.|

4.  Click **Submit**.

5.  Complete the steps in [Add the block to a page](t_AddContentToAPage.md).


**Parent Topic:**[Configure iFrames](t_IFrame.md)

**Related topics**  


[Content blocks](../concept/c_ContentBlocks.md)

[Configure a content block](t_CreateAContentBlock.md)

