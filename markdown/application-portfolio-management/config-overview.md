---
title: Create and apply a new configuration for the Overview section
description: Create visualization configurations for the Portfolio Overview section and apply them as needed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Create and apply a new configuration for the Overview section

Create visualization configurations for the Portfolio Overview section and apply them as needed.

## Before you begin

Role required: sn\_apm.apm\_admin

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Enterprise Architecture Workspace** &gt; **Configuration**.

2.  On the APM EA Configurations page, select **New**.

3.  On the form, fill in the fields.

<table id="table_pvc_h12_hwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the configuration.

</td></tr><tr><td>

Active

</td><td>

Option to make the configuration active to appear on the Overview section.

</td></tr><tr><td>

Section

</td><td>

Section name for which you’re creating the configuration.

</td></tr><tr><td>

Order

</td><td>

Position of the card in the sequential order of all other cards in that section.

</td></tr><tr><td>

Configuration Type

</td><td>

Type of the configuration. If the **Section** field is set to **Overview**, then this field value is automatically set to **Visualization**.

</td></tr><tr><td>

Saved Visualization

</td><td>

Name of the configuration. Select the lookup icon \(![Lookup icon](../image/icon-lookup.png)\) to select a configuration from the PAR Visualizations list.**Note:** You can create and save a visualization configuration using the Platform Analytics Workspace. For instructions, see [Create a single score visualization in the Visualization Designer](https://www.servicenow.com/docs/access?context=create-dv-sing-sc-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Manage Access

</td><td class="icon">

Option to provide access to the selected users and user groups. Add users or groups by selecting the lock icon \(![Lock icon](../../../common/image/icon-lock.png)\) for **Users** or **Groups**.

</td></tr></tbody>
</table>    Sample Configuration script to add a card \(Business applications at the same capability hierarchy level\) in the Business Portfolio tab of the Insights section:

    ```
    responseFromScript(); 
    
    function responseFromScript() { 
    
        return { 
    
       "title":{ 
    
          "label":"Test insight card", 
    
          "size":"sm", 
    
          "lines":2 
    
       }, 
    
       "count":"6", 
    
       "description":{ 
    
          "label":"6 testing description", 
    
          "lines":2 
    
       }, 
    
       "countLabel":"test count", 
    
       "buttonLabel":"View list", 
    
       "buttonTooltip":"View list for Business applications at the same capability hierarchy level", 
    
       "border":{ 
    
          "color":"brown", 
    
          "variant":"secondary" 
    
       }, 
    
       "highlightedHeader":{ 
    
          "label":"Business Portfolio", 
    
          "icon":"bag-outline" 
    
       }, 
    
       "navigation":{ 
    
          "route":"list", 
    
          "title":"Business applications at the same capability hierarchy level", 
    
          "fields":{ 
    
             "table":"cert_follow_on_task", 
    
             "listTitle":"Business applications at the same capability hierarchy level" 
    
          }, 
    
          "params":{ 
    
             "query":"sys_created_on>=2022-12-15 11:36:37^audit.sys_id=ae25162c3ba20300028fe79c83efc492^state=1", 
    
             "listView":"" 
    
          } 
    
       }, 
    
       "displayText":"6 Business applications at the same capability hierarchy level" 
    
    }; 
    
    } 
    ```

4.  Select **Submit**.


**Parent Topic:**[Configuring Enterprise Architecture Workspace](../concept/eaw-concept/configure-eaw.md)

