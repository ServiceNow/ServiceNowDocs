---
title: Workforce Optimization for Field Service components
description: Several types of components are installed with activation of the Workforce Optimization for Field Service \(com.snc.app\_fsm\_wfo\) plugin, including user roles, key performance indicators \(KPIs\), scheduled jobs, properties, and tables.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Workforce Optimization for Field Service components

Several types of components are installed with activation of the Workforce Optimization for Field Service \(com.snc.app\_fsm\_wfo\) plugin, including user roles, key performance indicators \(KPIs\), scheduled jobs, properties, and tables.

## Workforce Optimization for Field Service

<table id="table_fbd_qxp_dlb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Workforce Optimization User \[sn\_wfo.user\]

</td><td>

Grants read access to primary group and additional managers.

</td><td>

pa\_analyst

</td></tr><tr><td>

Workforce Optimization Admin \[sn\_wfo\_fsm.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) additional managers.

</td><td>

sn\_wfo.user

</td></tr><tr><td>

Workforce Optimization FSM Manager \[sn\_wfo\_fsm.manager \]

</td><td>

Grants rights to create, read, or update, coaching, scheduling, teams, or channel management applications.

</td><td>

-   skill\_manager
-   wm\_manager
-   sn\_wfo\_cfg\_ws.manager
-   sn\_shift\_planning.admin
-   sn\_customerservice\_manager
-   sn\_wfo.user
-   sn\_channel\_mgmt.user
-   sn\_coaching.coach
-   sn\_sre.user
-   sn\_team\_perf.team\_performance\_user

</td></tr><tr><td>

Workforce Optimization FSM Admin \[sn\_wfo\_fsm.admin \]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) coaching, scheduling, teams, or channel management applications.

</td><td>

-   agent\_schedule\_admin
-   sn\_wfo\_fsm.manager
-   sn\_coaching\_admin

</td></tr></tbody>
</table>## Scheduling

<table id="table_ztx_jwc_llb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Shift Planning User \[sn\_shift\_planning.user\]

</td><td>

Grants read access for scheduling including the ability to view schedules and shifts.

</td><td>



</td></tr><tr><td>

Shift Planning Agent \[sn\_shift\_planning.agent\]

</td><td>

Grants agents access to their calendar and request shift swap or time-off.

</td><td>

sn\_shift\_planning.user

</td></tr><tr><td>

Shift Planning Admin \[sn\_shift\_planning.admin\]

</td><td>

Grants administrative access to create, read, update, and delete \(CRUD\) schedules and work shifts.

</td><td>

-   sn\_shift\_planning.approver
-   sn\_shift\_planning.user
-   sn\_shift\_planning.agent

</td></tr></tbody>
</table>|Table|Description|
|-----|-----------|
|sn\_shift\_planning\_time\_worked\_summary|Stores the time worked summary of an agent.|
|sn\_shift\_planning\_agent\_time\_work|Stores the agent's time worked, such as clock-in and clock-out times. If an agent logs in early or logs out late, then the shift start and shift end times are stored in place of the clock-in and clock-out times.|
|sn\_shift\_planning\_agent\_time\_attendance|Stores the clock-in and clock-out times of agents. Data is retrieved when an agent logs in, logs out, or changes the Presence state.|

<table id="table_ywt_4t1_gnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_shift\_planning.number\_of\_days\_to\_cache

</td><td>

Number of days to cache agent schedules.-   **Type:** Integer
-   **Default value:** 5

</td></tr><tr><td>

sn\_shift\_planning.enable\_schedule\_adherence

</td><td>

Calculates and displays schedule adherence information for your agents.-   **Type:** Boolean
-   **Default value:** True

</td></tr><tr><td>

sn\_shift\_planning.early\_clockin\_threshold

</td><td>

Threshold settings indicate how many minutes early or late an agent can clock-in or clock-out from the scheduled time without being considered non-adherent. This is the acceptable duration of time flexibility for an agent to start work before the scheduled start time. -   **Type:** Integer
-   **Default value:** 60 min

