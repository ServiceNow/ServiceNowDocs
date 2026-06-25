---
title: Coaching in Workforce Optimization for Customer Service
description: Coaching lets you review and assess the quality of completed interactions and tasks, enhance your teams' skill set by assigning training based on the assessments, add skills to their profile when they get trained, and identify skill gaps to train your agents effectively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/explore-coaching-configurable-wfo-cs.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workforce Optimization for Customer Service, Agent management, Use, Customer Service Management]
---

# Coaching in Workforce Optimization for Customer Service

Coaching lets you review and assess the quality of completed interactions and tasks, enhance your teams' skill set by assigning training based on the assessments, add skills to their profile when they get trained, and identify skill gaps to train your agents effectively.

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
</table>As a coach, you can:

-   Use surveys to evaluate your team's performance.
-   Recognize improvement opportunities and assign training tasks.
-   Assess a trainee's ability to resolve cases.
-   Assign training that is based on the assessments.
-   Add skills to a trainee's profile that is based on a recommendation from Predictive Intelligence.

As a trainee, you can get trained to address your skill gaps.

## Example

For example, Amy Jones manages Customer Service operations for a large organization and has 12 teams reporting to them. Each team has anywhere from 8 through 15 agents. She is also added as a manager to other teams to increase visibility.

Amy Jones wants a single location to:

-   Monitor the skills each team uses to solve issues
-   Analyze metrics and monitor pending coaching assessments and training for the teams
-   Add skills used for resolving issues or when Predictive Intelligence Workbench recommends them.

Amy Jones can manage all of these actions by doing the following:

1.  Set conditions that trigger coaching opportunities.
2.  Assess agents' skills and assign training.
3.  Add skills to agent profile when they complete training or using recommendations from Predictive Intelligence.

For detailed instructions to use Coaching in Workforce Optimization for Customer Service, see [Coaching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/coaching-configurable-wfo-cs.md).

-   **[Using Coaching in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/coaching-configurable-wfo-cs.md)**  
By using Coaching in Workforce Optimization for Customer Service, you can assess your team's abilities to efficiently resolve cases by reviewing their work at critical moments of customer service.

**Parent Topic:**[Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/use-configurable-wfo-cs.md)

**Related topics**  


[Setting up skill prediction in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setting-up-skill-prediction-configurable-cs.md)

[Using Coaching in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/coaching-configurable-wfo-cs.md)

