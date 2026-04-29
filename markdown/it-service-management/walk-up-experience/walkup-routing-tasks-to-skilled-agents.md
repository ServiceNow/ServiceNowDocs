---
title: Route walk-up tasks to skilled agents
description: Use business rules to automatically route walk-up tasks to the agents based on their skill set.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure skill-based routing in Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Route walk-up tasks to skilled agents

Use business rules to automatically route walk-up tasks to the agents based on their skill set.

## Before you begin

Set up metadata in **All Skills**, **Group Skills**, and **User Skills**tables before configuring walk-up locations for skill-based routing. For more information, [Configuring Skills Management](https://www.servicenow.com/docs/access?context=configuring-skills-management&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Walk-up Experience** &gt; **Administration** &gt; **Walk-up Locations**.

2.  Select the location to add skills of the agents.

3.  In the related list, select **Reasons for Visit**.

4.  Select a reason to associate the skills.

5.  On the **Walk-up Skills for Reasons** related list, select **New**.

6.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Active|Option to make the skill active.|
    |Skill|Skill required for the selected walk-up reason.|
    |Mandatory|Option to make the skill mandatory. If the skill is set as mandatory, the walk-up task will not be routed to any agent who does not have that particular skill.|
    |Walk-up Reason|Reason for which a requester needs help.|

7.  Select **Submit**


**Parent Topic:**[Configure skill-based routing in Walk-up Experience](../concept/walkup-skill-based-routing.md)

