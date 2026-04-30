---
title: Workforce Optimization for HR reference
description: Workforce Optimization for HR reference includes information about the roles, system properties, and tables installed.Several types of components are installed with activation of Workforce Optimization for HR application, including user roles, key performance indicators \(kpis\), scheduled jobs, properties, and tables.
locale: en-US
release: xanadu
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 16
breadcrumb: [Workforce Optimization for HR Overview, HR Service Delivery, Employee Service Management]
---

# Workforce Optimization for HR reference

Workforce Optimization for HR reference includes information about the roles, system properties, and tables installed.

## Components installed with Workforce Optimization for HR

Several types of components are installed with activation of Workforce Optimization for HR application, including user roles, key performance indicators \(kpis\), scheduled jobs, properties, and tables.

### Workforce Optimization for HR

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|Workforce Optimization User \[sn\_hr-wfo.user\]|Typically uses Workforce Optmization for HR.|sn\_hr-wfo.user|
|Workforce Optimization Admin \[sn\_hr\_wfo.admin\]|Grants administrative rights to create, read, update, and delete \(CRUD\) additional managers.|sn\_hr\_wfo.admin|
|Workforce Optimization HR Manager \[sn\_hr\_wfo.manager\]|Grants rights to create, read, or update, coaching, scheduling, teams, or channel management applications.|sn\_hr\_wfo.manager|

|Properties|Description|
|----------|-----------|
|sn\_hr\_wfo.hr\_group\_types|System property that ensures the right HR related lists are rendered on the records in team performance module. The logged in user should belong to a group of the group types \(sysId\) specified in this property.|

<table id="table_jg2_3z2_wpb"><thead><tr><th>

Module Name

</th><th>

Module Tables/Database View

</th></tr></thead><tbody><tr><td>

Manager Workspace

</td><td>

Stores filter configurations for all applications such as, Schedule, and Coaching. \[sn\_mgr\_workspace\_filter\_configuration\]

</td></tr><tr><td>

Schedule

</td><td>

-   User \[sys\_user\]
-   User Skill \[sys\_user\_has\_skill\]
-   Agent Schedule \[sys\_shift\_planning\_agent\_schedule\]
-   Schedule Event \[sn\_shift\_planning\_event\]
-   Manager Groups database view \[sn\_wfo\_manager\_group\]

</td></tr><tr><td>

Coaching

</td><td>

-   Skill \[cmn\_skill\]
-   Skill Category M2M \[cmn\_skill\_m2m\_category\]
-   Group Member \[sys\_user\_grmember\]

</td></tr></tbody>
</table>### Manager Workspace

<table id="table_klf_rxp_dlb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Manager Workspace User \[sn\_mgr\_workspace.user\]

</td><td>

Grants read access to home and list modules.

</td><td>

workspace\_user

</td></tr><tr><td>

Manager Workspace Manager \[sn\_mgr\_workspace.manager\]

</td><td>

Grants read access to primary group, additional managers, and the approval button.

</td><td>

-   sn\_mgr\_workspace.user
-   sn\_wfo.user

</td></tr><tr><td>

Manager Workspace Admin \[sn\_mgr\_workspace.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) all applications and settings in Manager Workspace.

</td><td>

-   sn\_mgr\_workspace.manager
-   workspace\_admin
-   ui\_builder\_admin

</td></tr></tbody>
</table><table id="table_xrj_g32_5lb"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cnm\_skills.ws\_max\_users\_swap\_skill\_matrix

</td><td>

The maximum limit for the number of users that allows you to swap axes in the skill matrix.-   **Type:**Integer
-   **Default value:**50

</td></tr></tbody>
</table>|Indicator Name|Description|
|--------------|-----------|
|No. of cases resolved|Number cases resolved the first time it was handled.|
|No. of cases not updated in last 30 days|Number of cases that are not updated since 30 days.|
|No. of resolved cases reopened|Number of cases reopened because issues were not addressed properly.|
|No. of escalated open cases|Number of cases that are not worked on and are escalated.|

