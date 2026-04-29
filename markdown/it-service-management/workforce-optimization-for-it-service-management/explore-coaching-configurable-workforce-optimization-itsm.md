---
title: Coaching in Workforce Optimization for ITSM
description: Learn how you can review and assess the quality of the interactions and tasks completed by your teams. You can enhance the skills set of your teams by assigning training that is based on those assessments. You can also add skills to the profiles of your teams after they get trained.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Workforce Optimization for ITSM, IT Service Management]
---

# Coaching in Workforce Optimization for ITSM

Learn how you can review and assess the quality of the interactions and tasks completed by your teams. You can enhance the skills set of your teams by assigning training that is based on those assessments. You can also add skills to the profiles of your teams after they get trained.

Initiate a skill review process to have your teams assess their own skill set and approve or reject the skills. After it's approved, they’ll automatically be added to the skill set of the team member.

## Coaching overview

The image shows a high-level workflow on how coaching admins set up Coaching, and how managers and agents use Coaching.

![The infographic shows a high-level workflow on how coaching admins set up Coaching and how coaches and trainees use it.](../image/coaching-wfo-itsm.svg)

Here's an example of how Workforce Optimization for ITSM uses Predictive Intelligence to recommend skills for agents:

<table id="table_dsl_tmr_cmb"><thead><tr><th>

Step

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

1.

</td><td>

Predictive Intelligence associates the incidents that were closed using similar skills and then groups the tasks by the agents who resolved them.

</td><td>

Predictive Intelligence looks at the similarity between the tasks that were resolved using the skill Firewall.

</td></tr><tr><td>

2.

</td><td>

When agents resolve incidents, the Skill Recommendation application stores the skill and agent associations.

</td><td>

Agent A completes a task that requires the skill Firewall, but that skill is not in the agent's user profile yet.

</td></tr><tr><td>

3.

</td><td>

System administrators set the threshold for the skill and agent associations.

 When the threshold is reached, the Skill Recommendation application recommends to the agent's manager that the skill be added to the agent's profile.

</td><td>

The system administrator sets the threshold at 10. That means that the agents must have the same skill and complete 10 similar tasks.

 Agent A completes 10 tasks using the skill Firewall. The Skill Recommendation application recommends the skill Firewall for Agent A to the agent's manager.

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

Over time, the Predictive Intelligence machine learning algorithms learn which skills were assigned to the agents to resolve the incidents.

</td></tr></tbody>
</table>The infographic shows how you can use Predictive Intelligence to recommend skills for your agents.

![Infographic that shows how you can use Predictive Intelligence to recommend skills for your agents. The text in the table that precedes this infographic describes the flow.](../image/skill-recommendation.png)

## Coaching terminology

|Terminology|Description|
|-----------|-----------|
|Coaching assessment|Using assessments, you can evaluate an agent and then assign training and skills based on the evaluation. An assessment can be generated automatically from a coaching opportunity based on the conditions set in the opportunity. As assessment can also be generated manually.|
|Coaching opportunity|A critical moment in a process that generates an assessment based on set conditions. A coaching opportunity can be generated at any time during the life cycle of any task record, which could include incidents, problems, change requests, or request items.|
|Virtual coach|A record that can be associated with a coaching opportunity that automatically completes tasks associated with an assessment.|
|Coaching survey|A survey associated with a coaching assessment that lets coaches provide feedback on the work completed by the agents. It also lets agents provide feedback on the coaching effectiveness.|

## Coaching assessments

You can create coaching assessments manually and associate it with a task record or generate them automatically using coaching opportunities. When the trigger conditions set in a coaching opportunity are met, an assessment is automatically generated. It’s then automatically assigned to the coach for the trainee to assess the context in which the assessment was triggered. For example, let's assume an employee doesn't write clear work notes when they escalate an incident. You can set conditions for this scenario in the coaching opportunity to create a coaching assessment. The coach can evaluate the employee using the assessment and add learning tasks to train them to write better work notes.

After you create coaching assessments manually or automatically, you can do any of the following:

-   Award skills
-   Assign learning tasks
-   Associate coaching surveys to the assessment

**Note:** You can automate these tasks using a virtual coach that's associated with the coaching opportunity.

**Awarding skills**: After the coach completes an assessment, they can award skills that's related to the assessment to the trainee.

**Assigning learning tasks**: Coaching assessments can have learning tasks associated with it to train the agent based on the assessment. When the agent completes the training, the skills associated with the learning tasks are added to the skills set of the agent. For example, let's assume that the agent resolved an escalation that required router skills. If the agent doesn’t have that skill, then the learning tasks can include training for router skills. After the agent completes the training, the router skill is added to the skill set of the agent. Next time when an incident that requires router skills is assigned to the agent, they’ll be able to resolve the incident successfully.

