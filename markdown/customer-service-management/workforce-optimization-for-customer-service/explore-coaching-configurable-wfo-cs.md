---
title: Coaching in Workforce Optimization for Customer Service
description: Learn how you can review and assess the quality of completed interactions and tasks. Enhance your teams' skills set by assigning them training based on the assessments and add skills to their profile when they get trained.
locale: en-US
release: xanadu
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Coaching in Workforce Optimization for Customer Service

Learn how you can review and assess the quality of completed interactions and tasks. Enhance your teams' skills set by assigning them training based on the assessments and add skills to their profile when they get trained.

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

![Infographic displaying how predictive intelligence assesses agent skills and recommends training for agents. For more information, see the text the follows.](../image/coaching_wfo_cs.png)

Here's an example of how Workforce Optimization for Customer Service uses Predictive Intelligence to recommend skills for agents:

<table id="table_dsl_tmr_cmb"><thead><tr><th>

Step

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

1.

</td><td>

Predictive Intelligence associates the cases that were closed using similar skills and then groups the tasks by the agents who resolved them.

</td><td>

Predictive Intelligence looks at the similarity between the tasks that were resolved using the skill Firewall.

</td></tr><tr><td>

2.

</td><td>

When agents resolve cases, the Skill Recommendation application stores the skill and agent associations.

</td><td>

Agent A completes a task that requires the skill Firewall, but that skill is not in the agent's user profile yet.

</td></tr><tr><td>

3.

</td><td>

System administrators set the threshold for the skill and agent associations.

 When the threshold is reached, the Skill Recommendation application recommends to the agent's manager that the skill be added to an agent's profile.

</td><td>

The system administrator sets the threshold at 10. That means the agents have to complete at least 10 tasks that require a specific skill, before the predictive intelligence engine can recommend that specific skill for the agents.

 Agent A completes 10 tasks that required the skill Firewall, and currently Agent A is not assigned skill Firewall. The Skill Recommendation application recommends the skill Firewall for Agent A to the agent's manager.

</td></tr><tr><td>

4.

</td><td>

The manager approves and adds the skill to the agent's profile.

</td><td>

Agent A's manager approves the skill Firewall and adds that skill to Agent A's profile.

</td></tr><tr><td>

5.

</td><td>

Advanced work assignment \(AWA\) uses the new skills that were added to the agent's profile, looks up tasks that require those skills, and assigns the agents to complete those tasks.

</td><td>

When a task requires the skill Firewall, Agent A is automatically considered for that task assignment.

</td></tr><tr><td>

6.

</td><td colspan="2">

Over time, the Predictive Intelligence machine learning algorithms learn which skills were assigned to the agents to resolve the cases.

</td></tr></tbody>
</table>The infographic shows how you can use Predictive Intelligence to recommend skills for your agents.

![Infographic displaying work assigned to agents based on their skills by using Predictive Intelligence and Skill Recommendation application.](../image/csm_skills_recommendation_flow.png)

As a coach, you can:

-   Use surveys to evaluate your team's performance.
-   Recognize improvement opportunities and assign training tasks.
-   Assess a trainee's ability to resolve cases.
-   Assign training that is based on the assessments.
-   Add skills to a trainee's profile that is based on a recommendation from Predictive Intelligence.

As a trainee, you can get trained to address your skill gaps.

**Related topics**  


[Setting up skill prediction in Workforce Optimization for Customer Service](../task/setting-up-skill-prediction-configurable-cs.md#)

[Coaching in Workforce Optimization for Customer Service](coaching-configurable-wfo-cs.md#)

