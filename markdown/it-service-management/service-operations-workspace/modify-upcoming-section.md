---
title: Configure the Upcoming section on the landing page
description: Configure the data displayed in the Upcoming section.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Landing page configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the Upcoming section on the landing page

Configure the data displayed in the **Upcoming** section.

## Before you begin

Role required: admin

## About this task

Using an extension point, you can call the custom scripts to extend the functionality of the **Upcoming** section and also easily integrate customizations without having to alter the base code. For information about extension points, see Creating and adding a scripted extension point.

|Extension point|Description|
|---------------|-----------|
|sn\_sow.UpcomingLinkProvider|Gets a list of upcoming task records \(changes, incident, requests, and overdue tasks\) for the same day and the next day.|

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  From the Extension Points list, select **sn\_sow.UpcomingLinkProvider**.

3.  Create an implementation using the **Create Implementation** related link or edit an implementation from the Implementations related list.

    Following is an example of how to add a new announcement type for change tasks.

    -   Name: MyCustomUpcomingLinkProvider\_ChangeTask
    -   Script:

        ```
         var PREFIX_QUERY = 'active=true^' + assignToQuery; 
        
                var TODAY_QUERY = '^planned_start_dateONToday@javascript:gs.beginningOfToday()@javascript:gs.endOfToday()'; 
        
                var TOMORROW_QUERY = '^splanned_start_dateONTomorrow@javascript:gs.beginningOfTomorrow()@javascript:gs.endOfTomorrow()'; 
        
                var encodedQuery = null; 
        
                var listTitle = gs.getMessage("Change_Task"); 
        
                if ('beginningOfToday' == request.from && 'endOfToday' == request.to) { 
        
                    encodedQuery = PREFIX_QUERY + TODAY_QUERY; 
        
                } else if ('beginningOfTomorrow' == request.from && 'endOfTomorrow' == request.to) { 
        
                    encodedQuery = PREFIX_QUERY + TOMORROW_QUERY; 
        
                } else { 
        
                    throw gs.getMessage("Unsupported date range"); 
        
                } 
        
                var LIMIT = 10; 
        
                var changeTaskGr = new GlideRecordSecure('change_task'); 
        
                changeTaskGr.addEncodedQuery(encodedQuery); 
        
                changeTaskGr.setLimit(LIMIT + 1); 
        
                changeTaskGr.query(); 
        
                var count = changeTaskGr.next() ? changeTaskGr.getRowCount() : 0; 
        
                var items = []; 
        
                if (count > 0) { 
        
                    var msg = null; 
        
                    if (1 == count) { 
        
                        msg = gs.getMessage("{0} change task", [count]) + ""; 
        
                    } else { 
        
                        if (count > LIMIT) { 
        
                            msg = gs.getMessage("More than {0} change task(s)", [LIMIT.toString()]) + ""; 
        
                        } else { 
        
                            msg = gs.getMessage("{0} change task(s)", [count]) + ""; 
        
                        } 
        
                    } 
        
                    var route = { 
        
                        route: 'simplelist', 
        
                        fields: { 
        
                            table: changeTaskGr.getTableName() 
        
                        }, 
        
                        params: { 
        
                            listTitle: listTitle, 
        
                            query: changeTaskGr.getEncodedQuery() 
        
                        } 
        
                    }; 
        
                    if (1 == count) { 
        
                        route = { 
        
                            route: 'record', 
        
                            fields: { 
        
                                table: changeTaskGr.getTableName(), 
        
                                sysId: changeTaskGr.getUniqueValue() 
        
                            } 
        
                        }; 
        
                    } 
        
                    var item = { 
        
                        label: msg, 
        
                        type: 'route', 
        
                        value: route, 
        
                        "startsWith": { 
        
                            "icon": "change-outline", 
        
                            "align": "center" 
        
                        }, 
        
                        "opensWindow": false, 
        
                        "configAria": {}, 
        
                        "download": false 
        
                    }; 
        
                    items.push(item); 
        
                } 
        
                return items; 
        ```

4.  Select **Update** and save the script include record.

5.  Create a task to verify if it is displayed as an upcoming task.

    For example, create a change task.

    1.  From the **All** menu, navigate to **change\_task.list**.

    2.  Select **New**.

    3.  Specify the required information.

        -   Short Description
        -   Description
        -   Planned start date. You can specify today's date.
        -   Assigned to. Specify the user for whom the upcoming task should appear.
    4.  Select **Submit**.

    5.  Verify that the task appears in the **Upcoming** section of the Service Operations Workspace landing page for the selected user.


**Parent Topic:**[Landing page configurations in Service Operations Workspace for ITSM](../concept/landing-page-configurations-sow-itsm.md)

