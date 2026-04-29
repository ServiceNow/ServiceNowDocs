---
title: Configure event categories
description: Configure field settings for event categories. You can create or update field configurations for events and specify if an event category should be excluded from shift coverage calculations for agents.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up scheduling, Workforce Optimization, Set up workforce, Configure, Field Service Management]
---

# Configure event categories

Configure field settings for event categories. You can create or update field configurations for events and specify if an event category should be excluded from shift coverage calculations for agents.

## Before you begin

**Important:** To access the next generation of the Workforce Optimization for Field Service application, transition to the Workforce Optimization for Field Service application that is available from the ServiceNow Store. You can now configure Workforce Optimization for Field Service using the [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=australia&pubname=australia-application-development&ft:locale=en-US). For more information see, [Configuring Workforce Optimization for Field Service](../concept/configuring-wfo-fsm.md).

Role required: sn\_shift\_planning.admin

## About this task

The following event category configurations are available by default:

-   Work
-   Meeting
-   Training
-   Break
-   Time Off
-   Actual Work
-   Personal

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for FSM** &gt; **Scheduling** &gt; **Event Categories**.

2.  In the **Event Categories** list, select **New**.

3.  In the **Name** field, enter a name for the event category.

4.  If you want to exclude this event category for agent coverage calculation, enable the **Exclude from coverage** check box.

5.  In the **Event field configuration** dialog box, edit the following configuration as necessary:

    **Note:** You can remove any property that doesn’t apply to a type of event.

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
                    "attendeesFieldForAgent": { //Add attendees to events
                    "mandatory": true,
                    "visible":true,
                    "readOnly": false,
                    "allowAllUsers": false,
                    "label":"Attendees"
                    },
                    "startDate": {
                    "mandatory": true,
                    "readOnly": false
                    },
                    "endDate": {
                    "mandatory": true,
                    "readOnly": false
                    },
                     "description":{               //Add text fields to the form
    		    "mandatory":false,
    		    "readOnly":false,
    		    "label":"Notes"
    		    },
                    "additionalSelectors":[
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

6.  Select **Submit**.