|Scheduled job|Description|
|-------------|-----------|
|Daily Data Collection|Runs the job daily and collects data for all teams indicators.|
|Historic Data Collection|Runs the job and collects historic data for all teams indicators.|
|Weekly Data Collection|Runs the job weekly and collects data for all indicators in Manager Workspace.|

### Scheduling

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
|sn\_shift\_planning\_agent\_time\_work|Stores the agent's time worked, such as clock-in and clock-out timings. If an agent logs in early or logs out late, then the shift start and shift end times are stored in place of clock-in and clock-out timings.|
|sn\_shift\_planning\_agent\_time\_attendance|Stores the clock-in and clock-out timings of agents. Data is retrieved when an agent logs in, logs out or changes the presence state.|

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
-   **Default value:**True

</td></tr><tr><td>

sn\_shift\_planning.early\_clockin\_threshold

</td><td>

Threshold settings indicate how many minutes early or late an agent can clock-in or clock-out to the scheduled time without being considered non-adherent. This is the acceptable duration of time flexibility for an agent to start work before the scheduled start time. -   **Type:** Integer
-   **Default value:**60 min

</td></tr><tr><td>

sn\_shift\_planning.adherence\_threshold

</td><td>

Set the percentage for a threshold in adherence. The agents who do not qualify to be above the defined threshold value \(70%\) are considered non-adherent agents. -   **Type:** Integer
-   **Default value:**70%

</td></tr><tr><td>

sn\_shift\_planning.conformance\_lower\_threshold

</td><td>

Set the lower threshold percentage for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered non-conformance agents. -   **Type:** Integer
-   **Default value:**80%

</td></tr><tr><td>

sn\_shift\_planning.conformance\_upper\_threshold

</td><td>

Set the upper threshold percentage for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered non-conformance agents.-   **Type:** Integer
-   **Default value:**120%

</td></tr><tr><td>

sn\_shift\_planning.auto\_clockout\_threshold

</td><td>

Threshold time for the system to wait and generate automatic clock-out events when agents forgets to clock-out. For example, if an agent's planned work shift is 8 AM to 5 PM and fails to clock out at 5 PM, the system waits for 60 min as threshold time and generates an automatic clock-out event. -   **Type:** Integer
-   **Default value:**60 min

</td></tr></tbody>
</table><table id="table_vxk_ndy_pnb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shift Planning - Delete All Agent Schedules Cache

</td><td>

Deletes cache from the sn\_shift\_planning\_agent\_availability table.-   Runs automatically everyday at 2:30 am
-   Run this job on-demand when you import data.

</td></tr><tr><td>

Clock-out event generation \(For scenarios where clock-out event does not get triggered\)

</td><td>

Generates clock-out events every 4 hours if agents haven't clocked-out. **Note:** Consider an agent's work shift timings are from 8 AM to 5 PM and **sn\_shift\_planning.auto\_clockout\_threshold** property value is set to 60 minutes. The agent clocks-in and fails to clock out, the scheduled job waits till 6 PM\(5 PM+60 minutes\) and if there is no clock out till 6 PM, the system generates a clock-out event with agent's shift end time.

</td></tr><tr><td>

Populate Agent Time Worked Summary

</td><td>

