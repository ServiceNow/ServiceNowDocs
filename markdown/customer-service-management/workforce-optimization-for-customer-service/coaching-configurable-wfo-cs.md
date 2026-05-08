---
title: Coaching in Workforce Optimization for Customer Service
description: By using Coaching in Workforce Optimization for Customer Service, you can assess your team's abilities to efficiently resolve cases by reviewing their work at critical moments of customer service.Use Skills Overview to analyze skill data such as how many skills are assigned to users and tasks. You can also see how many experts you have for a particular skill and the overall skill coverage by your teams.Assess the ability of your agents to resolve cases or the quality of their completed tasks.Add or update skills for an agent. You can approve predicted skills if the skill is necessary for the agent to complete assigned tasks. You can also reject a skill if it doesn't apply to the agent.Use Coaching with Learning to train your agents with internal and external learning content. Organize similar content in catalogs. Assign learning tasks and track completion.Create a catalog to organize related content into categories.Create learning tasks for agents to keep track of their learning activities.Add internal courses so that agents can learn new content and enhance their skill set.Add courses from external sources such as Udemy, Pluralsight, or Cornerstone to enable your users to gain skills from external content.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Use, Workforce Optimization for Customer Service, Customer Service Management]
---

# Coaching in Workforce Optimization for Customer Service

By using Coaching in Workforce Optimization for Customer Service, you can assess your team's abilities to efficiently resolve cases by reviewing their work at critical moments of customer service.

With Coaching, you can do the following:

-   Recommend training for your agents to address skill gaps.
-   Use the coaching opportunities that are available by [default](../reference/components-installed-configurable-wfo-cs.md) to coach your agents. You can also create a coaching opportunity using the Coaching application specific to your agent needs.
-   Use assessments and surveys to apply consistent, measurable scores across teams.
-   Use Predictive Intelligence to recommend skills for your agents and provide training to address those skill gaps.

**Parent Topic:**[Using Workforce Optimization for Customer Service](use-configurable-wfo-cs.md)

## Skills Overview in Workforce Optimization for Customer Service

Use Skills Overview to analyze skill data such as how many skills are assigned to users and tasks. You can also see how many experts you have for a particular skill and the overall skill coverage by your teams.

Access Skills Overview from the Teams application:

1.  Go to **Workspaces** &gt; **Manager Workspace**.
2.  Click the Teams icon ![Teams icon.](../../itsm-manager-workspace/image/teams-icon.png).
3.  Select a team.
4.  Click the **Skills** tab.
5.  Select a skill.

You can access the Skills Overview page when you click on a skill in a user profile page in any Workforce Optimization for Customer Service application.

**Note:** You must enable the Coaching With Learning application to view the reports from the application. For enabling this application, see [Activate Workforce Optimization for Customer Service](../task/request-configurable-wfo-cs.md).

![Skill overview page displaying a skill assigned to tasks, agents, on-call experts, and a pie chart of skill coverage experience level dispersal.](../image/skills-overview-new.png)

### Use cases

<table id="table_m1n_xnm_v4b"><thead><tr><th>

User

</th><th>

Landing page use

</th></tr></thead><tbody><tr><td>

Skill Admin \[skill\_admin\]

</td><td>

-   Analyze all experts available for each skill.
-   Drill down into the skill hierarchy.
-   Number of skills assigned to users and tasks.
-   The mean time taken to resolve incidents for that skill.
-   Visualize how many users you have at different skill levels.

</td></tr></tbody>
</table>### Indicators

MTTR of incidents of skill - Mean time taken to resolve incidents with this skill.

### Breakdowns

The indicator is broken down by Skill.

### Components

<table id="table_qsw_cz5_v4b"><thead><tr><th>

Component Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skill Overview Container \[sn-manager-skill-overview-container\]

</td><td>

Visualization components

</td><td>

Contains the following components:-   Reports
-   Mean Time to Resolution \(MTTR\) indicator
-   Skill Coverage pie chart
-   Content tree
-   Skill Experts components

</td></tr><tr><td>

Skill Tree Connected \[sn-manager-skill-tree-connected\]

</td><td>

Tree

</td><td>

Displays the skill hierarchy. If the selected skill does not have a skill hierarchy then the component will not display on the Skill Overview page.

</td></tr><tr><td>

Skill Experts \[sn-manager-skill-experts-connected\]

</td><td>

List

</td><td>

