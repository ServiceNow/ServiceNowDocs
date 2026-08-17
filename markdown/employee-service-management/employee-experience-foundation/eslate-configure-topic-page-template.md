---
title: Assign a custom topic page template
description: Assign a custom layout template to a topic page and optionally apply the template to child topics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/eslate-configure-topic-page-template.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
keywords: [topic page template, Employee Slate, apply to children, default topic template]
breadcrumb: [Browse and topic experience, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Assign a custom topic page template

Assign a custom layout template to a topic page and optionally apply the template to child topics.

## Before you begin

Clone the default topic template widget and customize your sub-widget layout.

Role required: admin or aix\_widget\_admin

## About this task

A topic page template controls the layout of widgets on a topic page, such as the topic header, subtopics, quick links, and support resource content. Employee Slate includes a default template that renders on every topic page. You can assign a custom template to an individual topic when that topic requires a different layout.

-   Employee Slate checks for templates in this order: a custom template assigned to the topic and experience, the default topic template set on the experience record, or the default template.
-   You can apply a custom template to a single topic or extend it to all child topics for consistent layout across a subtree.
-   You can use template extension to maintain consistent layouts for related topics, such as all topics under a department-owned parent topic.

## Procedure

1.  In the topic record, open the **Experience Topic Template Mapping** related list.

    \[Omitted image "es-topic-template-mapping.png"\] Alt text: Experience Topic Template Mapping form for a topic showing Template, Topic, Experience, and Active fields.

2.  Complete the fields.

    |Field|Description|
    |-----|-----------|
    |**Template**|The default topic template widget to render for this topic.|
    |**Topic**|Topic to which this custom template applies.|
    |**Experience**|Experience to which this custom template applies.|
    |**Apply to children**|When selected, extends the custom template to all child topics under the selected topic.|
    |**Application**|This field is automatically set to Employee experience taxonomy.|
    |**Active**|When selected, activates the custom template.|

3.  Select **Save**.

4.  To change the default template for every topic in an experience, set the **Default topic template** property on the experience record.

    Employee Slate applies the default topic template to any topic that has no custom template assigned.


## Result

The topic page for the selected topic renders using the assigned template. When **Apply to children** is selected, child topics also render using the assigned template.

