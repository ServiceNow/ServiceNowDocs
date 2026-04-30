---
title: Setting up Scheduling in Workforce Optimization for Customer Service
description: Manage events using the team calendar. Create different types of event categories. Use scripted extension points to customize event types. Additionally, configure recurring meetings or trainings.Add an event category. Create or update field configurations for events. You can also specify if an event category must be excluded when the shift coverage for agents are calculated.Create multiple events from the same category and add them to the team calendar.Configure schedule adherence properties to calculate the adherence and conformance of your agents so that you can improve the operational efficiency of your organization.Configure and tweak the schedule adherence and conformance formulas using scripted extension points so that you can customize them for your organization.Use extension points to call scripts for event categories such as meeting, time off, or work time.
locale: en-US
release: xanadu
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Setting up Scheduling in Workforce Optimization for Customer Service

Manage events using the team calendar. Create different types of event categories. Use scripted extension points to customize event types. Additionally, configure recurring meetings or trainings.

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

**Parent Topic:**[Configuring Workforce Optimization for Customer Service](setup-configurable-wfo-cs.md)

## Configure event categories for Manager Workspace

Add an event category. Create or update field configurations for events. You can also specify if an event category must be excluded when the shift coverage for agents are calculated.

### Before you begin

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: sn\_shift\_planning.admin

The following event category configurations are available by default:

-   Work
-   Meeting
-   Training
-   Time Off
-   Break
-   Recurring Meeting
-   Recurring Training

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Scheduling** &gt; **Event Categories**.

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


## Create event types to display them on the team calendar

Create multiple events from the same category and add them to the team calendar.

### Before you begin

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: sn\_shift\_planning.admin

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Scheduling** &gt; **Event Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_kb2_yfx_3nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the event type.

</td></tr><tr><td>

Priority Order

</td><td>

Priority of the event type that you want to exclude from the coverage. The higher the number means the higher the priority.For example, let's say you are attending a work event for four hours in a day. You have marked that time window as both a time off and as a meeting event type. If time off has a higher order of priority, then the application excludes that event type from coverage.

</td></tr><tr><td>

Color

</td><td>

Color that identifies this type of event in the team calendar.

</td></tr><tr><td>

Active

</td><td>

Option that when enabled, displays the event type on the calendar.

</td></tr><tr><td>

Category

</td><td>

Type of event, for example, meeting, break, or time off.

</td></tr></tbody>
</table>    **Note:** To enable the Recurring Meetings or Trainings category, in the Event Configuration, select the Active field as **true**. Similarly, to disable the Meetings or Trainings category, in the Event Configuration, select the Active field as **false**.

4.  Click **Submit**.

    **Note:** After an event type is assigned to a shift, that event type cannot be deleted.


## Configure properties for schedule adherence and conformance

Configure schedule adherence properties to calculate the adherence and conformance of your agents so that you can improve the operational efficiency of your organization.

### Before you begin

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: admin

### About this task

The threshold settings for adherence and conformance indicate how many minutes early or late an agent can clock in or clock out to a scheduled work shift without being considered as non-adherent.

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Schedule Adherence** &gt; **Settings**

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Enable Schedule Adherence|Calculation and information about the agents' adherence to the schedules.|
    |Threshold for early checkin for planned shift \(in Minutes\)|Time that you can set for early check-in. This time is the acceptable time for an agent to start the work shift before the actual shift time. The default value is 60 minutes. For example, if an agent's planned work shift is 08:00 to 17:00 and the agent clocks in at 07:00, the threshold time allows flexibility and the agent isn’t considered as a non-adherent agent.|
    |Threshold for adherence% of Time Worked Summary|Percentage that you can set for a threshold in adherence. The agents who don’t qualify to be above the defined threshold value \(70%\) are considered non-adherent agents.|
    |Lower threshold conformance % of Time Worked Summary|Lower threshold percentage that you can set for flexibility in conformance. The agents who don’t qualify for the defined lower and upper conformance threshold values \(80-120\) are considered as non-conformant agents. The default value is 80%.|
    |Upper threshold for conformance % of Time Worked Summary|Upper threshold percentage that you can set for flexibility in conformance. The agents who don’t qualify for the defined lower and upper conformance threshold values \(80-120\) are considered as non-conformant agents. The default value is 120%.|
    |Default threshold time for clock-out event generation \(in Minutes\)|Default threshold time to generate an automatic clock-out event if an agent fails to clock out. The default value is 60 minutes. For example, if an agent's planned work shift is 08:00 to 17:00 and the agent fails to clock out at 17:00, the system waits for 60 minutes as the threshold time and generates an automatic clock-out event.|

3.  Click **Save**.


**Related topics**  


[Scheduling in Workforce Optimization for Customer Service](explore-scheduling-configurable-wfo-cs.md)

[Monitor schedule adherence of your agents](scheduling-configurable-wfo-cs.md#)

[Analyze adherence and conformance from the time worked summary](scheduling-configurable-wfo-cs.md#)

## Modify schedule adherence and conformance formulas by using extension points

Configure and tweak the schedule adherence and conformance formulas using scripted extension points so that you can customize them for your organization.

### Before you begin

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: admin

### About this task

Use the **sn\_shift\_planning.ScheduleAdherenceExtPt** extension point and create an implementation to configure the formulas. You can create multiple implementations. However, the implementation with the lowest order number is executed.

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for `sn_shift_planning.ScheduleAdherenceExtPt`.

3.  On the form banner, click the link **here** to edit the record.

4.  To create your extension point script, click **Create Implementation** in the related links.

5.  Modify the formulas for calculating the schedule adherence and conformance in the `getAdherencePercentage` and `getConformancePercentage` methods.

    ![Scripted extension point displaying the getAdherencePercentage and getConformancePercentage sections.](../image/extension_script_adherence.png)

6.  Click **Update**.


### Result

The schedule adherence and conformance calculations are based on the formulas in the implementation.

## Event type extension points in Workforce Optimization for Customer Service

Use extension points to call scripts for event categories such as meeting, time off, or work time.

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To see a list of extension points that you can use for Workforce Optimization for Customer Service, navigate to **System Extension Points** &gt; **Scripted Extension Points**. In the Extension Points list, open the sn\_shift\_planning.EventManagerextension point.

Use scripted extension points to integrate customizations without altering the core components in the application code. When customizing a base application, you implement the scripted extension points by creating the custom script includes and registering them against the scripted extension points.

|Extension point name|Description|
|--------------------|-----------|
|sn\_shift\_planning.EventManager|Implement this extension point to customize the logic for the event categories that you create.|

You can use extension points to create events such as meeting, training, and time-off requests. For example, for extension point implementations, see the following extension instances in the Implementations related list:

|Category|Extension Script|
|--------|----------------|
|Meeting|AgentScheduleMeetingEventManager|
|Break|AgentScheduleBreakEventManager|
|Training|AgentScheduleTrainingEventManager|
|Time off|AgentScheduleTimeOffEventManager|
|Work|AgentScheduleWorkEventManager|

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

