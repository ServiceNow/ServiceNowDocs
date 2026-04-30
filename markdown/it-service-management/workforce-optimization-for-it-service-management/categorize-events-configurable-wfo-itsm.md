---
title: Configure event categories for the ITSM Manager Workspace
description: Add an event category. Create or update field configurations for events. You can also specify if an event category must be excluded when the shift coverage for agents is calculated.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up Scheduling in Workforce Optimization for ITSM, Scheduling in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Configure event categories for the ITSM Manager Workspace

Add an event category. Create or update field configurations for events. You can also specify if an event category must be excluded when the shift coverage for agents is calculated.

## Before you begin

Role required: sn\_shift\_planning.admin

The following event category configurations are available by default:

-   Work
-   Meeting
-   Training
-   Custom Event
-   Time Off
-   Break

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Scheduling** &gt; **Event Categories**.

2.  In the **Event Categories** list, click **New**.

3.  In the **Name** field, enter a name for the event category.

4.  If you want to exclude this event category for agent coverage calculation, enable the **Exclude from coverage** check box.

5.  In the **Event field configuration** dialog box, edit the following configuration as needed:

    **Note:**

    -   You can remove any property that does not apply to a type of event.
    -   By default, agents can add attendees to the meeting and training event types.
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

6.  Click **Submit**.


-   **[Configure an event load order in Workforce Optimization for ITSM](add-event-load-property-configurable-workspace.md)**  
Add a system property to display your preferred event categories first on the calendar.

**Parent Topic:**[Setting up Scheduling in Workforce Optimization for ITSM](../concept/setup-scheduling-configurable-workforce-optimization-itsm.md)