Displays all users who are at the expert level for the skill.

</td></tr><tr><td>

Skill Coverage \[now-uxf-visualization-connected\]

</td><td>

Pie-chart

</td><td>

Displays the percentage as well as the number of users with different levels of expertise for the skill.

</td></tr></tbody>
</table>### Reports

**Important:** The Pending Users and Assigned Tasks reports display when you enable the Coaching with Learning application from the ServiceNow® Store. To enable this application, see [Activate Workforce Optimization for Customer Service](../task/request-configurable-wfo-cs.md).

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Assigned Users|![Single score icon.](../../../reuse/reporting/image/single-score-sm.svg)|User Skill \[sys\_user\_has\_skill\]|The number of users who have the selected skill assigned to them.|
|Assigned Tasks|![Single score icon.](../../../reuse/reporting/image/single-score-sm.svg)|Task Skill \[task\_m2m\_skill\]|The number of tasks for which this skill has been assigned.|
|Pending Users|![Single score icon.](../../../reuse/reporting/image/single-score-sm.svg)|Pending Users \[sn\_lc\_learning\_task\]|The numbers of users who are yet to be assigned the selected skill from the learning task.|
|Course Items|![Single score icon.](../../../reuse/reporting/image/single-score-sm.svg)|Learning Course Item \[sn\_lc\_course\_item\]|The number of internal and external courses that have the skill associated with the course item.|

## Assess the quality of completed tasks

Assess the ability of your agents to resolve cases or the quality of their completed tasks.

### Before you begin

You can create an assessment from an interaction or any task type.

When you manually create an assessment, you can add a survey to it. Coaching assessments also get created and assigned to the coach based on the trigger conditions that are defined in coaching opportunities.

Role required: sn\_coaching.coach

Watch this short video to get an overview on coaching, assessments, and trainings.

Workforce Optimization for Customer Service Coaching Overview.

### About this task

If the coaching opportunity includes a survey, you can opt to take the survey and the assessment. When you use a survey to assess a trainee, the score for the survey is automatically calculated when you complete the survey. The assessment rating is then updated based on that score.

The Coaching Overview screen displays the average quality of the tasks that were completed in the past 30 days for your assignment groups.

-   The donut chart displays the number of assessments in various states of completion. You can point to one of the states and click to open all assessments in that state.
-   The bar chart displays assessments created by coaching opportunities. You can click on any of the data in the graph to access the assessments.
-   You can click on the graph that displays the indicator data and access detailed information on the indicator.

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching \(![Coaching icon.](../image/coaching-new.png)\) icon.

3.  Do any of the following.

<table id="choicetable_k5z_rpq_pnb"><thead><tr><th align="left" id="d154966e658">

To

</th><th align="left" id="d154966e661">

Do this

</th></tr></thead><tbody><tr><td id="d154966e667">

**Perform adhoc assessments**

</td><td>

1.  Click the Lists \(![Lists icon.](../image/list-new.png)\) icon.
2.  Select any record, such as a case or interaction, for which you want to create an assessment.
3.  Select the Assessments \(![Coaching Assessment icon.](../image/coaching-assessment-new.png)\) icon. The assessment screen appears in the right panel.
4.  Click the plus \(+\) icon.


</td></tr><tr><td id="d154966e703">

**Use assessments triggered by coaching opportunities**

</td><td>

1.  Click the Coaching \(![Coaching icon.](../image/coaching-new.png)\) icon.
2.  Select any record for which you want to create an assessment.

**Note:** Click the **Active Assessments** tab to view assessments of all teams for which you are a manager or an additional manager.

3.  Select a case to assess.


</td></tr></tbody>
</table>4.  On the form, fill in the fields to assess the agent.

<table id="table_j31_ys1_mlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Opportunity

</td><td>

Coaching opportunity that is associated with the coaching assessment.

</td></tr><tr><td>

State

</td><td>

State of the assessment.-   **Open**: New coaching opportunity
-   **Work in progress**: Trainee is being coached
-   **Resolved**: Trainee is assigned coaching programs and training modules.
-   **Closed Complete**: Assessment has been resolved and closed.
-   **Closed Incomplete**: Assessment that has been closed but not completed, typically because the coaching assessment **Due Date** has expired.


</td></tr><tr><td>

Assessment Rating

</td><td>

How well the agent resolved the incident. The Coaching application automatically populates this field when a coach completes a survey for the trainee.