</td></tr><tr><td>

sn\_shift\_planning.adherence\_threshold

</td><td>

Sets the percentage for a threshold in adherence. The agents who do not qualify as above the defined threshold value \(70%\) are considered non-adherent agents. -   **Type:** Integer
-   **Default value:** 70%

</td></tr><tr><td>

sn\_shift\_planning.conformance\_lower\_threshold

</td><td>

Set the lower threshold percentage for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered non-conformant agents. -   **Type:** Integer
-   **Default value:** 80%

</td></tr><tr><td>

sn\_shift\_planning.conformance\_upper\_threshold

</td><td>

Sets the upper threshold percentage for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered non-conformant agents.-   **Type:** Integer
-   **Default value:** 120%

</td></tr><tr><td>

sn\_shift\_planning.auto\_clockout\_threshold

</td><td>

Threshold time for the system to wait and generate automatic clock-out events when agents forget to clock-out. For example, if the threshold is set to 60 minutes and an agent's planned work shift is 8 a.m. to 5 p.m. but the agent fails to clock out at 5 p.m., the system waits for 60 minutes and then generates an automatic clock-out event. -   **Type:** Integer
-   **Default value:** 60 min

</td></tr><tr><td>

sn\_fsm\_disp\_wrkspc.agent\_shift\_schdlng\_event\_color

</td><td>

Enables the default colors configured for each event type to display the same event spans with same color in Dispatcher Workspace.**Note:** You must select a dynamic value to display the selected color of workforce optimization events in Dispatcher Workspace.

 -   **Type:** String
-   **Default value:** static

</td></tr></tbody>
</table>|Script Include|Description|
|--------------|-----------|
|Notify User Clock In|Counts the clock-in events whenever there is a change in agent's Presence state.|
|Notify User Clock Out|Counts the clock-out events whenever there is a change in agent's Presence state.|

<table id="table_vxk_ndy_pnb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shift Planning - Delete All Agent Schedules Cache

</td><td>

Deletes cache from the sn\_shift\_planning\_agent\_availability table.-   Runs automatically everyday at 2:30 a.m.
-   Run this job on demand when you import data.

</td></tr><tr><td>

Clock-out event generation \(For scenarios where the clock-out event does not get triggered\)

</td><td>

Generates clock-out events every 4 hours if agents haven't clocked out. **Note:**

For example, say an agent's work shift times are from 8 a.m. to 5 p.m. and the **sn\_shift\_planning.auto\_clockout\_threshold** property value is set to 60 minutes. If the agent clocks in and fails to clock out, the scheduled job waits till 6 p.m. \(5 p.m.+60 minutes\) and if there is no clock out till 6 p.m., the system generates a clock-out event with the agent's shift end time.

</td></tr><tr><td>

Populate Agent Time Worked Summary

</td><td>

Runs daily to calculate the time worked, adherence, and conformance based on an agent's planned and actual work shift times for the previous day. The values are stored in the \[sn\_shift\_planning\_time\_worked\_summary\] table.

</td></tr><tr><td>

Update Wrapper End Time for Actual Work Events

</td><td>

Runs daily to make sure the actual work wrapper end-time is equal to last clock-out time.

</td></tr><tr><td>

\[Schedule Adherence\] Daily Data Collection

</td><td>

Runs the job daily and collects data for all teams indicators.

</td></tr><tr><td>

\[Schedule Adherence\] Historic Data Collection

</td><td>

Runs the job and collects historic data for all teams indicators.

</td></tr><tr><td>

\[Schedule Adherence\] Weekly Data Collection

</td><td>

Runs the job weekly and collects data for all indicators in Manager Workspace.

</td></tr></tbody>
</table>## Teams

<table id="table_lcw_kwc_llb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Teams User \[sn\_team\_perf.team\_performance\_user\]

</td><td>

Grants access to read KPI tables.

</td><td>

-   sn\_wfo.user
-   pa\_analyst

</td></tr><tr><td>

Teams Admin \[sn\_team\_perf.team\_performance\_admin\]

