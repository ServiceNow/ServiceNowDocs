---
title: Configure browse experience in Employee Slate
description: Configure the browse experience by associating a taxonomy with your Employee Slate experience to enable topic-based navigation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/eslate-configure-browse-experience.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 1
keywords: [Employee Slate, browse experience, taxonomy configuration, topic navigation]
breadcrumb: [Browse and topic experience, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure browse experience in Employee Slate

Configure the browse experience by associating a taxonomy with your Employee Slate experience to enable topic-based navigation.

## Before you begin

Verify that you have a taxonomy structure defined with root topics and subtopics.

Role required: **admin**

## About this task

The browse experience provides users with topic-based navigation similar to Employee Center. By configuring a taxonomy for your Employee Slate experience, you enable the explore button and topic catalog functionality.

## Procedure

1.  Navigate to **All** &gt; **AI Experience Framework** &gt; **AI Experiences**.

2.  Open an existing AI Experience such as **Employee Slate**, select **AI Experience Properties** related list, select the **Taxonomy** property, and edit or use the appropriate the taxonomy value.

    \[Omitted image "es-aix-properties.png"\] Alt text: AI Experience record for Employee Slate showing AI Experience Properties related list with chatType, default\_topic\_template, menu, and taxonomy fields.

    Use or edit the taxonomy that contains the topics and content structure you want to present to users.

3.  Save the experience record.

4.  Verify the configuration by accessing the Employee Slate interface.

    The explore button appears and opens the panel with root topics.


## Result

Users can now access the browse experience through the explore button, navigate topic pages, and discover content through the organized taxonomy structure.

## What to do next

Consider configuring quick links and associating knowledge articles and catalog items with specific topics to enhance the browse experience.

**Related topics**  


[Configure topic page widget instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-configure-topic-widget.md)

