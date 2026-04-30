---
title: Configure the main tag on a page
description: Specify the main content of a page to include in the &lt;main&gt; tag to improve search engine optimization and accessibility.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Improving search engine optimization for portals, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure the main tag on a page

Specify the main content of a page to include in the **&lt;main&gt;** tag to improve search engine optimization and accessibility.

## Before you begin

Role required: sp\_admin or admin

## About this task

The **&lt;main&gt;** tag is a semantic HTML element that contains the main content of the page. The **&lt;main&gt;** tag should be applied to content that is unique to the page and should be configured for only one element on the page.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  Select a page.

4.  Switch to the portal you want to design pages for by selecting the portal name in the header.

    ![Service Portal Designer header with the portal name SP highlighted](../image/DesignerSwitchPortal.png)

5.  Select a container, row, or column on the page that contains the main content of the page.

    See the breadcrumbs in the header to confirm you have the correct element selected. You can’t add the **&lt;main&gt;** tag to a widget.

6.  Select the edit icon \[![Edit icon](../image/IconEditOption.png)\].

7.  In the **Semantic tag** field, select **Main**.

8.  Select **Save**.


## Result

In the HTML of the page, the **&lt;main&gt;** tag contains the container, row, or column. In Service Portal Designer, a **&lt;main&gt;** tag displays in the bottom-right corner of the element.

![Main tag](../image/main-tag.png)

**Parent Topic:**[Improving search engine optimization for portals](../concept/seo-sp.md)

