---
title: Add slides to the carousel widget
description: Use the related lists for an instance of the carousel widget to add images for the carousel widget to scroll through.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Carousel widget, Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Add slides to the carousel widget

Use the related lists for an instance of the carousel widget to add images for the carousel widget to scroll through.

## Before you begin

Role required: Admin or sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Widgets**.

2.  Open the **Carousel** widget record.

3.  From the carousel form, on the **Instances** related list, under instances, open a carousel instance.

4.  From the instance of carousel form, click **New** on the **Carousel Slides** related list.

5.  Complete the form.

    ![New Carousel slide form completed similarly to the iPhone record for the SC carousel widget](../image/AddCarouselSlide.png)

    |Field|Description|
    |-----|-----------|
    |Name|Name of the carousel slide. Use the name to differentiate the slide from other slide records.|
    |Order|Where the slide appears in the list of slides|
    |HREF/URL|Link to the item in the slide. For example, for a slide with a catalog item, link to page for the catalog item using the HREF `?id=<page name>&sys_id=<sys_id for item>`. For more information on linking to a page within a portal, see [Page navigation in Service Portal by URL](../concept/navigate-by-portal-url.md). You can also link to other sites using the URL.|
    |Background|Upload an image for the slides. Carousel images should be 1022x300 pixels.|
    |Application|Automatically populated with the name of the application the portal falls under.|
    |Carousel|Name of the instance of the carousel widget you are adding the slide to. This field is not automatically populated and you cannot select an instance of the carousel widget if it does not have a name.|

    Repeat this step for as many slides as you want to appear in the carousel widget.


**Parent Topic:**[Carousel widget](../concept/carousel-widget.md)