</td></tr><tr><td>

Follow up

</td><td>

Whether the coach must take further action to improve the trainee performance.

</td></tr><tr><td>

Comments

</td><td>

Notes, if any, to add about the assessment.

</td></tr><tr><td>

Survey taken by coach

</td><td>

Survey for the trainee taken by the coach.You can add a survey for an assessment when you create the assessment manually or when the coaching opportunity triggers an assessment that does not have a survey.

 When a coaching opportunity triggers an assessment and contains a survey, the survey is automatically added to the assessment and cannot be changed by the coach.

</td></tr><tr><td>

Survey taken by trainee

</td><td>

Survey for the coach taken by the trainee.

</td></tr><tr><td>

Add skills

</td><td>

Skills to add to the trainee profile when the assessment is complete. When you click this field, it displays all skills and the skill levels that are not in the trainee profile.

</td></tr><tr><td>

Add training

</td><td>

Training to assign to the trainee.You can also assign learning tasks from course items.

</td></tr></tbody>
</table>5.  Do the following:

    -   To complete the adhoc assessment, click **Save**.
    -   To complete assessments creating using coaching opportunities, click **Complete assessment**.

## Manage skills using Workforce Optimization for Customer Service

Add or update skills for an agent. You can approve predicted skills if the skill is necessary for the agent to complete assigned tasks. You can also reject a skill if it doesn't apply to the agent.

### Before you begin

Role required: skill\_manager

### About this task

The Predictive Intelligence application for skills displays the recommended skills on each agent's profile. The application uses sample cases that the agent has worked on to recommend skills for an agent.

You can view skills for all users grouped by assignment group and the overall skill coverage for each group.

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching \(![Coaching icon.](../image/coaching-new.png)\) icon.

3.  Click the **Skills** tab.

    You can view the list of all assigned skills and the skill level for each agent on your team. For more information on skills and skills levels, see Skills Management.

    You can also filter the skill matrix based on users, groups, skill type, skill level, or skill category. Reset the filter if you want to view the skills for all users.

4.  Add a skill or skill level.

<table id="choicetable_ufk_1hx_nlb"><thead><tr><th align="left" id="d154966e1038">

To

</th><th align="left" id="d154966e1041">

Do this

</th></tr></thead><tbody><tr><td id="d154966e1047">

**Add a skill**

</td><td>

1.  In the skill matrix, click **Add** for the skill that you want to add to the agent.
2.  Select the **Skill Level** field and choose a level for the skill.
3.  Click **OK**.
The skill gets automatically added to the agent.

</td></tr><tr><td id="d154966e1077">

**Update a skill level**

</td><td>

1.  In the skill matrix, select a skill level for an agent.
2.  Select the skill level that you want to add for the agent.
3.  Click **OK**.


</td></tr></tbody>
</table>5.  Approve or reject a skill that is recommended by Predictive Intelligence.

    1.  In the skill matrix, click **Recommended** to approve and recommend a skill for the user.
    2.  In the **Details** tab, review the request for skill approval, the sample case resolutions that were used to predict the skill, and the activity stream.
    -   To approve a skill, click **Approve**. The skill is added to the agent and the lowest level for the skill is automatically associated with the added skill. The state for the request changes to **Approved** and the skill is added to the agent.
    -   To reject a skill, click **Reject**. The state for the request changes to **Rejected**. Predictive Intelligence does not recommend the skill for the user again and the field changes to **Add**.
    -   Click the More Options \(![More options icon.](../image/ellipsis-new.png)\) icon and select **Save**.
    The application assigns the skill to the user. If the assigned skill does not have a skill level, the application adds the basic skill level to the user.


## Coaching with Learning

Use Coaching with Learning to train your agents with internal and external learning content. Organize similar content in catalogs. Assign learning tasks and track completion.

**Important:** Coaching with Learning is available when you enable the Coaching with Learning application from the ServiceNow® Store. To enable this application, see [Activate Workforce Optimization for Customer Service](../task/request-configurable-wfo-cs.md).

### Create a learning catalog

Create a catalog to organize related content into categories.

#### Before you begin

Role required: sn\_lc.catalog\_manager

#### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching \(![Coaching icon.](../image/coaching-new.png)\) icon.

3.  Click the **Learning** tab.

4.  Click **Learning Catalogs** and select **My Catalogs**.

