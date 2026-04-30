---
title: Configure the donuts in the tier 1 landing page
description: Configure the data displayed in donuts in the Overview section of the tier 1 landing page.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Landing page configurations in SOW for ITSM, Getting started, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the donuts in the tier 1 landing page

Configure the data displayed in donuts in the **Overview** section of the tier 1 landing page.

## Before you begin

Role required: admin

## About this task

You can customize header label, data source, metric, group by field, and viewAllQuery for all donuts. For example, Problems assigned to me donut.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Overview**.

2.  On the **Overview** tab from the **Initial Setup** section, select the **Configure the landing page** option.

3.  On the Landing Page form, under **Tier 1** section, select **Configure** next to **Donut configurations**.

4.  If the PAR dashboard is active on the landing page, do the following:

    1.  [Configure the tier 1 dashboard configuration](https://www.servicenow.com/docs/access?context=edit-db-in-ac&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

        **Note:** If you’re creating a dashboard, you can use the saved visualizations to create a card for the dashboard. The data visualization is visible only to the users based on the respective roles.

        Ensure that you have added the value as Service Operations Workspace in the **Dashboard Visibility**.

    2.  Select the default dashboard for the SOW landing page from the **Dashboard loaded on the Landing Page** drop-down option. Select **Save**.
    3.  After modifying the elements in the dashboard, select **Save**.
5.  If the PAR dashboard isn't active on the landing page, edit the **Script** field add the code inside the class **ServiceDeskLandingPageUtils**.

    **Note:** This method is copied from **SowIncidentLandingPageUtilsSNC**. To add a new donut or to remove an existing one you need to copy **getVisualizationConfig** method to **SowIncidentLandingPageUtils** and modify as per your requirement.

    ```
    static async getVisualizationConfig(helpers, mode, conditionalRecordCount=0) {
                const evamDef = this.getEvamDef();
                const visualizationConfig = [{
                        "id": "incident_assigned",
                        "tableName": "incident",
                        "tableDisplayValue": "Incident",
                        "myWorkQuery": "active=true^assigned_toDYNAMIC90d1921e5f510100a9ad2572f2b477fe^state!=6",
                        "myTeamQuery": "active=true^assigned_toISNOTEMPTY^assignment_groupDYNAMICd6435e965f510100a9ad2572f2b47744^state!=6",
                        "listView": mode == "your_work" ? "sow_landing_page_assigned" : "sow_landing_page",
                        "header": mode == 'your_work' ? await helpers.translate("Incidents assigned to you") : await helpers.translate("Incidents assigned to your team"),
                        "groupByField": "state",
                        "evamId": evamDef['incidentEvamDefinitionId'],
                        "updated_on": "^ORDERBYDESCsys_updated_on",
                        "roles":mode == "your_work" ? ["itil","sn_incident_write"] : ["itil","sn_incident_read"],
                    },
                    {
                        "id": "incident_sla",
                        "tableName": "task_sla",
                        "tableDisplayValue": "Task SLA",
                        "myWorkQuery": "task.sys_class_name=incident^task.assigned_toDYNAMIC90d1921e5f510100a9ad2572f2b477fe^task.active=true^sla.type=SLA^ORsla.type=OLA^active=true^time_left<=1970-01-08 00:00:00",
                        "myTeamQuery": "task.sys_class_name=incident^task.assignment_groupDYNAMICd6435e965f510100a9ad2572f2b47744^task.active=true^sla.type=SLA^ORsla.type=OLA^active=true^time_left<=1970-01-08 00:00:00",
                        "listView": 'sow_landing_page',
                        "header": await helpers.translate("Incident SLAs"),
                        "groupByField": "time_left",
                        "evamId": evamDef['incidentSlaEvamDefinitionId'],
                        "updated_on": "^ORDERBYtime_left",
                        "roles":mode == "your_work" ? ["itil","sn_incident_write"] : ["itil","sn_incident_read"],
                    },
                    {
                        "id": "unassigned_incidents",
                        "tableName": "incident",
                        "tableDisplayValue": "Incident",
                        "myWorkQuery": "active=true^assigned_toISEMPTY^assignment_groupDYNAMICd6435e965f510100a9ad2572f2b47744",
                        "myTeamQuery": "active=true^assigned_toISEMPTY^assignment_groupDYNAMICd6435e965f510100a9ad2572f2b47744",
                        "listView": mode == "your_work" ? "sow_landing_page_assigned" : "sow_landing_page",
                        "header": await helpers.translate("Unassigned incidents"),
                        "groupByField": "priority",
                        "evamId": evamDef['incidentEvamDefinitionId'],
                        "updated_on": "^ORDERBYDESCsys_updated_on",
                        "roles":mode == "your_work" ? ["itil","sn_incident_read"] : ["itil","sn_incident_read"],
                    },
                    {
                        "id": "catalog_tasks",
                        "tableName": "sc_task",
                        "tableDisplayValue": "Catalog Task",
                        "myWorkQuery": "active=true^assigned_toDYNAMIC90d1921e5f510100a9ad2572f2b477fe",
                        "myTeamQuery": "active=true^assignment_groupDYNAMICd6435e965f510100a9ad2572f2b47744",
                        "listView": mode == "your_work" ? "sow_landing_page_assigned" : "sow_landing_page",
                        "header": mode == 'your_work' ? await helpers.translate("Catalog tasks assigned to you") : await helpers.translate("Catalog tasks assigned to your team"),
                        "groupByField": "state",
                        "evamId": evamDef["catalogTaskEvamDefinitionId"],
                        "updated_on": "^ORDERBYDESCsys_updated_on",
                        "roles":mode == "your_work" ? ["itil","sn_request_write"] : ["itil","sn_request_read"],
                    }
                ];
    
                if(mode=='your_work' && conditionalRecordCount>0){
                    const conditionalConfig = await this.getConditionalVisualizationConfig(helpers);
                    visualizationConfig.push(conditionalConfig);
                }
    
                return visualizationConfig;
            }
     
    ```

    To add Problem donut to tier 1 landing page, add additional snippets as per your requirement similar to the code snippet mentioned below.

    ```
    {
    "id": "problemsAssigned",
                    "tableName": "problem",
                    "tableDisplayValue": "Problem",
                    "myWorkQuery": "active=true^assigned_toDYNAMIC90d1921e5f510100a9ad2572f2b477fe",
                    "myTeamQuery": "active=true^assignment_groupDYNAMICd6435e965f510100a9ad2572f2b47744",
                    "header": mode == 'your_work' ? await helpers.translate("Problems assigned to you") : await helpers.translate("Problems assigned to your team"),
                    "groupByField": "state",
                    "evamId": "5f0697b8f49bc510f8773ad5bd0ae292",
                    "updated_on": "^ORDERBYDESCsys_updated_on",
                    "roles":mode == "your_work" ? ["itil","problem_coordinator"] : ["itil","sn_problem_read","problem_task_analyst"]
    }
    
    ```

    Copy the **fetchTitle** method from **SowIncidentLandingPageUtilsSNC** to add labels for list that is displayed when you click on the donut.

    ```
        static async fetchTitle(table, selectedField, groupByField, groupMode = false) {
                if(selectedField == undefined){
                     selectedField = 'all';
                    }
                const labelMap = {
                    'incident': {
                        'state': {
                            'all':'Incidents',
                            '1': 'New incidents',
                            '2': 'In Progress incidents',
                            '3': 'On Hold incidents',
                            '6': 'Resolved incidents'
                        },
                        'priority': {
                            'all':'Unassigned incidents',
                            '1': 'P1 unassigned incidents',
                            '2': 'P2 unassigned incidents',
                            '3': 'P3 unassigned incidents',
                            '4': 'P4 unassigned incidents',
                            '5': 'P5 unassigned incidents'
                        }
                    },
                    'sc_task': {
                        'state': {
                            'all':'Catalog tasks',
                            '-5': 'Pending catalog tasks',
                            '1': 'Open catalog tasks',
                            '2': 'Work in progress catalog tasks'
                        }
                    },
                    'task': {
                        'sys_class_name': {
                            'sc_task': 'Catalog tasks delegated to you',
                            'incident': 'Incidents delegated to you'
                        }
                    }
                };
    
                if((table == 'incident' && groupByField == 'priority') || table == 'task')
                    return labelMap[table][groupByField][selectedField];
    
                if (groupMode)
                    return labelMap[table][groupByField][selectedField] + ' assigned to your team';
                return labelMap[table][groupByField][selectedField] + ' assigned to you';
            }
    
    ```

    Add the labels as mentioned in the below example code block to view them as a list heading when you click on the donut.

    ```
       'problem': {  
    'state' :{      
         '101': 'New problems',
                        '102': 'Assess problems',
                        '106': 'Resolved problems',
                        '104': 'Fix in Progress problems',
                        '103': 'Root Cause Analysis problems',
                        'all':'Problems'
          }
                    },
    
    ```

6.  Select **Update**.


