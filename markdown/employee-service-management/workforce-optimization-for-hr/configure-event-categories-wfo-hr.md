---
title: Configure event categories
description: Add event categories and create or update field configurations for events in the Manager workspace.
locale: en-US
release: zurich
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up Scheduling, Configure, Workforce Optimization overview, HR Service Delivery, Employee Service Management]
---

# Configure event categories

Add event categories and create or update field configurations for events in the Manager workspace.

## Before you begin

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

## Procedure

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


**Parent Topic:**[Setting up Scheduling for Workforce Optimization for HR](setup-scheduling-wfo-hr.md)

