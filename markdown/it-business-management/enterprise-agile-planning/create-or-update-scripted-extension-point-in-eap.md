---
title: Create implementation of a Scripted Extension Point in EAP
description: Update the default Scripted Extension Point or create a scripted extension point using the default one as a template to filter the data displayed on the EAP dashboard.
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring custom dashboards in EAP, Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create implementation of a Scripted Extension Point in EAP

Update the default Scripted Extension Point or create a scripted extension point using the default one as a template to filter the data displayed on the EAP dashboard.

## Before you begin

[Associate the EAP read-only role to the dashboard](add-the-eap-read-only-role-to-the-dashboard.md).

Role required: sn\_apw\_advanced.eap\_admin

## About this task

The **Scripted Extension Points** enable you to create a custom query to filter the information from different data sources. By default, each EAP configuration is associated with an extension point. Each extension point handles all the team types associated with it. You must create an implementation of the scripted extension point every time you create a new EAP configuration.

**Important:** Perform this task only for a custom configuration or if you want to customize a default dashboard. This task is not required if you are using any of the default configurations.

## Procedure

1.  Navigate to **All** &gt; **Scripted Extension Points**.

2.  Search for and open the EAPDashboardsEncodedQueryProvider \(sn\_apw\_advanced.EAPDashboardsEncodedQueryProvider\) scripted extension point.

3.  Select the **Create implementation** related link to create an implementation of this scripted extension point.

    The new implementation record form is shown.

4.  Update the **Name** field of the newly created Implementation to a custom name of your choice.

    Ensure that you don't include any spaces in the name. For example, rename the implementation to **MyConfigEAPDashboardsEncodedQueryProvider**.

5.  Select **Update**.

6.  Open the EAPDashboardsEncodedQueryProvider \(sn\_apw\_advanced.EAPDashboardsEncodedQueryProvider\) scripted extension point.

7.  From the Implementations related list, click the Class of your newly created implementation record to open it.

8.  Update the **Script** field to include the following.

    -   In the `getConfigId` function, enter the sys\_id of your EAP configuration.
    -   In the `fetchEncodedQueries` function, enter queries to filter the information for each level of your EAP configuration such as iteration ID, team type, and team ID.

        The following is an example script for the default Large Solution Configuration.

        ```
        fetchEncodedQueries: function(teamType, teamId, iterationId) {
                switch (teamType) {
                    case "sn_apw_advanced_agile_team":
                        return {
                            rm_story: `iteration=${iterationId}`,
                            sn_apw_advanced_eap_iteration: `sys_id=${iterationId}`,
                            sn_gf_goal_m2m_relationship: `table_name=sn_apw_advanced_eap_iteration^entity_id=${iterationId}`,
                            sn_apw_advanced_eap_iteration_db_view: `iter_eap_team=${teamId}`
                        };
                    case "sn_apw_advanced_agile_release_train":
                        return {
                            sn_align_core_feature: `iteration=${iterationId}`,
                            sn_apw_advanced_eap_iteration: `sys_id=${iterationId}`,
                            sn_gf_goal_m2m_relationship: `table_name=sn_apw_advanced_eap_iteration^entity_id=${iterationId}`,
                            sn_apw_advanced_eap_iteration_db_view: `iter_parent=${iterationId}`
                        };
                    case "sn_apw_advanced_solution_train":
                        return {
                            sn_apw_advanced_eap_iteration: `eap_team.parent=${teamId}`,
                            sn_align_core_capability: `eap_team=${teamId}^OReap_team.parent=${teamId}`
                        };
                    default:
                        return {
                            sn_align_core_eap_planning_item: `iteration=${iterationId}`,
                        };
                }
            },
        
            getConfigId: function() {
                return "e4e11e0977243110740fefc0aa5a99f9";
            },
        
        
        ```

9.  **Update**.


## Result

The next time you reload the Home tab for your EAP teams, the dashboard shows the filtered data according to the updates you made to the implementation.

