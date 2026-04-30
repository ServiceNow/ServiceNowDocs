---
title: Improve the image load time on Employee Center
description: Use CDN URLs to reduce the load time of the banner images, background images, and app icons on the Employee Center portal.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing portal performance, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Improve the image load time on Employee Center

Use CDN URLs to reduce the load time of the banner images, background images, and app icons on the Employee Center portal.

## Before you begin

Role required: esc\_admin

Enable the System Property \[sn\_ex\_sp.enable.image.url.support\] for the feature support on the Employee Center portal.

## About this task

You can manage the icon images, background images on the profile pages, banner images of the topic pages, by storing all of it in a local CDN server. It doesn't need to be fetched from the ServiceNow AI Platform® server.

The feature considerably improves the first load time of the graphics. The load time keeps improving as frequently you use and reload the pages.

The CDN URL support is available for the Popular topics, the Quick Links, and the My applications widgets.

**Note:**

-   My applications is only available with the Employee Center Pro license.
-   The ServiceNow AI Platform® provides support to create and manage your own CDN server and URL. The configuration and maintenance are the responsibility of the customer.

## Procedure

1.  Navigate to **All** &gt; **Content Taxonomy** &gt; **Topics**.

2.  Select a topic to update the **Icon URL** and the **Banner Image URL**.

    Update the **Icon URL** and the **Banner Image URL** from your local CDN server. This enables you to have enhanced load time and better accessibility to the images.

3.  Go to **All** &gt; **Content Taxonomy** &gt; **Quick Links**.

4.  Select and item to update the **Background image URL** and the **Icon URL** from your local server.

5.  Go to **All** &gt; **Employee Center** &gt; **Web Applications**.

6.  Select a web application to update the **Application icon URL**.

    **Note:**

    -   Popular topics and Quick links have base system preference set to the CDN URLs. If a URL image is available, the icons and images from the ServiceNow AI Platform® server are not used.
    -   My application has preferences set for the **Application icon**. You must delete the **Application icon** for the CDN URL to be detected and used.

**Parent Topic:**[Managing portal performance](../concept/improve-manage.md)

