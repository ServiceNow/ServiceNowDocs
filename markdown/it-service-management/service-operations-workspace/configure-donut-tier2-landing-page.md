---
title: Configure the donuts in the tier 2 landing page
description: Configure the data displayed in donuts in the Overview section of the tier 2 landing page.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Landing page configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the donuts in the tier 2 landing page

Configure the data displayed in donuts in the **Overview** section of the tier 2 landing page.

## Before you begin

Role required: admin

## About this task

You can customize header label, data source, metric, group by field, and viewAllQuery for all donuts. For example, Catalog tasks assigned to me donut.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Overview**.

2.  On the **Overview** tab, from the **Initial Setup** section, select the **Configure the landing page** option.

3.  On the Landing Page form, under **Tier 2** section, select **Configure** next to **Donut configurations**.

4.  If the PAR dashboard is active on the landing page, do the following:

    1.  [Configure the tier 2 dashboard configuration](https://www.servicenow.com/docs/access?context=edit-db-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

        **Note:** If you’re creating a dashboard, you can use the saved visualizations to create a card for the dashboard. The data visualization is visible only to the users based on the respective roles.

        Ensure that you have added the value as Service Operations Workspace in the **Dashboard Visibility**.

    2.  Select the default dashboard for the SOW landing page from the **Dashboard loaded on the Landing Page** drop-down option. Select **Save**.
    3.  After modifying the elements in the dashboard, select **Save**.
5.  If the PAR dashboard isn't active on the landing page, edit the **Script** field add the code inside the class **SOWLandingPageTier2Utils**.

    ```
    static async getVisualizationConfig(helpers, mode, conditionalRecordCount) {
                const visualizationConfig = [{
                    "id": "incidentAssigned",
                    "tableName": "incident",
                    "tableDisplayValue": "Incident",
                    "myWorkQuery": "active=true^assigned_toDYNAMIC90d1921e5f510100a9ad2572f2b477fe^state!=6",
                    "myTeamQuery": "active=true^assignment_groupDYNAMICd6435e965f510100a9ad2572f2b47744^state!=6",
                    "header": mode == 'your_work' ? await helpers.translate("Incidents assigned to you") : await helpers.translate("Incidents assigned to your team"),
                    "groupByField": "state",
                    "evamId": "01a404e8b7203010e69dbc16de11a93f",
                    "updated_on": "^ORDERBYDESCsys_updated_on",
                    "roles":mode == "your_work" ? ["itil","sn_incident_write"] : ["itil","sn_incident_read"],
                },
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
                    "roles":mode == "your_work" ? ["itil","problem_coordinator"] : ["itil","sn_problem_read","problem_task_analyst"],
                },
                {
                    "id": "changesAssigned",
                    "tableName": "change_request",
                    "tableDisplayValue": "Change Request",
                    "myWorkQuery": "active=true^assigned_toDYNAMIC90d1921e5f510100a9ad2572f2b477fe",
                    "myTeamQuery": "active=true^assignment_groupDYNAMICd6435e965f510100a9ad2572f2b47744",
                    "header": mode == 'your_work' ? await helpers.translate("Changes assigned to you") : await helpers.translate("Changes assigned to your team"),
                    "groupByField": "state",
                    "evamId": "e1f06c4194130110f87765e94545da91",
                    "updated_on": "^ORDERBYDESCsys_updated_on",
                    "roles":mode == "your_work" ? ["itil","sn_change_write"] : ["itil","sn_change_read"],
                },
                {
                    "id": "taskAssigned",
                    "tableName": "task",
                    "tableDisplayValue": "Task",
                    "myWorkQuery": "active=true^assigned_toDYNAMIC90d1921e5f510100a9ad2572f2b477fe^sys_class_name=incident_task^ORsys_class_name=problem_task^ORsys_class_name=change_task^ORsys_class_name=sc_task",
                    "myTeamQuery": "active=true^assignment_groupDYNAMICd6435e965f510100a9ad2572f2b47744^sys_class_name=incident_task^ORsys_class_name=problem_task^ORsys_class_name=change_task^ORsys_class_name=sc_task",
                    "header": mode == 'your_work' ? await helpers.translate("Tasks assigned to you") : await helpers.translate("Tasks assigned to your team"),
                    "groupByField": "sys_class_name",
                    "evamId": "615d205d94df0110f87765e94545da03",
                    "updated_on": "^ORDERBYDESCsys_updated_on",
                    "roles":mode == "your_work" ? ["itil","sn_incident_write","sn_incident_task_assigned_user","problem_task_analyst","sn_change_write","sn_change_task_assigned_user","sn_request_write"] : ["itil","sn_incident_read","sn_incident_task_assigned_user","sn_problem_read","problem_task_analyst","sn_change_read","sn_change_task_assigned_user","sn_request_read","catalog"],
                }];
    
                if(mode=='your_work' && conditionalRecordCount>0){
                    const conditionalConfig = await this.getConditionalVisualizationConfig(helpers);
                    visualizationConfig.push(conditionalConfig);
                }
    
                return visualizationConfig;
            }
            
    
    ```

    Add below snippet object to add Catalog Tasks donut to tier2 landing page.

    ```
      {
                        "id": "catalog_tasks",
                        "tableName": "sc_task",
                        "tableDisplayValue": "Catalog Task",
                        "myWorkQuery": "active=true^assigned_toDYNAMIC90d1921e5f510100a9ad2572f2b477fe",
                        "myTeamQuery": "active=true^assignment_groupDYNAMICd6435e965f510100a9ad2572f2b47744",
                        "listView": mode == "your_work" ? "sow_landing_page_assigned" : "sow_landing_page",
                        "header": mode == 'your_work' ? await helpers.translate("Catalog tasks assigned to you") : await helpers.translate("Catalog tasks assigned to your team"),
                        "groupByField": "state",
                        "evamId": “4a59c876c7323010d7e818b1c7c26083”,
                        "updated_on": "^ORDERBYDESCsys_updated_on",
                        "roles":mode == "your_work" ? ["itil","sn_request_write"] : ["itil","sn_request_read"],
                    }
    
     
    ```

    Copy **getLabelMaps** and/or fetchTitle method from **SOWLandingPageTier2UtilsSNC** to add labels for list that is displayed when you click on the donut.

    ```
    static async fetchTitle(table, nameValueMap, groupMode = false, elementId) {
                if(table === "task") {
                    return this.getLabelMaps(table, nameValueMap['sys_class_name'], groupMode, elementId);
                }
                return this.getLabelMaps(table, nameValueMap['state'], groupMode, elementId);
            }
    
            static getLabelMaps(table, selectedField, groupMode = false, elementId) {
                if(selectedField == undefined){
                    selectedField = 'all';
                 }
                const labelMap = {
                    'incident': {
                        '1': 'New incidents',
                        '2': 'In Progress incidents',
                        '3': 'On Hold incidents',
                        '6': 'Resolved incidents',
                        'all':'Incidents'
                    },
                    'change_request': {
                        '0': 'In Review changes',
                        '-1': 'Implement changes',
                        '-2': 'Scheduled changes',
                        '-3': 'Authorize changes',
                        '-4': 'Assess changes',
                        '-5': 'New changes',
                        'all':'Changes'
                    },
                    'problem': {
                        '101': 'New problems',
                        '102': 'Assess problems',
                        '106': 'Resolved problems',
                        '104': 'Fix in Progress problems',
                        '103': 'Root Cause Analysis problems',
                        'all':'Problems'
                    },
                    'task': {
                        'incident_task': 'Incident tasks',
                        'problem_task': 'Problem tasks',
                        'change_task': 'Change tasks',
                        'sc_task': 'Catalog tasks',
                        'incident': 'Incidents',
                        'problem': 'Problems',
                        'change_request': 'Change requests',
                        'all':'Tasks'
                    }
                };
                if(elementId === 'delegated_task')
                    return labelMap[table][selectedField] + ' delegated to you';
                if (groupMode)
                    return labelMap[table][selectedField] + ' assigned to your team';
                return labelMap[table][selectedField] + ' assigned to you';
            }
    
    ```

    Catalog task labels can be added to the code snippet below to view them on the donut.

    ```
                    'sc_task': {
                            'all':'Catalog tasks',
                            '-5': 'Pending catalog tasks',
                            '1': 'Open catalog tasks',
                            '2': 'Work in progress catalog tasks'
                    },
    
    ```

6.  Select **Update**.


**Parent Topic:**[Landing page configurations in Service Operations Workspace for ITSM](../concept/landing-page-configurations-sow-itsm.md)

