---
title: Tutorial: Automatically assign work to agents by skill
description: Learn how you can configure Advanced Work Assignment to automatically route cases to agents who speak German. Use this tutorial as a guideline to help you understand how you can route work items to agents according to their designated skills.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure agent assignment rules, Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Tutorial: Automatically assign work to agents by skill

Learn how you can configure Advanced Work Assignment to automatically route cases to agents who speak German. Use this tutorial as a guideline to help you understand how you can route work items to agents according to their designated skills.

Before you begin:

-   Activate the Skills Management \(com.snc.skills\_management\) plugin.
-   A basic understanding of the [Skills Management](https://www.servicenow.com/docs/access?context=skills-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) feature is required.
-   To have skills automatically assigned to cases, consider activating the Skill Determination \(com.snc.skill\_determination\) plugin.
-   Create a group of users who work in customer support.
-   Assign the awa\_agent and workspace\_agent roles to the customer support group.

![Video link](../../conversational-interfaces/image/icon-video-link.png) [Advanced Work Assignment \(AWA\) Tutorial: Automatically assign work to agents by skill](https://www.youtube.com/watch?v=2epAFf8yAT0) Watch this video for a visual representation of the following tutorial example.

-   **[Create a skill](../task/skills-example.md)**  
Create a "German" skill.
-   **[Create an assignment rule that auto assigns agents' work](../task/skills-example-assignment-rule.md)**  
Create an assignment rule that routes cases according to skills.
-   **[Create a queue](../task/skills-example-queue.md)**  
Create a queue where you can route work to agents who have the German skill.
-   **[Define assignment eligibility](../task/skills-example-assignment-pool.md)**  
Define who is eligible to receive cases from the German Cases queue.
-   **[Enable skill determination](../task/skills-example-skill-determination.md)**  
Activate the skill determination business rule to tag skills for your work items.
-   **[Define a skill determination rule](../task/skills-example-define-skill-determination.md)**  
Create a skill determination rule to tag the German skill to incoming cases from German speakers.

**Parent Topic:**[Configure agent assignment rules](../task/awa-create-assignment-rule.md)