</td><td>

Grants access to create and configure KPIs, KPI groups, and assignment groups in the Teams module.

</td><td>

-   sn\_wfo.admin
-   sn\_team\_perf.team\_performance\_user

</td></tr></tbody>
</table><table id="table_ojw_fby_llb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_team\_perf.kpi\_group.max\_parent\_kpis

</td><td>

The maximum number of parent indicators that you can add to one KPI group.-   **Type:** Integer
-   **Default value:** 5

</td></tr><tr><td>

sn\_team\_perf.kpi\_group.max\_supporting\_kpis

</td><td>

The maximum number of supporting KPIs you can define for a parent KPI.-   **Type:** Integer
-   **Default value:** 10

</td></tr><tr><td>

sn\_team\_perf.ws.max\_assignment\_groups

</td><td>

The maximum number of assignment groups prioritized by order number to display on the Teams application in Manager Workspace.-   **Type:** Integer
-   **Default value:** 15

</td></tr><tr><td>

sn\_team\_perf.default\_date\_range

</td><td>

The default date range set in the date range picker.-   **Type:** Integer
-   **Default value:** 30

</td></tr></tbody>
</table>|Indicator Name|Description|
|--------------|-----------|
|\# of tasks resolved on first contact|Number of tasks resolved on first contact.|
|\# of P1 tasks resolved on first contact|Number of P1 tasks resolved on first contact.|
|\# of P2 tasks resolved on first contact|Number of P2 tasks resolved on first contact.|
|\# of P3 tasks resolved on first contact|Number of P3 tasks resolved on first contact.|
|\# of P4 tasks resolved on first contact|Number of P4 tasks resolved on first contact.|
|MTTR for Tasks|Mean time to resolve the tasks.|
|MTTR for P1 Tasks|Mean time to resolve the P1 tasks.|
|MTTR for P2 Tasks|Mean time to resolve P2 tasks.|
|MTTR for P3 Tasks|Mean time to resolve the P3 tasks.|
|MTTR for P4 Tasks|Mean time to resolve P4 tasks.|
|CSAT for Tasks|Customer satisfaction score for tasks.|
|CSAT for P1 Tasks|Customer satisfaction score for P1 tasks.|
|CSAT for P2 Tasks|Customer satisfaction score for P2 tasks.|
|CSAT for P3 tasks|Customer satisfaction score for P3 tasks.|
|CSAT for P4 tasks|Customer satisfaction score for P4 tasks.|
|Number of Closed tasks|Number of closed tasks.|
|Number of Closed P1 tasks|Number of closed P1 tasks.|
|Number of Closed P2 tasks|Number of closed P2 tasks.|
|Number of Closed P3 tasks|Number of closed P3 tasks.|
|Number of Closed P4 tasks|Number of closed P4 tasks;|
|Average Wait Time for Chats|Average waiting time for chats.|
|Number of Chats Handled|Number of chats handled.|
|Average Handling Time for Chats|Average handling time for chats.|
|Number of Abandoned Chats|Number of abandoned chats.|
|Number of Incoming tasks|Number of incoming tasks.|
|Schedule Adherence|Agents schedule adherence percentage.|
|Schedule Conformance|Agents schedule adherence percentage.|
|Summed duration of Time Worked|Agents total duration of time worked.|
|Summed Duration of Planned Time|Agents total duration of planned time.|
|Summed duration of Time Not Worked|Agents total duration of time not worked.|
|Summed duration of Available Non Planned Time|Agents total duration of available non planned time.|

## Coaching

<table id="table_q14_lwc_llb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Coaching Admin \[sn\_coaching.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) coaching opportunities, assessments, training, and skills.

</td><td>

-   sn\_coaching.coach
-   sn\_lc.learning\_admin

</td></tr><tr><td>

Coaching Coach \[sn\_coaching.coach\]

</td><td>

Grants administrative rights to create, read, or update coaching opportunities, assessments, training, and skills.

</td><td>

