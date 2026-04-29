---
title: Configure a guidance preview experience
description: Configure a preview experience that conveys relevant information about the guidance action to the agent before a recommendation is triggered. This information appears on the Recommended Actions card in the contextual side panel.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating guidance and field recommendation in Recommended Actions, Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Configure a guidance preview experience

Configure a preview experience that conveys relevant information about the guidance action to the agent before a recommendation is triggered. This information appears on the Recommended Actions card in the contextual side panel.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, admin

## About this task

A guidance preview includes the following elements:

-   A title
-   Fields to display
-   A message made up of text and HTML content, including images, videos, and links

You must configure at least one of these elements to save the guidance preview. This action prevents the guidance from appearing empty in the contextual side panel.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Action Types** &gt; **Guidances**.

2.  Select a guidance from the **Guidances** list.

3.  Select the **Preview Experience** tab.

4.  In the **Preview Title** field, add a title for the guidance preview.

    This field can contain static text, dynamic content \(field values from guidance inputs\), or a combination of static text and dynamic content. To select dynamic content as a field value:

    1.  Select the pill picker icon next to the **Preview Title** field.
    2.  Select a guidance input from the list. You can drill down to another level to find the input you want.

        ![Search bar listing a guidance input.](../image/ra-csm-guidance-preview-title.png)

5.  Select fields to display in the guidance preview.

    1.  In the **Fields To Display** field, click the lock icon to unlock the field.

    2.  Move the required fields from the **Available** column to the **Selected** column.

        You can select up to four fields.

    3.  Use the up and down arrows to arrange the selected fields.

    4.  Click the lock icon again to lock the field.

6.  In the **Message** field, create a message for the guidance preview.

    You can use the tools available in the rich text editor to create and format the message. This field can include text and HTML content like images, videos, and links.

7.  Click **Submit**.