Runs daily to calculate the time worked, adherence and conformance based on agent's planned and actual work shift timings of the previous day. The values are stored in \[sn\_shift\_planning\_time\_worked\_summary\] table.

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
</table>**Setting the due date for time-off and shift-swap request approvals:**Administrators can configure the due date logic for the Time Off Request and Shift Swap Request approval flows. The approval due date is set as the number of days before the request start date. The default is set to two days which means if the approval is not approved two days before the request start date, it will be auto-rejected. For information on configuring flows, refer to [Build your first flow in Flow Designer](https://www.servicenow.com/docs/access?context=build-your-first-flow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

### Demand Forecast

|Name|Description|
|----|-----------|
|Cases Assigned|Collects data for cases.|
|Chat Interactions Created|Collects data for chat interactions.|

The **WFO Forecast** time series metric retention policy is available by default for all forecast configurations. By default, this retention policy stores data at a 15min interval for the past three years for all zboot customers.

|Name|Formula to create this resource forecast configuration|
|----|------------------------------------------------------|
|Resources for Sales Support|`([FC:Chat Interactions Created] * [FP:Average Chat Work Time - Sales Support]`|
|Resources for Service Support|`([FC:Cases Assigned]*[FP:Average Case Work Time - Service Support]) + ([FC:Chat Interactions Created]*[FP:Average Chat Work Time -Service Support])`|
|Resources for Tech Support|`([FC:Cases Assigned]*[FP:Average Case Work Time - Tech support])+([FC:Chat Interactions Created]*[FP:Average Chat Work Time -Tech Support])`|

|Name|Description|
|----|-----------|
|Service Support: Average Case Work Time|Average time a service support agent worked on a case. Time is measured in hours. The default value is 0.5.|
|Service Support: Average Chat Work Time|Average chat duration a service support agent had for each interaction. Time is measured in hours. The default value is 0.25.|
|Tech Support: Average Case Work Time|Average time a tech support agent worked on a case. Time is measured in hours. The default value is 1.|
|Tech Support: Average Chat Work Time|Average chat duration a tech support agent had for each interaction. Time is measured in hours. The default value is 0.5.|
|Sales Support: Average Chat Work Time|Average chat duration a sales support agent had for each interaction. Time is measured in hours. The default value is 0.5.|

If you create forecast parameters for a forecast configuration, the values set in the configuration are used instead of the default forecast parameters listed in the forecast properties section. For information on configuring forecast parameters, see [Modify forecast parameters to visualize forecast data](../concept/configure-wfo-hr.md#).

|Name|Description|
|----|-----------|
|sn\_agent\_forecast.forecast\_interval|The smallest interval \(in minutes\) at which historical data is collected and forecasts are generated. Valid values are 15 and 60.|
|sn\_agent\_forecast.number\_of\_historical\_days\_in\_timeseries\_chart|The number of historical days that will be plotted in time series chart in Manager Workspace.|

<table id="table_jx5_c3c_3nb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Forecast admin \[sn\_agent\_forecast.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) forecast configuration tables.

</td><td>

-   sn\_agent\_forecast.users
-   clotho\_admin

</td></tr><tr><td>

Forecast user \[sn\_agent\_forecast.user\]

</td><td>

Grants read access to forecast configuration tables.

</td><td>

 

</td></tr></tbody>
</table>|Table|Description|
|-----|-----------|
|Forecast Configuration \[sn\_agent\_forecast\_configuration\]|Define data collection definition and resource conversion formula configurations.|
|Forecast Parameter \[sn\_agent\_forecast\_parameter\]|Define forecast parameters required for the formula.|
|Forecast Configuration group \[sn\_agent\_forecast\_configuration\_m2m\_sys\_user\_group\]|Associate resource conversion formula with assignment groups.|

By default, forecast configurations are available for the following groups:

-   Sales Support
-   Service Support
-   Tech Support

|Name|Description|
|----|-----------|
|Collect daily data for demand forecast data collection definitions|Runs daily at 2 am. For any table defined in the Data Collection Definition configuration, it counts the number of records from the previous day for each hour for every group and stores it in the MetricBase.|
|Forecast resources for future|Runs daily at 3 am. Calculates the forecast resources for the future based on the collected data and stores the data in the Agent Forecast metric in MetricBase.|
|Create cases and chats for previous day|Daily job that creates demo cases and chats for previous day.|
|Delete case demo data​|Deletes cases older than 90 days​. Not enabled by default.|
|Delete interaction demo data|Deletes chats older than 90 days​. Not enabled by default.|

<table id="table_ilq_351_pvb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Collect historical data for demand forecast data collection definitions

</td><td>

Runs on demand. Collects historical data daily for every hour for the past three years for automated forecast configuration.

</td></tr><tr><td>

Generate forecasting demo data

</td><td>

Runs on demand. Collects data for data collection definitions for past 90 days​. Runs Forecast resources for future jobs to generate volume forecasts and staffing plan for next 30 days​. Activates Create cases and chats for previous day job to create cases and chats​.

</td></tr></tbody>
</table>### Teams

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

The maximum number of parent indicators that you can add to one KPI group.-   **Type:**Integer
-   **Default value:**5

</td></tr><tr><td>

sn\_team\_perf.kpi\_group.max\_supporting\_kpis

</td><td>

The maximum number of supporting KPIs you can define for a parent KPI.-   **Type:**Integer
-   **Default value:**10

</td></tr><tr><td>

sn\_team\_perf.ws.max\_assignment\_groups

</td><td>

The maximum number of assignment groups prioritized by order number to display on the Teams application in Manager Workspace.-   **Type:**Integer
-   **Default value:**15

</td></tr><tr><td>

sn\_team\_perf.default\_date\_range

</td><td>

The default date range set in the date range picker.-   **Type:**Integer
-   **Default value:**30

</td></tr></tbody>
</table>### Coaching

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
</table>**Important:** This feature is available with the Workforce Optimization for HR from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](../concept/configure-wfo-hr.md#).

|Business rule|Table|Description|
|-------------|-----|-----------|
|Calculate coaching survey score|Assessment Instance \[asmt\_assessement\_instance\]|Sets the feedback rating based on the survey score.|

|Coaching Opportunity Name|Description|Table|
|-------------------------|-----------|-----|
|Coaching Opportunity for SLA Breach|Coaching opportunity for the agents who worked on the critical and high priority cases that breached SLA.|Task SLA \[task\_sla\]|
|Coaching Opportunity for low CSAT|Coaching Opportunity for the agents who worked on cases that has a customer satisfaction score less than 4.|Case Report \[sn\_customerservice\_case\_report\]|
|Coaching Opportunity for skills award verification|Coaching Opportunity for verification of skills awarded to agents.|Case \[sn\_customerservice\_case\]|
|Knowledge Management Process: Coaching on quality of knowledge articles|Coaching Opportunity for the agents who need to improve the quality of a knowledge article by reviewing the assessment.|Case \[sn\_customerservice\_case\]|
|Coaching Opportunity for high TTR|Coaching Opportunity for the agents who worked on a case that had time to resolution more than 3 days.|Case Report \[sn\_customerservice\_case\_report\]|
|Interaction: Coaching Opportunity for Handling Time|Coaching Opportunity for the agents who worked had handle time more than 10 mins on an interaction.|Interaction \[interaction\]|

**Note:** You can customise the coaching opportunities for low CSAT, high TTR, SLA breach, and handling time based on your business needs.

**Important:** This feature is available with the Workforce Optimization for HR from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](../concept/configure-wfo-hr.md#).

|Name|Description|
|----|-----------|
|Chat Quality Survey|Survey associated with the Chat Interaction coaching opportunity. The coach assess the agent using this survey after the agent completes a chat interaction.|
|Case Quality Survey|Survey associated with the Case Interaction coaching opportunity. The coach assess the agent using this survey after the agent completes a case interaction.|

<table id="table_u2w_jh5_fnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_coaching.learning\_default\_duration

</td><td>

Number of days to read the knowledge article or complete training. The admin \(sn\_wfo.admin\) sets the number of days for the trainee to complete reading the article or complete the training. The number of days is converted to the due date for the trainee to complete the training. It is calculated from the current date taking the trainee's time zone into consideration.-   **Type:**Integer
-   **Default value:**5

</td></tr><tr><td>

sn\_coaching.exclude\_weekends\_on\_training\_due\_date

</td><td>

Excludes weekends when the due date is set for trainees to complete training.-   **Type:**true \| false
-   **Default value:**true

</td></tr></tbody>
</table>### Coaching with Learning

**Important:** This feature is available with the Workforce Optimization for HR from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](../concept/configure-wfo-hr.md#).

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

sn\_lc.content\_reader

</td></tr><tr><td>

Learning content advisor \[sn\_lc.learning\_advisor\]

</td><td>

Can assign learning tasks.

</td><td>

sn\_lc.learning\_advisor

</td></tr><tr><td>

Learning task creator \[sn\_lc.task\_creator\]

</td><td>

Grants read or write access for learning tasks.

</td><td>

sn\_lc.task\_creator

</td></tr></tbody>
</table><table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Learning External Content\[sn\_lc\_external\_content\]

</td><td>

Stores details of external course items that are pulled from third-party systems.

</td></tr><tr><td>

Learning User Course Activity\[sn\_lc\_user\_course\_activity\]

</td><td>

Stores details of learning course activities such as user to whom the course is assigned, status, due date, and name of the learning course.

</td></tr><tr><td>

Learning Content\[sn\_lc\_content\]

</td><td>

Stores details of internal learning content such as knowledge articles, videos that are created in ServiceNow.

</td></tr><tr><td>

Learning Course Item\[sn\_lc\_course\_item\]

</td><td>

Stores details of learning course items, such as the source to which the learning course belongs.

</td></tr><tr><td>

Learning Catalog\[sn\_lc\_catalog\]

</td><td>

Stores details of learning catalog items with its course items.

</td></tr><tr><td>

Learning Task\[sn\_lc\_learning\_task\]

</td><td>

Stores details of learning tasks, such as user to whom the learning task assigned, and due date by when the learning task must be completed.

</td></tr><tr><td>

Learning System Configuration\[sn\_lc\_learning\_system\_configuration\]

</td><td>

Stores configuration parameters of sources \(third-party learning management systems\).

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

Coaching Recommended Trainings is being deprecated and replaced with the Learning Tasks and course items from Coaching with Learning.-   **Type:** string
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

You must [Add this system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to set the desired value.

</td></tr><tr><td>

com.snc.process\_flow.reporting.serialized.val\_size\_limit

</td><td>

Specify the number of bytes allowed for runtime values in each step in the flow execution details. To prevent truncation, set the value to an integer equal to or less than zero.-   **Type:** integer
-   **Default value:** 16384

</td></tr></tbody>
</table>**Important:** This feature is available with the Workforce Optimization for CSM Configurable Workspace \(sn\_csm\_wfo\_workspa\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](https://www.servicenow.com/docs/access?context=request-configurable-wfo-cs&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

### Skill Recommendation

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

Enable this property to start recommending skills for agents.-   **Type:**true \| false
-   **Default value:**true

</td></tr><tr><td>

Maximum number of skills to predict based on supervised learning.

sn\_sre.max\_supervised\_skills

</td><td>

Using supervised learning, the maximum number of skills to predict for each incident ordered by confidence of prediction.-   **Type:**Integer
-   **Default value:**3

</td></tr><tr><td>

Maximum number of skills to predict based on supervised learning.

sn\_sre.max\_unsupervised\_skills

</td><td>

Using unsupervised learning, the maximum number of skills to predict for each incident ordered by confidence of prediction.-   **Type:**Integer
-   **Default value:**3

</td></tr><tr><td>

Number of times Predictive Intelligence must predict the same skill for an agent before recommending it for the agent.

sn\_sre.user\_predicted\_skill\_threshold

</td><td>

The number of times Predictive Intelligence must predict the same skill for an agent before recommending the skill for the agent. -   **Type:**Integer
-   **Default value:**20

</td></tr><tr><td>

Similarity solution definition to recommend skills from similar cases.

sn\_customerservice.unsupervised\_solution\_definition\_for\_cases

</td><td>

Name of the Predictive Intelligence solution definition used for predicting skills to resolve cases using unsupervised learning. If you have created your own solution definition, you can replace the default one with the one you have created.-   **Type:**String
-   **Default value:**ml\_sn\_sn\_customerservice\_global\_recommend\_similar\_skills\_for\_cases

</td></tr><tr><td>

Similarity solution definition to recommend skills for cases.

sn\_customerservice.supervised\_solution\_definition\_for\_cases

</td><td>

Name of the Predictive Intelligence solution definition used for predicting skills to resolve cases using supervised learning. If you have created your own solution definition, you can replace the default one with the one you have created.-   **Type:**String
-   **Default value:**ml\_sn\_sn\_customerservice\_global\_recommend\_skills\_from\_similar\_cases

</td></tr></tbody>
</table>|Scheduled job|Description|
|-------------|-----------|
|Start skill prediction|Runs the job every day at 1 AM on all incidents that were closed the previous day. Recommends the skills used to close the incidents to resolve similar open incidents.|

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
</table>