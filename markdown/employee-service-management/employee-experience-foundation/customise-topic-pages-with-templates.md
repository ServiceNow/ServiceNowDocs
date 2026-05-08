---
title: Customize topic pages with various templates
description: Design topic pages with various custom-made templates to suit the tone of the topic for an enhanced user experience.Design topic pages with different templates using simplified cascading rules that provide a better designing experience for curators.Create customized topic page templates to present different types of topics in distinguished manner to enhance customer engagement.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Dynamic topic pages, Setup Employee Center browse experience features, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Customize topic pages with various templates

Design topic pages with various custom-made templates to suit the tone of the topic for an enhanced user experience.

## Before you begin

Role required: taxonomy\_admin

## About this task

Customize topic templates to improve your user experience. Each topic requires a different way of presentation for optimal customer engagement.

-   Decide whether to change the appearance of the parent topic or the entire sub-tree.
-   Make different topic sub-trees look different if the topic requires it.
-   Easily switch to the default template for the parent topic, the sub-tree topics, or all topics.
-   Preview the appearance before you publish.

**Note:**

Ensure that you have San Diego installed along with Employee Center app version 24.0.5 to use the feature.

## Procedure

1.  Navigate to **All** &gt; **Content Taxonomy** &gt; **Taxonomies**.

    You can choose any taxonomy and the topics within the taxonomy to assign a custom template.

2.  Select your preferred template from the list of templates to customize the chosen topic page.

3.  Click **Preview template** to view the topic page in the new template before applying.

4.  Click **Apply template to child topics** to apply the template for all child topics.

    **Note:**

    -   All scheduled content, such as a campaign or content targeted for the respective topic must be rescheduled after a new template is applied to a topic page.
    -   When you clone, move, or create a topic, the default template is automatically used. You must assign the desired custom template to the topic.
5.  Click **Reset to default templates** to remove the customization and reset to the default template.

6.  Click **Save** to publish.


## Result

Customization of topic pages enables users to have better representation and autonomy in presenting different content.

## Simplified topic page template cascade rule

Design topic pages with different templates using simplified cascading rules that provide a better designing experience for curators.

A few modifications have been made to the topic page cascading rules to streamline the process of customizing topic pages.

-   When a parent topic cascades its template to its child topics by selecting **Apply template to child topics**, it overrides any changes made to a child topic, on the topic level, and it adapts to the cascaded rules from the parent.
-   If you move a child topic from one parent topic to another, the child topic reflects the template cascaded by the new parent topic.

    **Note:** If you try to move a child topic from one sub-tree to another, you receive a warning stating that you will lose the current changes present in the topic page.

    The feature upgrade clones the applied template when you clone a topic.


## Create topic page template

Create customized topic page templates to present different types of topics in distinguished manner to enhance customer engagement.

### Before you begin

Role required: sp\_admin

Application scope: Employee Center

### About this task

Assign various topic templates based on the content after you create or clone a new topic page. For more information, see Create and edit a page using the Service Portal Designer.

For design recommendations for the topic page templates, see [Curated Experiences – Topic Page Templates UX Guidance \[KB1002813\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1002813).

**Note:** It is advised to clone a topic page and make the required modifications instead of creating one.

This would ensure consistency among the topic pages.

### Procedure

1.  Navigate to **Service Portal** &gt; **Pages**.

2.  Select the topic page template you have created.

3.  To make **Category** available on the page, right-click and navigate to **Configure** &gt; **Form Layout** to make **Category** visible, which is by default inaccessible.

    ![Contextual menu to configure category visibility.](../images/form-layout.png "Category visibility setting")

4.  Add **Category** to the **Selected** list and **Save**.

    ![Category field added to selected list.](../images/category-selected.png "Category field in selected list")

    **Note:** It is essential to set the **Category** to **Taxonomy**. Only the templates set to **Category**, **Taxonomy** are visible in the topic form template list.


