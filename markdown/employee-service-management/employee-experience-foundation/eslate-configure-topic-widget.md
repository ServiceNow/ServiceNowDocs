---
title: Configure topic page widget instance
description: Configure the topic page widget instance to control applications, topic subtopics, and topic assistance settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/eslate-configure-topic-widget.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-27"
reading_time_minutes: 1
keywords: [Topic Page widget, widget instance, employee slate, widget properties, featured applications, topic subtopics, topic assistance]
breadcrumb: [Browse and topic experience, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure topic page widget instance

Configure the topic page widget instance to control applications, topic subtopics, and topic assistance settings.

## Before you begin

Role required: admin

## About this task

The topic page widget displays topic-related content and applications to employees. Configure widget instance properties to control featured applications, topic subtopics display, and topic assistance prompts.

## Procedure

1.  Navigate to **All** &gt; **AI Experience Framework Components** &gt; **Widget Instances**.

2.  Open the **Topic Page Instance** widget instance record.

    The widget instance record displays the following fields:

    |Field|Description|
    |-----|-----------|
    |**Container**|Container that holds the widget instance.|
    |**Widget**|Widget type. This field is automatically set to `Topic Page`.|
    |**Order**|Position of the widget within the container. Lower numbers appear first.|
    |**Name**|Identifier for the widget instance. This field is automatically set to `Topic Page Instance`.|
    |**Application**|Application that contains the widget instance. This field is automatically set to `Employee Slate Core`.|

    \[Omitted image "es-topic-widge.png"\] Alt text: AIX Widget Instance record for the Topic Page Instance showing widgetOptions JSON with featured-apps, topic-subtopics, and ask-topic-assist sections.

3.  In the **Properties** field, configure the widget options using JSON format.

    The Properties field contains a JSON object with the following structure:

    ```
    {
      "widgetOptions": {
        "featured-apps": {
          "dataSource": "topic",
          "showViewAll": false,
          "hideWhenEmpty": true,
          "heading": "Applications",
          "headingWeight": "normal",
          "fixedHeight": true
        },
        "topic-subtopics": {
          "heading": "Sub"
        },
        "ask-topic-assist": {
          "heading": "Ask Otto",
          "numberOfPrompts": "5"
        }
      }
    }
    ```

    **Note:** Modify the values as required.

4.  Configure the **featured-apps** section to control how featured applications appear.

5.  Configure the **topic-subtopics** section to control subtopic display.

    Set the **heading** property to specify the section heading. Leave empty to use the default heading.

6.  Configure the **ask-topic-assist** section to control topic assistance prompts.

    |Property|Description|
    |--------|-----------|
    |**heading**|Section heading text. Example: `Ask Otto`.|
    |**numberOfPrompts**|Number of assistance prompts to display. Leave empty to use the default value of 5.|

7.  Select **Update** to save the configuration.


## Result

The Topic Page widget displays featured applications, subtopics, and topic assistance based on your configuration.

**Note:** Only for Moveworks experiences, the topic suggested prompts are available. For other experiences, Ask Otto or topic assist isn't available.

