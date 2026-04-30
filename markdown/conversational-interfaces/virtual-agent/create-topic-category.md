---
title: Create or modify custom categories
description: Create or change custom categories for organizing and grouping related Virtual Agent assets, such as topics. You can also make category labels visible in the Topic picker menu displayed to end users.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create or modify custom categories

Create or change custom categories for organizing and grouping related Virtual Agent assets, such as topics. You can also make category labels visible in the Topic picker menu displayed to end users.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Use topic categories to group related conversation topics. When your create or update a topic, you can assign one or more categories to which the topic belongs. You can also view your topics by category in Virtual Agent Designer.

For your end users, you can make the custom category label visible in the Topic picker menu so that associated topics are displayed by category.

Before you create a new category, review the existing categories \(**All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Categories**\) to determine if you need a new category.

**Note:** Pre-built topics have associated, default categories that can't be changed or deleted. Also, you can delete a custom category only when the category does not have any topics assigned to it.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Categories**.

2.  Select **New** to create a custom category or select a category record to change it.

<table id="table_rhm_zgv_14b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Label for the category.

</td></tr><tr><td>

Description

</td><td>

Brief description of the category purpose.

</td></tr><tr><td>

Application

</td><td>

Application scope of the category.

</td></tr><tr><td>

Visible to end user

</td><td>

Option to display the category label in the Topic picker menu for end users. **Note:**

-   If you upgraded from a previous release, existing category labels are set to not visible.
-   This option does not control the topics displayed within the category. At the topic level, use the **Condition** field in the Topic Properties page to set conditions that control when a topic is displayed to end users.


</td></tr></tbody>
</table>3.  Select **Submit** or **Update**.

    The topic category appears in the following items:

    -   **Category** list collector \(slushbucket\) on the Topic Properties page in Virtual Agent Designer so that you can assign one or more categories to a topic.
    -   **Category** filter on the Topics page, so that you can view topics by category.
    -   Topic cards on the Topics page, for topics that have assigned categories.
    -   Topic picker menu displayed to end users, if you made the category visible. Topics with multiple categories are displayed in the appropriate categories. Topics without categories are listed in the Others category.

        ![Topic picker menu that shows topics organized by categories.](../images/va-topic-picker.png "Topic picker menu")

4.  To delete a topic category, open the category record and click **Delete**.

    If there are no topics associated with the category, the category is deleted. It is no longer listed in the **Category** field on the Topics Properties page and in the **Category** filter on the Topics page in Virtual Agent Designer.


**Parent Topic:**[Configuring Virtual Agent](../concept/configure-virtual-agent.md)

