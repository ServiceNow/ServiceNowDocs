---
title: Configuring Workforce Optimization for HR
description: Enable Workforce Optimization for HR and configure settings to use Scheduling, Teams, and Coaching applications.Workforce Optimization for HR solution is highly modular, offering a wide range of capabilities such as Scheduling, Coaching, and Teams applications in Manager Workspace. Configurable Workspace \(sn\_hr\_wfo\_workspa\) plugin activates all other dependent plugins to enable users to access Scheduling, Coaching, and Teams applications in Workforce Optimization for HR.After you install or upgrade to the latest Workforce Optimization for HR from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages.If any conrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file. In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conref at the end that describes domain separation.Domain separation is supported for Workforce Optimization for HR. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.Manage events the team calendar. Create schedule plans, shift plans, event categories, and event types.Add event categories and create or update field configurations for events in the Manager workspace.Create multiple events and add them to the team calendar.Configure schedule adherence properties to calculate the adherence to improve the operational efficiency of your organization.Configure and tweak the schedule adherence and conformance formulas using scripted extension points to customize them for your organization.Use extension points to call scripts for event categories such as meeting, time off, or work time.Organize your teams into assignment groups and create reports for those groups to can gain visibility into the team's performance.Create key performance indicator \(KPI\) groups with the KPIs that matter most to your teams. When you associate your KPI groups with assignment groups, you can monitor your team's performance.Add managers to a KPI assignment group.Manage agent skills and assess the quality of completed tasks. Use predictive intelligence to recommend skills for agents. Train your agents with internal and external learning content.Add a system property to display the desired indicator in the Coaching Overview tab in the Coaching application.Collect skill data based on skills agents have used for case resolution. Use supervised learning to recommend these skills for agents to resolve similar open case. You can also find patterns in how skills are used for case resolution and use unsupervised learning to recommend skills for agents.Use scripted extension points to customize skill prediction for tasks.Add list or list categories to modify the list menu for Coaching with Learning in the Coaching application in Workforce Optimization for HR.Configure the data you want to collect, modify forecast parameters and calibrate manual adjustments using Demand Forecast.Define the data you want to collect for cases, interactions, or any table to forecast the number of agents that you require for your staffing needs.Add parameters to be defined in the formula to calculate agent count per hour in a day.Configure the resource conversion formula.Associate an assignment group with a Resource Conversion Formula. You can assign a forecast configuration to multiple assignment groups, but an assignment group can have only one forecast configuration.Configure and tweak forecast parameters to see how the forecast behaves when you vary the period length, periods to forecast, or algorithm. You can view the modified forecast on the time-series visualization.Adjust forecasts manually to fine-tune them for greater accuracy. Create the adjustment for a specified time period and analyze how it impacts your forecast.
locale: en-US
release: xanadu
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 25
breadcrumb: [Workforce Optimization for HR Overview, HR Service Delivery, Employee Service Management]
---

# Configuring Workforce Optimization for HR

Enable Workforce Optimization for HR and configure settings to use Scheduling, Teams, and Coaching applications.

## Activate Workforce Optimization for HR

Workforce Optimization for HR solution is highly modular, offering a wide range of capabilities such as Scheduling, Coaching, and Teams applications in Manager Workspace. Configurable Workspace \(sn\_hr\_wfo\_workspa\) plugin activates all other dependent plugins to enable users to access Scheduling, Coaching, and Teams applications in Workforce Optimization for HR.

### Before you begin

Role required: sn\_hr\_wfo.admin

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its nae or ID/ If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install**, and then in the Activate Plugin dialog box, select **Activate**.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears:`Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>`


### RCA approvals in Workforce Optimization for HR

After you install or upgrade to the latest Workforce Optimization for HR from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages.

#### Before you begin

Role required: sn\_hr\_wfo.admin

#### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Right-click the header and choose **Import XML**.

3.  Click **Choose file** and select the XML file that you downloaded.

4.  Search and find the HR Agent WS bulk RCAs approval script record.

5.  Click **Run Script** to approve all the requested RCAs.

    **Note:** RCA fix script can approve the RCAs which exist at the time of execution. After running the RCA script \(if you install the Document Templates from ServiceNow Store, Human Resources Scoped App: Lifecycle Events, and Human Resources Scoped App: Employee Relations plugins\), re-run the RCA script to approve the new RCAs.


