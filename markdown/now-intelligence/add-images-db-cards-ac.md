---
title: Add images to Platform Analytics dashboard cards
description: Distinguish the cards in the dashboard overview with uploaded images.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/add-images-db-cards-ac.html
release: zurich
topic_type: task
last_updated: "2023-11-09"
reading_time_minutes: 1
breadcrumb: [Edit a dashboard, Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Add images to Platform Analytics dashboard cards

Distinguish the cards in the dashboard overview with uploaded images.

## Before you begin

Role required: ui\_builder\_admin to enable the image preview; dashboard\_admin to add the image.

## About this task

Add an image to the cards in the Platform Analytics dashboard overview.

## Procedure

1.  Enable the image preview in the Dashboard overview component.

    1.  Navigate to **Now Experience Framework** &gt; **UI Builder**.

    2.  Change the application scope to Platform Analytics.

    3.  Select the Platform Analytics experience.

    4.  Open the Dashboard Library \(Default\) item.

    5.  In the outline, select **Dashboard overview 1**.

    6.  In the component configuration, select **Display image preview**.

        \[Omitted image "par-db-enable-image-preview.gif"\] Alt text: Short video showing how to enable image preview in UI Builder

2.  Navigate to `par_dashboard_user_metadata.list`.

3.  Select the **Preview record** icon \(\[Omitted image "InfoIcon.png"\] Alt text: info button\) next to the dashboard that you want to add an image to.

    \[Omitted image "par-db-metadata-info.png"\] Alt text: PAR Dashboard metadata list with preview record icon highlighted

4.  Select **Open Record**.

5.  Next to Card Image Preview, select **Click to add** to choose a card background image.

    There’s no limit on the size of the image that you can upload, but the card thumbnail area is 260 pixels wide by 110 pixels high.

6.  Choose an image file and select **OK**.

    The image appears on the form for the dashboard.

    \[Omitted image "par-db-metadata-upload.gif"\] Alt text: Short video showing how to select an image to upload for a dashboard card

7.  Select **Update**.


## Result

The image appears on the dashboard's card in the dashboard overview.

\[Omitted image "par-db-card-w-image.png"\] Alt text: Dashboard overview with one card featuring the uploaded image

**Parent Topic:**[Edit Platform Analytics dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/edit-db-in-ac.md)

