---
title: Configure knowledge widget
description: Control the visibility of author and last updated fields in the Knowledge widget using widget instance properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/eslate-configure-knowledge-widget.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-27"
reading_time_minutes: 1
keywords: [Knowledge widget, widget configuration, employee slate, widget properties, visibility settings]
breadcrumb: [Knowledge overview, Tasks and requests, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure knowledge widget

Control the visibility of author and last updated fields in the Knowledge widget using widget instance properties.

## Before you begin

Role required: admin

## About this task

The Knowledge widget displays knowledge articles to employees. You can configure widget instance properties to show or hide the author name and last updated date fields.

## Procedure

1.  Navigate to **All** &gt; **AI Experience Framework Components** &gt; **Widget Instances**.

2.  Open the **Knowledge** widget instance record.

3.  In the Properties field, locate the visibility properties for the Knowledge widget.

    \[Omitted image "es-aix-page-property.png"\] Alt text: AIX Widget Instance record showing Knowledge Article properties with showAuthor and showLastUpdated settings

    The properties control which metadata fields appear in the widget.

4.  Set the **showAuthor** property to `true` or `false`.

    When set to `true`, the author name appears on knowledge articles. When set to `false`, the author name is hidden.

5.  Set the **showLastUpdated** property to `true` or `false`.

    When set to `true`, the last updated date appears on knowledge articles. When set to `false`, the last updated date is hidden.

6.  Select **Update**.


## Result

The Knowledge widget displays or hides the **author** and **last updated** fields based on your configuration.