## Workforce Optimization for HR Domain Separation

Domain separation is supported for Workforce Optimization for HR. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

### Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

### Workforce Optimization for Customer Service overview

The goal of Workforce Optimization for Customer Service is to simplify the daily routine of HR Agent Managers to develop high-performing teams by optimizing schedules and work assignments, respond to ad hoc changes in real time, manage time-off requests and providing the skills they need to succeed—all in one workspace .

### How domain separation works in Workforce Optimization for HR

Domain separation is supported.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

## Setting up Scheduling for Workforce Optimization for HR

Manage events the team calendar. Create schedule plans, shift plans, event categories, and event types.

### Configure event categories

Add event categories and create or update field configurations for events in the Manager workspace.

#### Before you begin

Role required: sn\_hr\_wfo.admin

The following event category configurations are available by default:

-   Actual Work
-   Break
-   Meeting
-   On-Call
-   On-Call Time Off
-   Time Off
-   Training
-   Work

#### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for HR** &gt; **Scheduling** &gt; **Event Categories**.

2.  In the **Event Categories** list, click **New**.

3.  In the **Name** field, enter a name for the event category.

4.  If you want to exclude this event category for agent coverage calculation, enable the **Exclude from coverage** check box.

5.  In the **Event field configuration** dialog box, edit the following configuration as necessary:

    **Note:** You can remove any property that does not apply to a type of event.

    ```
    {
                "create": {                //Creates an event type form
                    "attendees": {         //Adds the Attendees field       
                    "mandatory": true,     //Sets this field as mandatory
                    "readOnly": false,     //Sets this field as read-only
                    "allowAllUsers": false //Allows you to only add users managed by the logged-in user; to add any user, set this value to true
                    },
                    "startDate": {    
                    "mandatory": true,
                    "readOnly": false
                    },
                    "endDate": {
                    "mandatory": true,
                    "readOnly": false
                    },
                    "additionalSelectors": [    //Add custom fields to the form
                    {
                        "fieldLabel": "Select Shift", //Name of the field that displays on the form
                        "table": "sn_shift_planning_shift_plan", //Name of the table referenced by the field
                        "field": "name", //Any field from the selected table whose display values must be shown in the custom field
                        "value": "",
                        "mandatory": true,
                        "additionalQueryString": ""
                    }
                    ]
                },
                "edit": {                    //Edit an event type form
                    "attendees": {
                    "mandatory": true,
                    "readOnly": false,
                    "allowAllUsers": false
                    },
                    "startDate": {
                    "mandatory": true,
                    "readOnly": false
                    },
                    "endDate": {
                    "mandatory": true,
                    "readOnly": false
                    },
                    "additionalSelectors": [
                    {
                        "fieldLabel": "Select Shift",
                        "table": "sn_shift_planning_shift_plan",
                        "field": "name",
                        "value": "",
                        "mandatory": true,
                        "additionalQueryString": ""
                    }
                    ]
                }
            }
    ```

6.  Click **Submit**.


### Create event types

Create multiple events and add them to the team calendar.

#### Before you begin

Role required: sn\_hr\_wfo.admin

#### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for HR** &gt; **Scheduling** &gt; **Event Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the event type.|
    |Category|Type of event, for example, meeting, break, or time off.|
    |Priority Order|Priority of the event type that you want to exclude from the coverage. The higher the number means the higher the priority.|
    |Color|Color that identifies this type of event in the team calendar.|

4.  Click **Submit**.


### Configure schedule adherence properties

Configure schedule adherence properties to calculate the adherence to improve the operational efficiency of your organization.

#### Before you begin

Role required: sn\_hr\_wfo.admin

#### About this task

The threshold settings for adherence and conformance indicate how many minutes early or late an agent can clock in or clock out to a scheduled work shift without being considered as non-adherent.

#### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for HR** &gt; **Schedule Adherence** &gt; **Settings**

