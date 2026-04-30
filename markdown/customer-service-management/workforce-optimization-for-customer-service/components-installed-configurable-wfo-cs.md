---
title: Components installed with Workforce Optimization for Customer Service
description: Several types of components are installed with activation of the CSM Configurable Workspace \(sn\_csm\_wfo\_workspa\) plugin, including user roles, key performance indicators \(KPIs\), scheduled jobs, properties, and tables.
locale: en-US
release: yokohama
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 25
breadcrumb: [Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Components installed with Workforce Optimization for Customer Service

Several types of components are installed with activation of the CSM Configurable Workspace \(sn\_csm\_wfo\_workspa\) plugin, including user roles, key performance indicators \(KPIs\), scheduled jobs, properties, and tables.

## Workforce Optimization for Customer Service

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

Workforce Optimization Admin \[sn\_wfo.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) additional managers.

</td><td>

sn\_wfo.user

</td></tr><tr><td>

Workforce Optimization CSM Manager \[sn\_csm\_wfo\_workspa.manager\]

</td><td>

Grants rights to create, read, or update, coaching, scheduling, teams, or channel management applications.

</td><td>

-   sn\_mgr\_workspace.manager
-   sn\_customerservice\_manager
-   sn\_wfo.user
-   sn\_channel\_mgmt.user
-   sn\_shift\_planning.admin
-   sn\_coaching.coach
-   sn\_sre.user
-   sn\_team\_perf.team\_performance\_user

</td></tr><tr><td>

Workforce Optimization CSM Admin \[sn\_csm\_wfo\_workspa.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) coaching, scheduling, teams, or channel management applications.

</td><td>

-   sn\_team\_perf.team\_performance\_admin
-   sn\_coaching.admin
-   skill\_model\_admin
-   sn\_channel\_mgmt.admin
-   sn\_csm\_wfo\_workspa.manager
-   sn\_mgr\_workspace.admin
-   sn\_sre.admin

</td></tr></tbody>
</table><table id="table_jg2_3z2_wpb"><thead><tr><th>

Module Name

</th><th>

Module Tables / Database View

</th></tr></thead><tbody><tr><td>

Manager Workspace

</td><td>

Stores filter configurations for all applications such as Channels, Schedule, and Coaching. \[sn\_mgr\_workspace\_filter\_configuration\]

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

</td></tr><tr><td>

Channels

</td><td>

Manager Groups database view \[sn\_wfo\_manager\_groups\]

</td></tr></tbody>
</table>## Manager workspace

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

The maximum limit for the number of users that allows you to swap axes in the skill matrix.-   **Type:** Integer
-   **Default value:** 50

</td></tr></tbody>
</table>|Indicator Name|Description|
|--------------|-----------|
|Total Open Cases|Total number of open that cases are waiting to be worked on by agents. The total count is divided into **New**, **Open** and **Awaiting info** cases.|
|Waiting Work Items|Total count of cases and interaction that are in queue to be assigned to agents.|
|Help Requested|Number of interactions for which agents requested for help.|
|Total Agents|All the agents that you manage. The total count is divided into **Available**, **Break**, **Away** and **Offline** agents.|
|Time-off Requests|Requests made by agents to take time-off from work.|
|Shift Swap Requests|Requests made by agents to swap shifts with other agents.|
|Open Cases|Graphs depicting cases waiting to be worked on, featured by open case type and age.|
|Critical Open Cases​|Number of critical open cases.|

|Indicator Name|Description|
|--------------|-----------|
|No. of cases resolved on first contact|Number cases resolved the first time it was handled.|
|No. of cases not updated in last 30 days|Number of cases that are not updated since 30 days.|
|No. of resolved cases reopened|Number of cases reopened because issues were not addressed properly.|
|No. of escalated open cases|Number of cases that are not worked on and are escalated.|

|Scheduled job|Description|
|-------------|-----------|
|\[CSM Manager Workspace\] Daily Data Collection|Runs the job daily and collects data for all teams indicators.|
|\[CSM Manager Workspace\] Historic Data Collection|Runs the job and collects historic data for all teams indicators.|
|\[CSM Manager Workspace\] Weekly Data Collection|Runs the job weekly and collects data for all indicators in Manager Workspace.|

## Channel management

<table id="table_yny_rvc_llb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Channel Management User \[sn\_channel\_mgmt.user\]

</td><td>

Grants read access to channel reports, channel view, and queue report tables.

</td><td>

awa\_manager

</td></tr><tr><td>

Channel Management Admin \[sn\_channel\_mgmt.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) channel reports, channel view, and queue report tables.

</td><td>

-   sn\_channel\_mgmt.user
-   awa\_admin
-   sn\_wfo.admin
-   report\_admin

</td></tr></tbody>
</table>|Interactive Filter Name|Description|Reference Table|
|-----------------------|-----------|---------------|
|Channel Management Agent Filter|Filters reports based on an agent.|\[sys\_user\]|
|Channel Management Group Filter|Filters reports based on groups.|\[sys\_user\_group\]|
|Channel Management Queues Filter|Filters reports based on queues.|\[awa\_queue\]|
|Channel Management Service Channel Filter|Filters reports based on service channels.|\[awa\_service\_channel\]|

|Report Name|Description|
|-----------|-----------|
|Agents available to take case work items|Number of available agents to take case work items.|
|Interaction Work Items Assigned Today|Number of interaction work items assigned on any given day.|
|Abandoned Interaction Work Items|Number of abandoned interaction work items.|
|Case Work Items Assigned Today|Number of case work items assigned on any given day.|
|Average CSAT Score|Average customer satisfaction score.|
|Case Work Items Resolved Today|Number of case work items resolved on any given day.|
|Interaction Work Items Resolved Today|Number of interaction work items resolved on any given day.|
|Average Handling time for Interaction Work Items|Average time for handling interaction work items.|
|Agents Available to take Interaction Work Items|Number of available agents to take interaction work items.|
|Case Work Items Closed Today|Number of case work items closed on any given day.|

|Report Name|Description|
|-----------|-----------|
|Active Chats|Number of ongoing chat conversations.|
|Chats Completed Today|Number of chats completed on any given day.|
|Chat Rejections Today|Number of chats rejected on any given day.|
|Active Cases|Number of ongoing cases.|
|Cases Resolved Today|Number of resolved cases on any given day.|

|Report Name|Description|
|-----------|-----------|
|Active Calls|Number of ongoing calls between customers and agents.|
|Agents Available|Number of agents online.|
|Abandoned Calls|Number of calls that the agents were not able to attend on any given day.|
|Handled Calls Today|Number of calls attended by the agents on any given day.|
|Average Wait Time|Average amount of time in minutes that the customers needed to wait before talking to an agent.|
|Contacts in ACW State|Number of customer calls in which the agent must take some action after the call is over.|
|Oldest Contact Age|Call during which the customer had to wait the longest before speaking to an agent.|
|Average Abundant Time \(seconds\)|Average time before the customer disconnects the call after waiting for the agent to respond.|
|Average Handling Time Today|The average duration, from beginning to end, that a contact is engaged with an agent. This metric includes talk time, hold time, and the time spent on After Contact Work \(ACW\).|
|Average Wait Time Today|The average duration \(seconds\) that a contact remains in the queue before being attended to by an agent.|
|Max Queued Time Today|The longest time a contact waits in the queue. This includes all contacts added to the queue, even those that didn’t connect with an agent.|
|Average Hold Time Today|The average duration \(seconds\) that a contact spends on hold while waiting in the queue.|
|Average Interaction Time Today|The average time \(seconds\) that contacts are actively engaged and interacting with agents. This does not include the time spent waiting in the queue.|
|Average Wrap Up Duration Today|The average duration \(seconds\) that agents spend in the After Contact Work \(ACW\) state, within the specified time range.|

|Scheduled job|Description|
|-------------|-----------|
|\[Channel Management\] Reset Temporary Capacity Override|Runs the job every two minutes check the invalid or expired overridden capacity and resets to the previous channel capacity.|

<table id="table_dqp_rw2_nlb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_channel\_mgmt.list\_auto\_refresh.enable

</td><td>

Select to disable auto-refresh of lists in Channel Management.-   **Type**: True or False
-   **Default value**: True

</td></tr><tr><td>

sn\_channel\_mgmt.channels\_card\_auto\_refresh.enable

</td><td>

Select to disable auto-refresh of lists in Channel Management.-   **Type**: True or False
-   **Default value**: True

</td></tr><tr><td>

sn\_channel\_mgmt.list\_auto\_refresh.interval.seconds

</td><td>

Defines the auto-refresh interval for the channel management list.-   **Type**: Integer
-   **Default value**: 30

</td></tr><tr><td>

sn\_channel\_mgmt.kpi\_auto\_refresh.interval.seconds

</td><td>

Set the frequency for refreshing data on channel management indicators.-   **Type**: Integer
-   **Default value**: 5

</td></tr><tr><td>

sn\_channel\_mgmt.channel\_card\_auto\_refresh.interval.seconds

</td><td>

Defines the auto-refresh interval for the cards on channel management overview container.-   **Type**: Integer
-   **Default value**: 120

</td></tr><tr><td>

sn\_channel\_mgmt.filter\_config.enable

</td><td>

Displays **Assignment Group** interactive filter in channels.-   **Type**: True or False
-   **Default value**: True

</td></tr><tr><td>

sn\_channel\_mgmt.awa\_agent\_temporary\_override\_time.minutes

</td><td>

Duration for the channel capacity that is overridden.-   **Type**: Integer
-   **Default value**: 12 hours

</td></tr></tbody>
</table>**Note:** Channel management properties are not visible by default in the \[sys\_properties\] table. To use any of the channel management properties, you must add the required property to the System Property \[sys\_properties\] table. For more information, refer to [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

## Scheduling

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

None

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
-   **Default value:** True

</td></tr><tr><td>

sn\_shift\_planning.early\_clockin\_threshold

</td><td>

Threshold settings indicate how many minutes early or late an agent can clock-in or clock-out to the scheduled time without being considered non-adherent. This is the acceptable duration of time flexibility for an agent to start work before the scheduled start time. -   **Type:** Integer
-   **Default value:** 60 min

</td></tr><tr><td>

sn\_shift\_planning.adherence\_threshold

</td><td>

Set the percentage for a threshold in adherence. The agents who do not qualify to be above the defined threshold value \(70%\) are considered non-adherent agents. -   **Type:** Integer
-   **Default value:** 70%

</td></tr><tr><td>

sn\_shift\_planning.conformance\_lower\_threshold

</td><td>

Set the lower threshold percentage for flexibility in conformance. The agents who don’t qualify for the defined lower and upper conformance threshold values \(80-120\) are considered non-conformance agents. -   **Type:** Integer
-   **Default value:** 80%

</td></tr><tr><td>

sn\_shift\_planning.conformance\_upper\_threshold

</td><td>

Set the upper threshold percentage for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered non-conformance agents.-   **Type:** Integer
-   **Default value:** 120%

</td></tr><tr><td>

sn\_shift\_planning.auto\_clockout\_threshold

</td><td>

Threshold time for the system to wait and generate automatic clock-out events when agents forgets to clock-out. For example, if an agent's planned work shift is 8 AM to 5 PM and fails to clock out at 5 PM, the system waits for 60 min as threshold time and generates an automatic clock-out event. -   **Type:** Integer
-   **Default value:** 60 min

</td></tr><tr><td>

sn\_shift\_planning.display\_shift\_name

</td><td>

Set this property to true to display the shift name. If the value is false, event type will be displayed.-   **Type:** Boolean
-   **Default value:** True

**Note:** If you change the value of this property, the changes are effective after 24 hours. To view the changes immediately, run the **Shift Planning - Delete All Agent Schedules Cache** scheduled job.

</td></tr></tbody>
</table>|Business rule|Table|Description|
|-------------|-----|-----------|
|Agent Time Work Event Trigger|Agent Presence \[awa\_agent\_presence\]|Sets the clock-in and clock-out events whenever there is a change in agent's presence state.|

<table id="table_vxk_ndy_pnb"><thead><tr><th>

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

Generates clock-out events every 4 hours if agents haven't clocked-out. **Note:** Consider an agent's work shift timings are from 8 AM to 5 PM and **sn\_shift\_planning.auto\_clockout\_threshold** property value is set to 60 minutes. The agent clocks-in and fails to clock out, the scheduled job waits until 6 PM\(5 PM+60 minutes\) and if there’s no clock out until 6 PM, the system generates a clock-out event with agent's shift end time.

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
</table>**Setting the due date for time-off and shift-swap request approvals**: Administrators can configure the due date logic for the Time Off Request and Shift Swap Request approval flows. The approval due date is set as the number of days before the request start date. The default is set to two days which means if the approval is not approved two days before the request start date, it will be auto-rejected. For information on configuring flows, refer to [Build your first flow in Flow Designer](https://www.servicenow.com/docs/access?context=build-your-first-flow&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Demand Forecast

|Name|Description|
|----|-----------|
|Cases Assigned|Collects data for cases.|
|Chat Interactions Created|Collects data for chat interactions.|

The **WFO Forecast** time series metric retention policy is available by default for all forecast configurations. By default, this retention policy stores data at a 15min interval for the past three years for all zBoot customers.

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

If you create forecast parameters for a forecast configuration, the values set in the configuration are used instead of the default forecast parameters listed in the forecast properties section. For information on configuring forecast parameters, see [Modify forecast parameters to visualize forecast data](../task/modify-demand-forecast-parameters-configurable-wfo.md).

|Name|Description|
|----|-----------|
|sn\_agent\_forecast.forecast\_interval|The smallest interval \(in minutes\) at which historical data is collected and forecasts are generated. Valid values are 15 and 60.|
|sn\_agent\_forecast.number\_of\_historical\_days\_in\_timeseries\_chart|The number of historical days that will be plotted in time series chart for 15-, 30-, and 60-minute intervals in Manager Workspace.|
|sn\_agent\_forecast.number\_of\_historical\_days\_in\_daily\_timeseries\_chart|The number of historical days that will be plotted in time series chart for daily interval in Manager Workspace.|

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
|Collect daily data for demand forecast data collection definitions|Runs daily at 2 am. For any table defined in the Data Collection Definition configuration, it counts the number of records from the previous day at 15-minute interval for every group and stores it in the MetricBase. Data collected at 15-minute interval is also aggregated at daily interval and stored in the MetricBase.|
|Forecast resources for future|Runs daily at 3 am. Calculates the forecast resources for the future based on the collected data and stores the data in the Agent Forecast metric in MetricBase.|
|Create cases and chats for previous day|Daily job that creates demo cases and chats for previous day.|
|Delete case demo data​|Deletes cases older than 90 days​. Not enabled by default.|
|Delete interaction demo data|Deletes chats older than 90 days​. Not enabled by default.|

| | |
|---|---|
|Collect historical data for demand forecast data collection definitions|Runs on demand. Collects historical data daily for 15-minute interval and aggregates the data at daily interval for 1098 days \(past three years\) and stores it in the MetricBase. Once the job is executed, the **Daily Historical data duration** column displays the number of days for which historical data has been collected for daily interval. The **Duration** column displays the number of days for which historical data has been collected for 15-minute interval. Both the columns are associated with the Forecast Configuration \[sn\_agent\_forecast\_configuration\] table.|
|Generate forecasting demo data|Runs on demand. Collects data for data collection definitions for past 90 days​. Runs Forecast resources for future jobs to generate volume forecasts and staffing plan for next 30 days​. Activates Create cases and chats for previous day job to create cases and chats​.|

## Teams

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
</table>|Indicator Name|Description|
|--------------|-----------|
|\# of cases resolved on first contact|Number of cases resolved on first contact.|
|\# of P1 cases resolved on first contact|Number of P1 cases resolved on first contact.|
|\# of P2 cases resolved on first contact|Number of P2 cases resolved on first contact.|
|\# of P3 cases resolved on first contact|Number of P3 cases resolved on first contact.|
|\# of P4 cases resolved on first contact|Number of P4 cases resolved on first contact.|
|MTTR for Cases|Mean time to resolve the cases.|
|MTTR for P1 Cases|Mean time to resolve the P1 cases.|
|MTTR for P2 Cases|Mean time to resolve P2 cases.|
|MTTR for P3 Cases|Mean time to resolve the P3 cases.|
|MTTR for P4 Cases|Mean time to resolve P4 cases.|
|CSAT for Cases|Customer satisfaction score for cases.|
|CSAT for P1 Cases|Customer satisfaction score for P1 cases.|
|CSAT for P2 Cases|Customer satisfaction score for P2 cases.|
|CSAT for P3 Cases|Customer satisfaction score for P3 cases.|
|CSAT for P4 Cases|Customer satisfaction score for P4 cases.|
|Number of Closed Cases|Number of closed cases.|
|Number of Closed P1 Cases|Number of closed P1 cases.|
|Number of Closed P2 Cases|Number of closed P2 cases.|
|Number of Closed P3 Cases|Number of closed P3 cases.|
|Number of Closed P4 Cases|Number of closed P4 cases;|
|Average Wait Time for Chats|Average waiting time for chats.|
|Number of Chats Handled|Number of chats handled.|
|Average Handling Time for Chats|Average handling time for chats.|
|Number of Abandoned Chats|Number of abandoned chats.|
|Number of Incoming Cases|Number of incoming cases.|
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
</table>**Important:** This feature is available with the Workforce Optimization for CSM Configurable Workspace \(sn\_csm\_wfo\_workspa\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](../task/request-configurable-wfo-cs.md).

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

**Note:** You can customize the coaching opportunities for low CSAT, high TTR, SLA breach, and handling time based on your business needs.

**Important:** This feature is available with the Workforce Optimization for CSM Configurable Workspace \(sn\_csm\_wfo\_workspa\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](../task/request-configurable-wfo-cs.md).

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
</table>## Coaching with Learning

**Important:** This feature is available with the Workforce Optimization for CSM Configurable Workspace \(sn\_csm\_wfo\_workspa\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](../task/request-configurable-wfo-cs.md).

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

 

</td></tr><tr><td>

Learning content advisor \[sn\_lc.learning\_advisor\]

</td><td>

Can assign learning tasks.

</td><td>

 

</td></tr><tr><td>

Learning task creator \[sn\_lc.task\_creator\]

</td><td>

Grants read or write access for learning tasks.

</td><td>

 

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

You must [Add this system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to set the desired value.

When you [synchronize](../task/integrate-learning-third-party-configurable-wfo-cs.md) third-party learning content with your ServiceNow instance, if the word count of the content being pulled into your instance exceeds the value set for this property, the synchronization fails.

</td></tr><tr><td>

com.snc.process\_flow.reporting.serialized.val\_size\_limit

</td><td>

Specify the number of bytes allowed for runtime values in each step in the flow execution details. To prevent truncation, set the value to an integer equal to or less than zero.-   **Type:** integer
-   **Default value:** 16384

 **Note:** When you [synchronize](../task/integrate-learning-third-party-configurable-wfo-cs.md) third-party learning content with your ServiceNow instance, if the word count of the content being pulled into your instance exceeds the value set for this property, the synchronization fails.

</td></tr></tbody>
</table>**Important:** This feature is available with the Workforce Optimization for CSM Configurable Workspace \(sn\_csm\_wfo\_workspa\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for CS configurable workspace](../task/request-configurable-wfo-cs.md).

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
</table>**Parent Topic:**[Configuring Workforce Optimization for Customer Service](../concept/setup-configurable-wfo-cs.md)

