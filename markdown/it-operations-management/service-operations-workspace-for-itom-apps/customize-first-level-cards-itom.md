---
title: Modify the first-level cards in the Service Operations Workspace for ITOM Overview section
description: Customize the data displayed in the first-level cards in the Overview section by configuring various parameters such as the header label, data source, metric, group by field, and viewAllQuery. This allows for a more tailored and relevant display of information.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customize the Service Operations Workspace for ITOM home page, Configuring Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Modify the first-level cards in the Service Operations Workspace for ITOM Overview section

Customize the data displayed in the first-level cards in the Overview section by configuring various parameters such as the header label, data source, metric, group by field, and viewAllQuery. This allows for a more tailored and relevant display of information.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **sys\_ux\_client\_script\_include.list**.

2.  From the UX Client Script Includes list, select `SowEMLandingPageUtilsSNC` client script include definition.

3.  On the UX Client Script Include form, edit the **Script** field.

    For example:

    ```
       }
         };
        const labelMap = {
            'em_alert': {
                'alerts_assigned_to_you': {
                    '1': 'Alerts assigned to you - Urgent',
                    '2': 'Alerts assigned to you - High',
                    '3': 'Alerts assigned to you - Moderate',
                    '4': 'Alerts assigned to you - Low'
                },
                'open_alerts': {
                    '1': 'Open alerts - Urgent',
                    '2': 'Open alerts - High',
                    '3': 'Open alerts - Moderate',
                    '4': 'Open alerts - Low'
                },
                'team_alerts_assigned': 'Assigned team alerts - to ',
                'team_alerts_unassigned': {
                    '1': 'Unassigned team alerts - Urgent',
                    '2': 'Unassigned team alerts - High',
                    '3': 'Unassigned team alerts - Moderate',
                    '4': 'Unassigned team alerts - Low'
                }
            }
    
    ```

4.  Click **Update**.


**Parent Topic:**[Customize the Service Operations Workspace for ITOM home page](customize-sow-landing-page-itom.md)