2.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Enable Schedule Adherence|Calculation and information about the agents' adherence to the schedules.|
    |Threshold for early checkin for planned shift \(in Minutes\)|Time set early check in. This time is the acceptable time for an agent to start the work shift before the actual shift time. The default value is 60 minutes. For example, if an agent's planned work shift is 8 a.m. to 5 p.m., and the agent clocks in at 7 a.m., the threshold time allows flexibility and the agent is not considered as a non-adherent agent.|
    |Threshold for adherence% of Time Worked Summary|Percentage set for a threshold in adherence. The agents who do not qualify to be above the defined threshold value \(70%\) are considered non-adherent agents.|
    |Lower threshold conformance % of Time Worked Summary|Lower threshold percentage set for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered as non-conformant agents. The default value is 80%.|
    |Upper threshold for conformance % of Time Worked Summary|Upper threshold percentage set for flexibility in conformance. The agents who do not qualify for the defined lower and upper conformance threshold values \(80-120\) are considered as non-conformant agents. The default value is 120%.|
    |Default threshold time for clock-out event generation \(in Minutes\)|Default threshold time to generate an automatic clock-out event if an agent fails to clock out. The default value is 60 minutes. For example, if an agent's planned work shift is 8 a.m. to 5 p.m. and the agent fails to clock out at 5 p.m., the system waits for 60 minutes as the threshold time and generates an automatic clock-out event.|

3.  Click **Save**.


### Modify schedule adherence and conformance formulas by using extension points

Configure and tweak the schedule adherence and conformance formulas using scripted extension points to customize them for your organization.

#### Before you begin

Role required: sn\_hr\_wfo.admin

#### About this task

Use the `sn_shift_planning.ScheduleAdherenceExtPt` extension point and create an implementation to configure the formulas. You can create multiple implementations. However, the implementation with the lowest order number is executed.

#### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for `sn_shift_planning.ScheduleAdherenceExtPt`.

3.  On the form banner, click the link **here** to edit the record.

4.  To create your extension point script, click **Create Implementation** in the related links.

5.  Modify the formulas for calculating the schedule adherence and conformance in the `getAdherencePercentage` and `getConformancePercentage` methods.

    ![Extension Script for Schedule Adherence.](../image/extension-script-adherence-wfo-hr.jpg)

6.  Click **Update**.


#### Result

The schedule adherence and conformance calculations are based on the formulas in the implementation.

### Event type extension points in Workforce Optimization for HR

Use extension points to call scripts for event categories such as meeting, time off, or work time.

To see a list of extension points that you can use for Workforce Optimization for HR, navigate to **System Extension Points** &gt; **Scripted Extension Points**. In the Extension Points list, open the sn\_shift\_planning.EventManagerextension point.

Use scripted extension points to integrate customizations without altering the core components in the application code. When customizing a base application, you implement the scripted extension points by creating the custom script includes and registering them against the scripted extension points.

|Extension points|Description|
|----------------|-----------|
|sn\_shift\_planning.EventManager|Implement this extension point to customize the logic for the event categories that you create.|

You can use extension points to create events such as meeting, training, and time-off requests. For example extension point implementations, see the following extension instances in the Implementations related list:

|Category|Extension Script|
|--------|----------------|
|Meeting|AgentScheduleMeetingEventManager|
|Break|AgentScheduleBreakEventManager|
|Training|AgentScheduleTrainingEventManager|
|Time off|AgentScheduleTimeOffEventManager|
|Work|AgentScheduleWorkEventManager|
|On call|AgentScheduleOnCallEventManager|
|On Call Time Off|AgentScheduleOnCallTimeOffEventManager|
|Actual Work|AgentScheduleActualWorkEventManager|

## Setting up Teams in Workforce Optimization for HR

Organize your teams into assignment groups and create reports for those groups to can gain visibility into the team's performance.

As an administrator, you can configure KPIs as well as child KPIs. The child KPIs appear when you drill-down into top level KPIs. For example, Closed Cases KPI has P1 Cases, P2 Cases as child KPIs.

### Create KPI Groups to monitor performance

Create key performance indicator \(KPI\) groups with the KPIs that matter most to your teams. When you associate your KPI groups with assignment groups, you can monitor your team's performance.

#### Before you begin

Role required: sn\_hr\_wfo.admin

#### Procedure

1.  Create a KPI group.

    1.  Navigate to **Workforce Optimization for HR** &gt; **Team Performance** &gt; **KPI Groups**.
    2.  Click **New**.
    3.  In the **Name** field, enter a name for the KPI group.
    4.  In the **Type** menu, select **Teams**.
    5.  Right-click the form header and click **Save**.

        You can add up to five KPIs to a KPI group.