5.  Create a catalog.

    1.  Click **New**.
    2.  In the **Title** field, enter a unique name for the catalog.
    3.  In the **Description** field, enter a description for the catalog.
    4.  Click **Save**.
    **Note:** The catalog is visible to all groups that you directly or additionally manage.

6.  Add course items to the catalog.

    1.  Click the **Content** tab.
    2.  Click **Add**.
    3.  In the **Add Learning Courses** pop-up window, select all course items you want to add to the catalog.
    4.  Click **Add**. The course items are added to the catalog.
    **Note:** To remove any course item you have added, select the course item and click **Remove**.

7.  Add a group to a catalog.

    1.  Click the **Applicable Groups** tab.
    2.  Click **New**.
    3.  In the **Group** field, select a group that you want to associate with the catalog.
    4.  Click **Save**.

### Create a learning task

Create learning tasks for agents to keep track of their learning activities.

#### Before you begin

Role required: sn\_lc.task\_creator

#### About this task

Set learning task completion due dates to include or exclude weekends using the **exclude\_weekends\_on\_learning\_task\_due\_date** system property. For more information, see [Workforce Optimization for Customer Service Reference](../reference/components-installed-configurable-wfo-cs.md).

#### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching \(![Coaching icon.](../image/coaching-new.png)\) icon.

3.  Click **Learning Tasks** and select **All Tasks**.

4.  Create a learning task.

    1.  Click **New**.
    2.  Fill in the following fields.

<table id="table_pr4_zgk_bpb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assigned to

</td><td>

Name of the agent to whom you want to assign the learning task.

</td></tr><tr><td>

Course item

</td><td>

The course that needs to be completed by the agent.

</td></tr><tr><td>

Due date

</td><td>

Date when the agent must complete the course. Default is 5 days after the creation of the learning task. This value is calculated from the **Days to Complete** field for the course item. The due date field is highlighted as follows:-   Green—if the task is due before the current day.
-   Yellow—if the task is due on the current day.
-   Red—if the task is due after the current day.


</td></tr><tr><td>

Catalog

</td><td>

The catalog that contains the course item for the learning task.

</td></tr></tbody>
</table>5.  Click **Save**.


### Create internal learning content

Add internal courses so that agents can learn new content and enhance their skill set.

#### Before you begin

Role required: sn\_lc.content\_creator

#### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching \(![Coaching icon.](../image/coaching-new.png)\) icon.

3.  Click **Learning Courses** and select **Internal Courses**.

4.  Create an internal learning course.

    1.  Click **New**.
    2.  Fill in the following fields in the Details tab.

<table id="table_bdh_5jk_bpb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the course.

</td></tr><tr><td>

Internal source

</td><td>

Select the type of content for the course.Here are the available types of courses:

 -   URL—YouTube, Vimeo, or any link for a video
-   Knowledge article
-   Free form


</td></tr><tr><td>

Days to complete

</td><td>

The number of days required to complete the course. Default value is set to 5.

</td></tr><tr><td>

Estimated duration

</td><td>

Length of time when the course has to be completed. For example, for a video, it is the duration of the video. For a KB article, the duration is estimated based on the length of the article.

</td></tr><tr><td>

Description

</td><td>

Description of the course.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  Add a skill to the internal content.

    1.  Select the **Associated skills** tab.
    2.  Select **New**.
    3.  In the **Skill** field, select a skill you want to associate with the internal content.
    4.  In the **Skill level** field, select a skill level for the selected skill.
    5.  Select **Save**.
7.  Add a learning task to the internal content.

    1.  Select the **Learning Tasks** tab.
    2.  Select **New**.
    3.  In the **Assigned to** field, select a trainee to whom you want to assign the learning task.
    4.  In the **Catalog** field, select the catalog to associate with the learning task.
    5.  In the **Due date** field, select the calendar icon and select the date and time when you want to trainee to complete the learning task.
    6.  Select **Save**.

### Add external courses to coaching with learning

Add courses from external sources such as Udemy, Pluralsight, or Cornerstone to enable your users to gain skills from external content.

#### Before you begin

Role required: sn\_lc.learning\_admin

#### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching \(![Coaching icon.](../image/coaching-new.png)\) icon.

3.  Click the **Learning** tab.

4.  Go to **Learning Courses** &gt; **External Courses**.

5.  Select a course.

6.  Click **Go to course**.

    You can review and learn the external course.