-   sn\_coaching.trainee
-   pa\_viewer
-   sn\_lc.catalog\_manager

</td></tr><tr><td>

Coaching Trainee \[sn\_coaching.trainee\]

</td><td>

Grants access to add training, assessments, and skill records.

</td><td>

-   skill\_user
-   pa\_viewer
-   survey\_reader

</td></tr></tbody>
</table>**Important:** This feature is available with the Workforce Optimization for Field Service \(com.snc.app\_fsm\_wfo\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

|Business rule|Table|Description|
|-------------|-----|-----------|
|Calculate coaching survey score|Assessment Instance \[asmt\_assessment\_instance\]|Sets the feedback rating based on the survey score.|

|Coaching Opportunity Name|Description|Table|
|-------------------------|-----------|-----|
|Coaching Opportunity for SLA Breach|Coaching opportunity for agents who worked on the critical and high priority tasks that breached SLA.|Task SLA \[task\_sla\]|
|Coaching Opportunity for low CSAT|Coaching opportunity for agents who worked on tasks that has a customer satisfaction score less than 4.|Task Report \[sn\_customerservice\_task\_report\]|
|Coaching Opportunity for skills award verification|Coaching opportunity for verification of skills awarded to agents.|Task \[sn\_customerservice\_task\]|
|Knowledge Management Process: Coaching on quality of knowledge articles|Coaching opportunity for agents who need to improve the quality of a knowledge article by reviewing the assessment.|Task \[sn\_customerservice\_task\]|
|Coaching Opportunity for high TTR|Coaching opportunity for agents who worked on a task that had a time to resolution of more than 3 days.|task Report \[sn\_customerservice\_task\_report\]|
|Interaction: Coaching Opportunity for Handling Time|Coaching opportunity for agents who had a handle time of more than 10 minutes on an interaction.|Interaction \[interaction\]|

**Note:** You can customize the coaching opportunities for low CSAT, high TTR, SLA breach, and handling time based on your business needs.

**Important:** This feature is available with the Workforce Optimization for Field Service \(com.snc.app\_fsm\_wfo\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

|Name|Description|
|----|-----------|
|Chat Quality Survey|Survey associated with the Chat Interaction coaching opportunity. The coach assesses the agent using this survey after the agent completes a chat interaction.|
|Task Quality Survey|Survey associated with the Task Interaction coaching opportunity. The coach assesses the agent using this survey after the agent completes a task interaction.|

<table id="table_u2w_jh5_fnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_coaching.learning\_default\_duration

</td><td>

Number of days to read a knowledge article or complete training. The admin \(sn\_wfo.admin\) sets the number of days for the trainee to complete reading an article or complete training. The number of days is converted to the due date for the trainee to complete the training. It is calculated from the current date, taking the trainee's time zone into consideration.-   **Type:** Integer
-   **Default value:** 5

</td></tr><tr><td>

sn\_coaching.exclude\_weekends\_on\_training\_due\_date

</td><td>

Excludes weekends when the due date is set for trainees to complete training.-   **Type:** true \| false
-   **Default value:** true

</td></tr></tbody>
</table>## Coaching with Learning

**Important:** This feature is available with the Workforce Optimization for Field Service \(com.snc.app\_fsm\_wfo\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

<table id="table_fk4_mwq_npb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

Learning admin \[sn\_lc.learning\_admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) catalog, learning content, roles, and configure learning source.

</td><td>

-   sn\_lc.catalog\_manager
-   sn\_hr.integr\_fw.admin

</td></tr><tr><td>

Learning catalog manager \[sn\_lc.catalog\_manager\]

</td><td>

Grants administrative rights to create, read, or update learning catalogs.

</td><td>

-   sn\_lc.task\_creator
-   sn\_lc.content\_writer

</td></tr><tr><td>

Learning catalog group manager \[sn\_lc.catalog\_group\_manager\]

</td><td>

Grants administrative rights to create, read, or update learning catalogs based on groups.

</td><td>

-   sn\_lc.task\_creator
-   sn\_lc.content\_writer

</td></tr><tr><td>

Learning content creator \[sn\_lc.content\_creator\]

</td><td>

Grants administrative rights to create, read, or update internal courses.

</td><td>

sn\_lc.content\_reader

</td></tr><tr><td>

Learning content writer \[sn\_lc.content\_writer\]

</td><td>

Grants read or write access for learning courses.

</td><td>

sn\_lc.content\_creator

</td></tr><tr><td>

Learning content reader \[sn\_lc.content\_reader\]

</td><td>

Grants read access for learning courses.

</td><td>

none

</td></tr><tr><td>

Learning content advisor \[sn\_lc.learning\_advisor\]

</td><td>

Can assign learning tasks.

</td><td>

none

</td></tr><tr><td>

Learning task creator \[sn\_lc.task\_creator\]

</td><td>

Grants read or write access for learning tasks.

</td><td>

none

</td></tr></tbody>
</table><table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Learning External Content\[sn\_lc\_external\_content\]

</td><td>

Stores details of external course items pulled from third-party systems.

</td></tr><tr><td>

Learning User Course Activity\[sn\_lc\_user\_course\_activity\]

</td><td>

Stores details of learning course activities such as the user to whom the course is assigned, status, due date, and name of the learning course.

</td></tr><tr><td>

Learning Content\[sn\_lc\_content\]

</td><td>

Stores details of internal learning content such as knowledge articles or videos that are created in ServiceNow.

</td></tr><tr><td>

Learning Course Item\[sn\_lc\_course\_item\]

</td><td>

Stores details of learning course items such as the source to which the learning course belongs.

</td></tr><tr><td>

Learning Catalog\[sn\_lc\_catalog\]

</td><td>

Stores details of learning catalog items with its course items.

</td></tr><tr><td>

Learning Task\[sn\_lc\_learning\_task\]

</td><td>

Stores details of learning tasks, such as the user to whom the learning task is assigned and the date by which the learning task must be completed.

</td></tr><tr><td>

Learning System Configuration\[sn\_lc\_learning\_system\_configuration\]

</td><td>

Stores configuration parameters of third-party learning management system sources.

</td></tr></tbody>
</table><table id="table_bzr_kkw_dpb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.sn\_coaching\_assessment\_activity.fields

</td><td>

Edit coaching assessment activities.-   **Type:** string
-   **Default value:** assigned\_to,cmdb\_ci,state,impact,priority,opened\_by,work\_notes,comments,\*Attachments\*,assessment\_of

</td></tr><tr><td>

sn\_coaching.recommended\_learning\_deprecated

</td><td>

Coaching recommended trainings is being deprecated and replaced with learning tasks and course items from Coaching With Learning.-   **Type:** string
-   **Default value:** true

</td></tr><tr><td>

sn\_coach.lrn.exclude\_weekends\_on\_learning\_task\_due\_date

</td><td>

Enable property to exclude weekends while setting the due date for learning tasks.-   **Type:** true\|false
-   **Default value:** true

</td></tr><tr><td>

sn\_coach\_lrn.learning\_list\_menu\_props

</td><td>

Data array properties for the now-list-menu component on the Learning Tasks tab, coaching module.-   **Type:** string
-   **Default value:** script for data array

</td></tr><tr><td>

com.glide.transform.json.max-partial-length

</td><td>

Transforms JSON objects to internal objects and sets the word limit for records fetched through an API call.-   **Type:** integer
-   **Default value:** 16384

 **Note:**

You must add this system property to set the desired value. For more information, see [Add this system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

When you synchronize third-party learning content with your ServiceNow instance, if the word count of the content being pulled into your instance exceeds the value set for this property, the synchronization will fail. For more information, see [Integrate Coaching With Learning with third-party learning management systems](https://www.servicenow.com/docs/access?context=integrate-learning-third-party-configurable-wfo-cs&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

com.snc.process\_flow.reporting.serialized.val\_size\_limit

</td><td>

Specify the number of bytes allowed for runtime values in each step in the flow execution details. To prevent truncation, set the value to an integer equal to or less than zero.-   **Type:** integer
-   **Default value:** 16384

 **Note:** When you synchronize third-party learning content with your ServiceNow instance, if the word count of the content being pulled into your instance exceeds the value set for this property, the synchronization will fail. For more information, see [synchronize](https://www.servicenow.com/docs/access?context=integrate-learning-third-party-configurable-wfo-cs&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

</td></tr></tbody>
</table>**Important:** This feature is available with the Workforce Optimization for Field Service \(com.snc.app\_fsm\_wfo\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

## Skill Recommendation

<table id="table_sql_wbd_llb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Skill Recommendation User \[sn\_sre.user\]

</td><td>

Grants rights to view skill recommendation tables.

</td><td>

wfo.user

</td></tr><tr><td>

Skill Recommendation Admin \[sn\_sre.admin\]

</td><td>

Grants administrative rights to edit the properties for skill recommendation.

</td><td>

-   wfo.admin
-   sn\_sre.user

</td></tr></tbody>
</table>Navigate to **Skill Recommendation** &gt; **Configuration** to configure these properties.

<table id="table_zhp_cdq_dlb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable skill recommendation.

sn\_sre.enable\_skill\_recommendation

</td><td>

Enable this property to start recommending skills for agents.-   **Type:** true \| false
-   **Default value:** true

</td></tr><tr><td>

Maximum number of skills to predict based on supervised learning.

sn\_sre.max\_supervised\_skills

</td><td>

Using supervised learning, the maximum number of skills to predict for each incident ordered by confidence of prediction.-   **Type:** Integer
-   **Default value:** 3

</td></tr><tr><td>

Maximum number of skills to predict based on supervised learning.

sn\_sre.max\_unsupervised\_skills

</td><td>

Using unsupervised learning, the maximum number of skills to predict for each incident ordered by confidence of prediction.-   **Type:** Integer
-   **Default value:** 3

</td></tr><tr><td>

Number of times Predictive Intelligence must predict the same skill for an agent before recommending it for the agent.

sn\_sre.user\_predicted\_skill\_threshold

</td><td>

The number of times Predictive Intelligence must predict the same skill for an agent before recommending the skill for the agent. -   **Type:** Integer
-   **Default value:** 20

</td></tr><tr><td>

Similarity solution definition to recommend skills from similar tasks.

sn\_customerservice.unsupervised\_solution\_definition\_for\_tasks

</td><td>

Name of the Predictive Intelligence solution definition used for predicting skills to resolve tasks using unsupervised learning. If you have created your own solution definition, you can replace the default one with the one you have created.-   **Type:** String
-   **Default value:**ml\_sn\_sn\_customerservice\_global\_recommend\_similar\_skills\_for\_tasks

</td></tr><tr><td>

Similarity solution definition to recommend skills for tasks.

sn\_customerservice.supervised\_solution\_definition\_for\_tasks

</td><td>

Name of the Predictive Intelligence solution definition used for predicting skills to resolve tasks using supervised learning. If you have created your own solution definition, you can replace the default one with the one you have created.-   **Type:** String
-   **Default value:**ml\_sn\_sn\_customerservice\_global\_recommend\_skills\_from\_similar\_tasks

</td></tr></tbody>
</table>|Scheduled job|Description|
|-------------|-----------|
|Start skill prediction|Runs the job every day at 1 a.m. on all incidents that were closed the previous day. Recommends the skills necessary to close the incidents to resolve similar open incidents.|

<table id="table_gkk_4hd_llb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Predicted Skill \[sn\_sre\_user\_predicted\_skill\]

</td><td>

-   Stores how many times a skill has been predicted for the user.
-   Skills not recommended in the last 60 days are automatically deleted from this table.

</td></tr><tr><td>

Task Predicted Skill \[sn\_sre\_task\_predicted\_skill\]

</td><td>

-   Stores the skills predicted to resolve each type of incident.
-   Records created over 60 days ago are automatically deleted from this table.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

