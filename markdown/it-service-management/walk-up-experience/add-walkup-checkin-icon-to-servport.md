---
title: Configure Walk-up Experience online check-in icon to appear on Service Portal
description: Requesters can check into a walk-up location online via the Service Portal. You can edit the Service Portal Home page to replace the general IT Get Help support icon link with the Walk-up Experience online check-in support icon link.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Walk-up Experience, IT Service Management]
---

# Configure Walk-up Experience online check-in icon to appear on Service Portal

Requesters can check into a walk-up location online via the Service Portal. You can edit the Service Portal Home page to replace the general IT **Get Help** support icon link with the Walk-up Experience online check-in support icon link.

## Before you begin

Service Portal for Enterprise Service Management \(com.glide.service-portal.esm\) must be activated.

Role required: sp\_admin or admin

## About this task

To replace the Get Help icon link with the Walk-up Check-in icon link on the Service Portal Home page, access Service Portal Designer. Alternatively, you can add a new container to the Service Portal for the Walk-up Check-in icon link, so that the Get Help icon link remains.

![service portal with get help link](../image/ServicePortalGetHelp.png "Service Portal Home page with Get Help icon link")

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Click the **Designer** tile on the configuration page.

3.  Select the **Service Portal** index page to edit.

4.  Ensure you are in edit mode by verifying that **Edit** is highlighted as active in the Service Portal Designer banner.

    In edit mode, you can add a new container for the Walk-up Check-in icon link or edit an existing container, depending on where you want to place the icon link.

5.  To edit an existing container, select the **Get Help** icon link container.

6.  Click the edit icon in the upper right corner.

7.  Edit the form fields with the following data and presentation details.

    |Fields|Configuration input|
    |------|-------------------|
    |Data| |
    |Type|Select **Page** to embed the walkup\_online\_checkin page with widget on the icon link.|
    |Page|Select **walkup\_online checkin**.|
    |Presentation| |
    |Title|Enter `Walk-up Check-in`.|
    |Short description|Enter details about the icon link, that you want displayed, such as `Check in to an IT walk-up location to make a request or report a problem.`|
    |Bootstrap color|Select **Default**.|
    |Bootstrap class name|Enter a class name or leave this field empty.|
    |Glyph|Select a glyph or you can select the empty glyph to bypass this field.|
    |Template|Select **Circle Icon**.|

8.  Click **Save**.

    The Service Portal Home page opens in edit mode. The online Walk-up Check-in icon link with your selected glyph image and description displays in place of the former **Get Help** icon link.

    ![service portal with walk-up check-in link](../image/ServicePortalWalkupCheckin.png "Service Portal Home page with Walk-up Check-in icon link")

9.  Navigate to **Service Portal** &gt; **Service Portal Home** to verify and test the newly created Walk-up Check-in icon link.

10. To add the Walk-up Check-in icon link to a new container, refer to Create and edit a page using the Service Portal Designer.

11. Edit the container form fields with the same data and presentation information as detailed above in the form configuration input descriptions and follow the remaining relevant steps.


**Parent Topic:**[Configuring Walk-up Experience](../concept/walkup-experience-configuration.md)

