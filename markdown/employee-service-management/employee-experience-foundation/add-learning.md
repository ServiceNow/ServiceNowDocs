---
title: Associate learning content to a topic
description: Add learning content to a topic page to provide employees with quick access to training and career development.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create and associate topics, Unified Taxonomy for Employee Center, Setup Employee Center browse experience features, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Associate learning content to a topic

Add learning content to a topic page to provide employees with quick access to training and career development.

## Before you begin

Role required: taxonomy\_admin

User Criteria required: Taxonomy Manager, Taxonomy Contributor, Topic Manager, Topic Contributor.

Do the following steps:

1.  Install the Learning \[sn\_lep\] application: [Install and configure Learning](../../human-resources/concept/configuring-learning.md)
2.  Provide employees with the Talent Development license to enable access to the learning content: [License Talent Development Core users](../../employee-service-management/task/egd-employee-profile-licensing.md)
3.  Navigate to the **Scheduled jobs** &gt; **Refresh access to all apps** and click **Execute Now**.

    This adds a new record to the Employee Application Access \[sn\_employee\_app\_access.list\] table.


## About this task

The Topic Content widget displays the connected content associated with that topic, such as Knowledge Base articles, courses, and Service Catalog request items.

## Procedure

1.  Navigate to **All** &gt; **Content Taxonomy** &gt; **Topics**.

2.  Select any topic and go the **Connected Content** and click **New**.

3.  Select the **Learning** content type.

    ![The content type shows Learning as a listed option on the field.](../images/cnnctd-cntnt-lrng.jpg)

    The **Learning course** field appears.

4.  Select the course.

    ![The Learning course field opens a new window with all the learning course items listed.](../images/learning-content-course.png)

5.  Click **Submit**.


## Result

Employees with Talent Development license can now access the learning content on the topic page.

![The course appears in the topic content widget.](../images/learning-content.png)

