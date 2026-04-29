---
title: About Coaching
description: After you enable Coaching, you can set up roles and groups, define coaching opportunities, create training material, and start assessing and coaching employees. The Coach and Trainee dashboards provide useful overviews to manage and measure results.
locale: en-US
release: australia
product: Coaching
classification: coaching
topic_type: concept
last_updated: "2026-04-04"
reading_time_minutes: 7
breadcrumb: [Explore, Coaching, IT Service Management]
---

# About Coaching

After you enable Coaching, you can set up roles and groups, define coaching opportunities, create training material, and start assessing and coaching employees. The Coach and Trainee dashboards provide useful overviews to manage and measure results.

**Note:** For detailed information on how to get started with Coaching, see the [Coaching demo](https://www.servicenow.com/community/itsm-blog/servicenow-coaching-module-demo/ba-p/2332545).

## Coaching terminology

|Terminology|Description|
|-----------|-----------|
|Coaching assessment|Used to evaluate an agent and then assign training and skills based on the evaluation. An assessment can be generated automatically from a coaching opportunity based on conditions set in the opportunity. As assessment can also be generated manually.|
|Coaching opportunity|A critical moment in a process that generates an assessment based on set conditions. A coaching opportunity can be generated at any time during the life cycle of any task record such as incident, problem, change request, or request items.|
|Virtual coach|A record that can be associated with a coaching opportunity that automatically completes tasks associated with an assessment.|
|Coaching survey|A survey associated with a coaching assessment that lets coaches provide feedback on the agents' completed work and lets agents provide feedback on the coaching effectiveness.|

## Coaching assessments

You can create coaching assessments manually and associate it with a task record or generate them automatically using coaching opportunities. When the trigger conditions set in a coaching opportunity are met, an assessment is automatically generated and automatically assigned to the trainee's coach to assess the context in which the assessment was triggered. For example, you can set conditions in the coaching opportunity to create a coaching assessment when an employee does not write clear work notes when they escalate an incident. The coach can evaluate the employee using the assessment and add learning tasks to train them to write better work notes.

After you create coaching assessments manually or automatically, you can do any of the following:

-   Award skills
-   Assign learning tasks
-   Associate coaching surveys to the assessment

**Note:** You can automate these tasks using a virtual coach that's associated with the coaching opportunity.

**Awarding skills**: After the coach completes an assessment, they can award skills that's related to the assessment to the trainee.

**Assigning learning tasks**: Coaching assessments can have learning tasks associated with it to train the agent based on the assessment. When the agent completes the training, the skills associated with the learning tasks are added to the agent's skills set. For example, if the agent resolved an escalation that required router skills and if the agent does not have that skill, then the learning tasks can include training for router skills. After the agent completes the training, the router skills is added to the agent's skill set. Next time when an incident that requires router skills is assigned to the agent, they will be able to successfully resolve the incident.

**Setting up coaching surveys**: Coaching surveys can be associated with a coaching assessment. When the coach completes the coaching assessment, a survey can be triggered. Coaching surveys let coaches provide feedback on the ability of the agents' to resolve incidents or the quality of their completed tasks. Trainee surveys let agents provide feedback on the coaching effectiveness.

-   **Survey for the coach** is taken by the coach where the coach can provide feedback to rate the trainee. For example, did the trainee demonstrate the knowledge and technical competence required?
-   **Survey for the trainee** is taken by the agent where the agent can provide feedback to rate the coach. For example, were the learning tasks assigned to the agent useful in building skills?

## Coaching opportunity

A coaching opportunity is a critical moment in a process where coaching assessments get triggered based on conditions set in the coaching opportunity record. A coaching opportunity can be generated at any time during the life cycle of any task record such as incident, problem, change request, or request items. For example, you can set conditions to trigger a coaching opportunity when an incident reassigned or escalated. For examples on identifying coaching opportunities, see the Identifying coaching opportunities section.

You can do the following in a coaching opportunity record:

-   Set trigger conditions.
-   Associate skills, learning tasks, or surveys with the coaching opportunity. These items get automatically associated with the assessment that is associated with the opportunity.
-   Define a virtual coach. When an assessment is automatically created from an opportunity, and if a virtual coach record is associated with it, then the assessment will automatically be moved to closed, complete state. It will also automatically award skills and any learning tasks associated with the assessment to the trainee. The surveys associated with the opportunity will be assigned to the coaches or trainee as well.

    **Note:**

    -   All virtual coach records will have a coaching opportunity associated with it but not all coaching opportunities will have an associated virtual coach record.
    -   A virtual coach cannot be associated a manually generated assessment.
    For information on virtual coach, see [Identify and add course items for a virtual coach](../task/cf-identify-learning-content.md).


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

Because a virtual coach is not associated with the coaching opportunity, you must complete the following tasks manually:-   Award skills
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
</table>You can use Coaching for any task-based process for such as Change Management, Customer Service Management or Incident Management to set up Coaching. You can also use Coaching for a non-task or custom table source by [configuring a business rule](../reference/cf-coaching-reference.md).

## Initial Coaching setup

Once you have enabled Coaching, set up the application by assigning user roles, configuring coaching opportunities and creating training content.

1.  Set up Coaching [Coaching roles](../reference/cf-coaching-roles.md) and groups
2.  [Define trigger conditions for a coaching opportunity](../task/cf-create-coaching-opportunity.md)
3.  [Identify and add course items for a virtual coach](../task/cf-identify-learning-content.md)
4.  Set up [surveys](cf-setting-up-coaching.md)

## Coaching dashboards

Use Coaching dashboards to manage and measure results in a simplified view.

-   [Coaching Dashboard](cf-coaching-your-trainee.md)
-   [Trainee Dashboard](cf-getting-coached.md)

## Identifying coaching opportunities

Coaching opportunities can be found in many tasks that occur throughout your environment.

-   Writing better work notes when service desk escalates incidents to a second level.
-   Correctly setting affected configuration items when the service desk works on incidents.
-   Using the correct naming convention for admin in update sets.
-   Coaching during the onboarding and the warranty period of a new application.
-   Correctly reassigning a case to another user with pertinent information in comments.
-   Engaging a user on closed records when non-positive feedback is received through surveys.
-   Spot-checking a user on quality control.
-   Helping to guide project managers in projects.
-   Improving knowledge article quality when knowledge articles are attached to resolved incidents.

## Common ITSM assessment triggers

You can define activities that occur when trainees work through an ITSM process, such as resolving an incident, as assessment triggers.

|Table|Assessment triggers|
|-----|-------------------|
|Incident|Moment of first response|
|Categorization and prioritization|
|Reassignment|
|Proposal of solution to the customer|
|Problem|Definition of the Problem statement|
|Writing the Known Error|
|Writing the Workaround|
|Root Cause analysis|
|Root Cause confirmation|
|How can this issue be avoided?|
|Change|Categorization and prioritization|
|Implementation description|
|Risk analysis|
|Impact analysis|
|Approval|
|Implementation|
|Post implementation review|