**Setting up coaching surveys**: Coaching surveys can be associated with a coaching assessment. When the coach completes the coaching assessment, a survey can be triggered. Coaching surveys let coaches provide feedback on the ability of the agents' to resolve incidents or the quality of their completed tasks. Trainee surveys let agents provide feedback on the coaching effectiveness.

-   **Survey for the coach** is taken by the coach where the coach can provide feedback to rate the trainee. For example, did the trainee demonstrate the knowledge and technical competence required?
-   **Survey for the trainee** is taken by the agent where the agent can provide feedback to rate the coach. For example, were the learning tasks assigned to the agent useful in building skills?

## Coaching opportunity

A coaching opportunity is a critical moment in a process where coaching assessments get triggered based on conditions set in the coaching opportunity record. A coaching opportunity can be generated at any time during the life cycle of any task record. These records could include any task such as an incident, problem, change request, or request item. For example, you can set conditions to trigger a coaching opportunity when an incident reassigned or escalated. For examples on identifying coaching opportunities, see [About Coaching](../../cf-coaching/concept/cf-coaching-overview.md).

You can do the following in a coaching opportunity record:

-   Set trigger conditions.
-   Associate skills, learning tasks, or surveys with the coaching opportunity. These items are automatically associated with the assessment that is associated with the opportunity.
-   Define a virtual coach. When an assessment is automatically created from an opportunity, and if a virtual coach record is associated with it, then the assessment is automatically moved to the closed, complete state. It will also automatically award skills and any learning tasks associated with the assessment to the trainee. The surveys associated with the opportunity will be assigned to the coach or the trainee as well.

    **Note:**

    -   All virtual coach records have a coaching opportunity associated with it but not all coaching opportunities have an associated virtual coach record.
    -   A virtual coach can’t be associated with a manually generated assessment.
    For information on virtual coach, see [Identify and add course items for a virtual coach](../../cf-coaching/task/cf-identify-learning-content.md).


## Example of assessment triggers

<table id="table_gqt_yrv_1xb"><thead><tr><th>

Did the coaching opportunity trigger an assessment?

</th><th>

Is a virtual coach associated with the coaching opportunity and are the conditions set met?

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Yes

</td><td>

Yes

</td><td>

Because a virtual coach is associated with the coaching opportunity, it completes the following tasks automatically:-   Award skills
-   Assign learning tasks
-   Associate coaching surveys to the assessment

</td></tr><tr><td>

Yes

</td><td>

No

</td><td>

Because a virtual coach isn’t associated with the coaching opportunity, you must complete the following tasks manually:-   Award skills
-   Assign learning tasks
-   Associate coaching surveys to the assessment

</td></tr><tr><td>

No

</td><td>

No

</td><td>

You can create a manual assessment and complete the following tasks manually:-   Award skills
-   Assign learning tasks
-   Associate coaching surveys to the assessment

</td></tr></tbody>
</table>You can use Coaching for any task-based process for such as Change Management, Customer Service Management or Incident Management to set up Coaching. You can also use Coaching for a non-task or custom table source by [configuring a business rule](../../cf-coaching/reference/cf-coaching-reference.md).

As a coach, you can:

-   Use surveys to evaluate the performance. of your teams.
-   Recognize improvement opportunities and assign training tasks.
-   Assess the ability of trainees to resolve incidents.
-   Assign training that is based on the assessments.
-   Add skills to the skill set of a trainee that is based on a recommendation from Predictive Intelligence.
-   Initiate a skill review process to have your teams assess their own skill set.
-   Approve or reject a skill assessed by members of your team.

As a trainee, you can:

-   Get trained to address your skill gaps.
-   Evaluate the skill proficiency for an existing skill or add a new skill to your skill set.
-   Request approval from your manager to add the evaluated skills to your skill set.

## Getting started with Coaching in Workforce Optimization for ITSM

Easily find the tasks that you must complete in the Coaching module.

|Benefit|Roles|Finding tasks to complete in Coaching|
|-------|-----|-------------------------------------|
|Activate Coaching in the Workforce Optimization for ITSM.|admin|[Activate Coaching](../task/activate-configurable-workforce-optimization-itsm.md)|
|Refer to the roles, tables, and other components used in Coaching.|[Any coaching role](../reference/configurable-wfo-itsm-coaching-reference.md)|[Understand components used in Coaching in Workforce Optimization for ITSM](../reference/configurable-wfo-itsm-coaching-reference.md)|
|Set up Coaching.|[Admin](../reference/configurable-wfo-itsm-coaching-reference.md)|[Set up Coaching in Workforce Optimization for ITSM](setup-coaching-configurable-workforce-optimization-itsm.md)|
|Train your teams using Coaching with Learning.|[Coach](../reference/configurable-wfo-itsm-coaching-reference.md)|[Train your teams using Coaching with Learning in Workforce Optimization for ITSM](coaching-configurable-wfo-itsm.md)|
|Manage skills for your teams from a central location|Skill admin|[Manage skills in Workforce Optimization for ITSM](skills-management-wfo-itsm.md)|

