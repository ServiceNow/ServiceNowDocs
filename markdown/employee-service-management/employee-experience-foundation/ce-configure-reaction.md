---
title: Configure a custom reaction
description: Content engagement utilizes font awesome icons to provide several out-of-the-box reactions for employees to interact with news articles. Engagement admins can customize the out-of-the-box reactions or configure their own.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Content engagement, Setup employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure a custom reaction

Content engagement utilizes font awesome icons to provide several out-of-the-box reactions for employees to interact with news articles. Engagement admins can customize the out-of-the-box reactions or configure their own.

## Before you begin

Role required: Engagement admin \[sn\_ce.admin\]

## About this task

The system supports a maximum of six reactions. To create a custom reaction, you can either upload an .SVG or .PNG image file or specify a Font Awesome version 4.7 icon.

## Procedure

1.  Navigate to **All** &gt; **Content Engagement** &gt; **Reaction Config**.

2.  Click **New**.

3.  Fill in the following fields:

<table id="table_ob2_j1s_wbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

System name for the reaction

</td></tr><tr><td>

Display text

</td><td>

Text that appears on the portal when the user hovers over or click a reaction icon

</td></tr><tr><td>

Font awesome icon

</td><td>

Name of the font awesome icon, as it appears on the website

</td></tr><tr><td>

Icon

</td><td>

Field to upload an .SVG or .PNG image file**Note:** If you enter a Font Awesome icon name in the previous field, you can skip this field.

</td></tr><tr><td>

Order

</td><td>

The order in which the icon appears when the user hovers over the **Like** icon on the portal relative to the other icons

</td></tr><tr><td>

Active

</td><td>

Makes the reaction available for users \(enabled by default\)

</td></tr></tbody>
</table>4.  Click **Submit**.

    The custom reaction appears in the **Reaction Configs** list.

5.  If you create a custom reaction, you must enable Content Publishing to access the reaction by creating an **App Reaction Config** record. You must repeat the following steps for each reaction that you want to make available to employees - including the out-of-the-box reactions.
6.  Navigate to **All** &gt; **Content Engagement** &gt; **App Reaction Config**.

7.  Click **New**.

8.  Fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |Reaction config|Select the reaction.|
    |Application|Connects the reaction with the application. This value is set at the Application scope.|
    |Active|Makes the reaction available for use.|
    |Order|The order in which the icon appears when the user hovers over the **Like** icon on the portal relative to the other icons|

9.  Click **Submit**.

    The reaction is now available for use in the portal.