2.  Add KPIs to a KPI group.

    1.  In the **KPIs** related list, click **New**.
    2.  In the **KPI** field, select the KPI to apply for this group.
    3.  Click **Submit**.
3.  Add KPI assignment groups to the KPI group.

    **Note:**

    -   You can associate a KPI assignment group only to one KPI type.
    -   You can add additional managers to each assignment group.
    -   You can associate a user with a KPI group as the primary assignment group for that user.
    1.  In the **Assignment Groups** tab, click **Edit**.
    2.  Move the desired assignment groups from the Collection to the Assignment Groups list.
    3.  Click **Save**.

### Add managers to a KPI assignment group

Add managers to a KPI assignment group.

#### Before you begin

Role required: sn\_hr\_wfo.admin

#### About this task

You can associate a user with a primary assignment group by selecting the group in the [user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

#### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for HR** &gt; **Team Performance** &gt; **Additional Managers**.

2.  Click **New**.

3.  In the **Assignment Group** field, select an assignment group.

4.  In the **Manager** field, select a manager you want to add for this assignment group.

5.  Click **Submit**.


## Setting up Coaching in Workforce Optimization for HR

Manage agent skills and assess the quality of completed tasks. Use predictive intelligence to recommend skills for agents. Train your agents with internal and external learning content.

### Configure an indicator to display in the Coaching Overview tab in Workforce Optimization for HR

Add a system property to display the desired indicator in the Coaching Overview tab in the Coaching application.

#### Before you begin

**Important:** This feature is available with the Workforce Optimization for HR from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for HR](configure-wfo-hr.md#).

Set the map application scope to **Coaching**. For information on how to set the scope, see [Set map application scope](https://www.servicenow.com/docs/access?context=set-map-application-scope&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Role required: sn\_hr\_wfo.admin

#### About this task

Replace the existing indicator with any Performance Analytics indicator that has the Assigned to and Assignment group breakdowns to display in the Coaching Overview tab in the Coaching application.

#### Procedure

1.  In the application navigator, enter `sys_properties.list`.

2.  Click **New**.

3.  Enter the following field values.

<table id="table_yfh_h3p_f4b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

sn\_coaching.coaching\_overview\_default\_quality\_indicator

</td></tr><tr><td>

Application

</td><td>

Coaching

</td></tr><tr><td>

Type

</td><td>

string

</td></tr><tr><td>

Value

</td><td>

\{"title": "&lt;name&gt;", "sys\_id": "&lt;sys id&gt;"\}where &lt;name&gt; is the name of the indicator that you want to display in the Coaching Overview tab and &lt;sys id&gt; is the [unique record identifier](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)Example:

-   Name: % of P1 incidents resolved on first call.
-   Sys ID: 0423e59387401010ca99e12397cb0bbb
\{"title": "% of P1 incidents resolved on first call", "sys\_id": "0423e59387401010ca99e12397cb0bbb"\}

</td></tr><tr><td>

Read roles

</td><td>

sn\_coaching.coach

</td></tr></tbody>
</table>4.  Click **Submit**.

    The configured indicator replaces the existing indicator in the Overview tab in the Coaching application in Workforce Optimization for HR.


### Setting up skill prediction in Workforce Optimization for HR

Collect skill data based on skills agents have used for case resolution. Use supervised learning to recommend these skills for agents to resolve similar open case. You can also find patterns in how skills are used for case resolution and use unsupervised learning to recommend skills for agents.

#### Before you begin

Set up skills. For more information, see [Skills Management](https://www.servicenow.com/docs/access?context=skills-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

Predictive Intelligence must be set up and configured on your instance to train the models. For more information, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

Activate the Skill Recommendation application plugin \(com.snc.sre\) to use predictive intelligence for recommending skills.

Role required: sn\_hr\_wfo.admin

#### Procedure

1.  Configure the skill prediction property.

2.  Run the solution definition models such as **Recommend similar skills for cases** or **Recommend skills from similar cases** to train the supervised and unsupervised solutions.

    For more information on training a solution, refer to [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

3.  Run the **Start skill prediction** scheduled job everyday to start predicting skills for cases or agents.

    This scheduled job is inactive by default. When you activate it, the job runs daily at 1:00 AM on all cases resolved the previous day. The job then adds the skills to the User Predicted Skill \[sn\_sre\_user\_predicted\_skill\] table and Task Predicted Skill \[sn\_sre\_task\_predicted\_skill\] table.

    **Note:** Recommended skills will start appearing once the number of records in \[sn\_sre\_task\_predicted\_skill\] table exceeds the value defined in the \[sn\_sre.user\_predicted\_skill\_threshold\] .


#### Use extension points for skill prediction in Workforce Optimization for HR

Use scripted extension points to customize skill prediction for tasks.

##### Before you begin

The Skill Recommendation extension point is included with the Skill Recommendation \(com.snc.sre\) plugin.

Role required: sn\_hr\_wfo.admin

##### About this task

You can create multiple implementations for each extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed.

##### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Client Extension Points**.

2.  From the Extension Points list, select **Skill Recommendation** \(sn\_sre.SkillPredictionAPI\).

3.  Do one of the following:

    -   To create a new skill recommendation implementation, click **Create Implementation**.
    -   To modify an existing implementation, from the **Implementations** related list, select a class.
4.  Modify the script as required.

5.  Click **Update**.


### Configure a list menu to display in the Learning tab in Workforce Optimization for HR

Add list or list categories to modify the list menu for Coaching with Learning in the Coaching application in Workforce Optimization for HR.

#### Before you begin

**Important:** This feature is available with the Workforce Optimization for HR Configurable Workspace from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for HR](configure-wfo-hr.md#).

Set the map application scope to **Coaching With Learning**. For information on how to set the scope, see [Set map application scope](https://www.servicenow.com/docs/access?context=set-map-application-scope&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Role required: sn\_hr\_wfo.admin

#### Procedure

1.  In the application navigator, enter `sys_ux_list_menu_config.list`.

2.  Click **Learning list** record.

3.  Under UX list category, click **New**.

4.  On the form, fill in the fields:

    |Field|Value|
    |-----|-----|
    |Title|Enter the name of the list category.|
    |Description|Enter a short description about the list category.|
    |Order|Enter a value to set the position of the list category in the current list.|
    |Active|Select the check box to make the list category visible.|

5.  Click **Submit**.

6.  Under UX Lists, click **New** to create lists under that list category.

7.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |Title|Enter the name of the list.|
    |Table|Select the table for the data that you want to display in the list.|
    |Configuration|Select **Learning List**.|
    |Columns|Select the columns that you want to display for the table.|

8.  Click **Submit**.

9.  Click **Update**.


## Setting up Demand Forecast in Workforce Optimization for HR

Configure the data you want to collect, modify forecast parameters and calibrate manual adjustments using Demand Forecast.

### Configure data collection for Demand Forecast

Define the data you want to collect for cases, interactions, or any table to forecast the number of agents that you require for your staffing needs.

#### Before you begin

You must have the MetricBase plugin \[com.snc.clotho\] enabled to use Demand Forecast in Workforce Optimization for HR. For more information, see [Requesting the MetricBase product](https://www.servicenow.com/docs/access?context=request-metricbase&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

Role required: sn\_hr\_wfo.admin

#### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for HR** &gt; **Demand Forecast**.

2.  Define the data you want to collect for forecasting agents to resolve cases.

    1.  Click **Data Collection Definitions**.

        See the [Components installed with Workforce Optimization for HR](../reference/wfo-hr-reference.md#) for the list of configurations that are available by default.

    2.  Click **New**.
    3.  On the form, fill in the fields:

        |Field|Description|
        |-----|-----------|
        |Name|Name for the collection forecast configuration.|
        |Table|Table that is used for collecting data.|
        |Type|Data Collection Definition type is set to **Collection** by default and collects data using a scheduled job.|
        |Date Field|Data that you can add to forecast for the future.|
        |Conditions|Conditions that you can set so that you can capture the data that you need.|

    4.  Click **Submit**.
    5.  Create an index for the table you have created using the date field and the conditions you have added to the table. For information on creating a table index, see [Create a table index](https://www.servicenow.com/docs/access?context=t_CreateCustomIndex&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

#### Add parameters to be defined in the formula

Add parameters to be defined in the formula to calculate agent count per hour in a day.

##### Before you begin

Role required: admin

##### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for HR** &gt; **Demand Forecast** &gt; **Formula Parameters**.

2.  In the **Name** field, enter a name for the parameter.

3.  Do one of the following:

    -   If you need to add a value to be calculated for the formula, in the **Value** field, enter a value.
    -   If you want to use the performance analytics score card API or a custom API, select **Advanced**, and add a script.
    The Average Case Work Time and Average Chat Work Time forecast parameters provided by default are examples of how you can use scripts to add the parameters. For a list of parameters provided by default, see [Components installed with Workforce Optimization for HR](../reference/wfo-hr-reference.md#).

4.  Click **Submit**.


#### Configure resource conversion formula

Configure the resource conversion formula.

##### Before you begin

Role required: sn\_hr\_wfo.admin

##### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for HR** &gt; **Demand Forecast** &gt; **Resource conversion formula**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_t2w_wsr_dmc"><thead><tr><th>

Field

</th><th>

Instructions

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the resource forecast configuration.

</td></tr><tr><td>

Type

</td><td>

Type is set to **Resource Conversion Formula**.

</td></tr><tr><td>

Formula

</td><td>

Formula to calculate the forecasted number of agents that you need.In the Related Links section, do the following:

 -   Click **Browse Forecast Configuration**, select the forecast configuration to add to the formula and click **Add**.
-   Click the Browse Forecast Parameter, select the forecast parameter to add to the formula and click **Add**.

**Note:** **FC** refers to Forecast Configuration and **FP** refers to Forecast Parameter.

</td></tr></tbody>
</table>4.  Click **Submit**.


#### Group forecast configuration

Associate an assignment group with a Resource Conversion Formula. You can assign a forecast configuration to multiple assignment groups, but an assignment group can have only one forecast configuration.

##### Before you begin

Role required: admin

##### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for HR** &gt; **Demand Forecast** &gt; **Group Forecast Configuration**.

2.  Click **New** and fill in the fields on the group forecast configuration form.

    -   In the **Assignment Group** field, browse and select the group to which you want to associate a forecast configuration.
    -   In the **Forecast Configuration** field, browse and select a **Resource Conversion Formula**.

### Modify forecast parameters to visualize forecast data

Configure and tweak forecast parameters to see how the forecast behaves when you vary the period length, periods to forecast, or algorithm. You can view the modified forecast on the time-series visualization.

#### Before you begin

Role required: sn\_hr\_wfo.admin, sn\_hr\_wfo.manager

The user with these roles must also be a manager of the assignment group that is associated with the resource conversion formula.

#### About this task

You can define the start and end dates for which you want to visualize the forecast data. The start date for a forecast configuration is based on the number of historical days you want to consider for data visualization. This is set using the **sn\_agent\_forecast.number\_of\_historical\_days\_in\_timeseries\_chart**.

The published forecast is reflected on the team calendar only when the **Forecast resources for future** job is executed.

The default start date is set to 3 days ago starting from the day before the current day. The end date is calculated based on the period length and the periods to forecast represented in days. For example, if the period length is 1 day and the periods to forecast is 30, then the end date is 30 days including the current day. Forecast can be generated for a maximum period of 90 days.

#### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule \(![Schedule icon](../../workforce-optimization-for-customer-service-configurable/image/schedule-new.png)\) icon.

3.  Click **Forecasts**.

4.  Select the forecast model for which you want to view the time-series data.

    You can visualize each of the forecast parameters that were created for the forecast model.

5.  Click the gear \(![Forecast Parameters icon](../../workforce-optimization-for-customer-service-configurable/image/gear-new.png)\)icon.

6.  Click the plus \(+\) sign.

7.  Configure the forecast parameter.

    1.  From the **Period length unit** list, select the unit for the length of the period to forecast.
    2.  In the **Period length** field, enter the duration of the period to forecast.
    3.  In the **Periods to forecast** field, enter the number of seasons, which is the period length, for which you want to forecast.
    4.  In the **Algorithm** field, select an algorithm you want to use to calculate the forecast.
    5.  Click **Update**.
    The forecast is created in **Draft** state. The forecast is calculated and displays in the forecast model. You can analyze the forecast with the new forecast parameters before you publish it.

8.  To preview a forecast before publishing it, click **Preview**.

    The forecast is calculated using the algorithm and parameters configured in the forecast parameter. When you [create a manual adjustment](configure-wfo-hr.md#) to predict future resources, Demand Forecast overlays the adjustment in the time-series chart.

    |When you|Then the forecast|
    |--------|-----------------|
    |**Unpublish a published forecast**|Become inactive.|
    |**Preview an inactive forecast parameter**|Displays for the date range for which the forecast parameter was active.|
    |**Preview an active forecast**|Displays the time-series data for the future time-period.|

9.  Publish the forecast parameters.

    -   To publish a newly created forecast parameter, click **Save** and then click **Publish**.
    -   To publish an active forecast parameter, click **Publish**.
    **Note:** You can only have one forecast in **Published** state, which is used to calculate the resources.

    When the forecast parameter is published:

    -   The state of the record changes to **Published**.
    -   The **Forecast resources for future** job runs daily and uses the published forecast parameters to calculate the agent forecast. The calculation uses the resource conversion formula to calculate the forecast data from the current point forward. You can view the updated resources in the team calendar.
    -   Any other forecast parameters that were created would be unpublished and inactive.

### Create a manual adjustment for a forecast

Adjust forecasts manually to fine-tune them for greater accuracy. Create the adjustment for a specified time period and analyze how it impacts your forecast.

#### Before you begin

Role required: sn\_hr\_wfo.admin

The user with these roles must also be a manager of the assignment group that is associated with the resource conversion formula.

#### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule \(![Schedule icon](../../workforce-optimization-for-customer-service-configurable/image/schedule-new.png)\) icon.

3.  Click **Forecasts**.

4.  Select the forecast model for which you want to make a manual adjustment.

5.  Click the Manual Adjustments \(\) icon.

6.  Make a manual adjustment.

    1.  Click the plus \(+\) sign.
    2.  On the form, fill in the fields:

<table id="table_uwd_qxv_dpb"><thead><tr><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the manual adjustment.

</td></tr><tr><td>

Start Date Time

</td><td>

Date and time when the manual adjustment for the forecast must start.

</td></tr><tr><td>

End Date Time

</td><td>

Date and time when the manual adjustment for the forecast must end.

</td></tr><tr><td>

Adjustment Unit

</td><td>

Unit for the manual adjustment.Available units:

-   Percentage—adjustment value percentage. For example, if the forecast data shows case count and if the adjustment value is 15, the manual adjustment shows a 15% increase in case count than the forecast data.
-   Number—adjustment value count. For example, if the forecast data shows case count and if the adjustment value is 15, the manual adjustment shows 15 more cases than the forecast data.


</td></tr><tr><td>

Adjustment Value

</td><td>

The numeric value for which you want to adjust the forecast. The value is applied to each group in the Groups \[sys\_user\_groups\] table. The manual adjustment visualization on the time-series chart displays the data for your groups. For example, let's assume that the value is 15 and the unit is number. If you have two groups for a forecast model and both have 2 agents each before you do the manual overlay, when you enter the value as 15, it is applied to each of the two groups and the total value displays as 34.This is calculated as follows:

-   Two agents for group A + the adjustment value 15 = 17
-   Two agents for group B + the adjustment value 15 = 17
The total is 34.

 If you have two groups for a forecast model and both have a volume \(for example: Cases/ Chats\) of 2 before you do the manual overlay, when you enter the value as 15, it is applied to each of the two groups and the total value displays as 34. This is calculated as follows:

 -   Two cases/chats for group A + the adjustment value 15 = 17
-   Two cases/chats for group B + the adjustment value 15 = 17
 The total is 34.

</td></tr></tbody>
</table>    3.  Click **Save**.
    The manual adjustment is created in **Draft** state. The manual adjustment is calculated and displays as a green line in the forecast model. You can analyze or update the forecast with this manual adjustment before you publish it.

7.  Publish the manual adjustment.

    1.  Click the saved manual adjustment that you want to use for forecasting resources.
    2.  Click **Publish**. The state changes to **Ready to Publish**.
    When the **Forecast resources for future** job is run, it calculates the forecast, checks for manual adjustments, applies those values if any, and moves it to the **Published** state.

    **Note:**

    -   When you unpublish a forecast, it moves to **Draft** state. You can delete a forecast that is in **Draft** state.
    -   If you want to end a manual adjustment after it has started and before its end date, you can click **End Now**.
    The forecast will no longer be used in the resource conversion formula.

    When the manual adjustment is published:

    -   The state of the record changes to **Published**.
    -   The adjusted values will be used in the resource conversion formula and the demand forecast displayed on the calendar.
    -   Any other manual adjustment configurations that were created would be unpublished and moved to **Draft** state.

