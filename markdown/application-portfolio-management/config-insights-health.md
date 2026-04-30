---
title: Create and apply a new configuration for the Health or Insights section
description: Create configurations for the Health or Insights section and apply them as needed.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure the Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create and apply a new configuration for the Health or Insights section

Create configurations for the Health or Insights section and apply them as needed.

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

Option to make the configuration active to appear on the Health or Insights section.

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

Type of the configuration. If the **Section** field is set to any of the following, then this field value is automatically set to **Script**.-   Health
-   Insights - Application Portfolio
-   Insights - Business Portfolio
-   Insights - Information Portfolio
-   Insights - Technology Portfolio


</td></tr><tr><td>

Configuration Script

</td><td>

Script of the configuration.

</td></tr><tr><td>

Manage Access

</td><td>

Option to provide access to the selected users and user groups. Add users or groups by clicking the lock icon for **Users** or **Groups**.

</td></tr></tbody>
</table>    Sample Configuration script to add a card \(Business Capabilities not Assessed\) in the Health section:

    ```
    function responseFromScript(filters) { 
    
        return {"count":74,"percentage":"45","subtext":"45% of all Capabilities","query":"sys_idIN016d2c3d18400300964f2ff0d21a4ee4,016d2c3d18400300964f2ff0d21a4eeb,016d6c3d18400300964f2ff0d21a4e00,016d6c3d18400300964f2ff0d21a4e0b,016d6c3d18400300964f2ff0d21a4e0e,056d2c3d18400300964f2ff0d21a4ee2,056d2c3d18400300964f2ff0d21a4ee9,056d2c3d18400300964f2ff0d21a4ef7,056d6c3d18400300964f2ff0d21a4e13,096d2c3d18400300964f2ff0d21a4ee0,096d2c3d18400300964f2ff0d21a4ef5,096d2c3d18400300964f2ff0d21a4efc,096d6c3d18400300964f2ff0d21a4e03,0d6d2c3d18400300964f2ff0d21a4ee5,0d6d2c3d18400300964f2ff0d21a4eec,0d6d2c3d18400300964f2ff0d21a4efa,0d6d6c3d18400300964f2ff0d21a4e08,116d6c3d18400300964f2ff0d21a4e23,156d6c3d18400300964f2ff0d21a4e21,343ab8b1c172d700964f1c9d9204dfc4,3df0ce8111f01300964fb19f04b5016c,3eaa906187082110cb387406dabb3502,416d2c3d18400300964f2ff0d21a4eee,416d2c3d18400300964f2ff0d21a4efc,416d6c3d18400300964f2ff0d21a4e03,416d6c3d18400300964f2ff0d21a4e0a,456d2c3d18400300964f2ff0d21a4ef3,4ad8bca987482110cb387406dabb3548,4d6d2c3d18400300964f2ff0d21a4ef6,596d6c3d18400300964f2ff0d21a4e22,5d6d6c3d18400300964f2ff0d21a4e19,816b418b876f1110cb387406dabb3548,816d2c3d18400300964f2ff0d21a4eea,816d2c3d18400300964f2ff0d21a4ef8,816d2c3d18400300964f2ff0d21a4eff,856d2c3d18400300964f2ff0d21a4ee1,856d2c3d18400300964f2ff0d21a4ee8,856d2c3d18400300964f2ff0d21a4ef6,896d2c3d18400300964f2ff0d21a4ee6,896d2c3d18400300964f2ff0d21a4ef4,896d6c3d18400300964f2ff0d21a4e02,896d6c3d18400300964f2ff0d21a4e09,896d6c3d18400300964f2ff0d21a4e10,8d6d2c3d18400300964f2ff0d21a4ee4,8d6d2c3d18400300964f2ff0d21a4eeb,8d6d2c3d18400300964f2ff0d21a4ef2,8d6d2c3d18400300964f2ff0d21a4ef9,8d6d6c3d18400300964f2ff0d21a4e00,916d6c3d18400300964f2ff0d21a4e22,956d6c3d18400300964f2ff0d21a4e19,a770d85187046110cb387406dabb3540,c16d2c3d18400300964f2ff0d21a4eed,c16d2c3d18400300964f2ff0d21a4ef4,c16d2c3d18400300964f2ff0d21a4efb,c4c7273087442110cb387406dabb3520,c56d2c3d18400300964f2ff0d21a4ee4,c56d2c3d18400300964f2ff0d21a4eeb,c56d6c3d18400300964f2ff0d21a4e00,c56d6c3d18400300964f2ff0d21a4e0e,c96d2c3d18400300964f2ff0d21a4ee2,c96d2c3d18400300964f2ff0d21a4ee9,c96d2c3d18400300964f2ff0d21a4ef0,c96d2c3d18400300964f2ff0d21a4efe,c96d6c3d18400300964f2ff0d21a4e05,c96d6c3d18400300964f2ff0d21a4e13,cd6d2c3d18400300964f2ff0d21a4ee7,cd6d2c3d18400300964f2ff0d21a4eee,d16d6c3d18400300964f2ff0d21a4e1e,d56d6c3d18400300964f2ff0d21a4e15,d56d6c3d18400300964f2ff0d21a4e1c,dd026ed887d82110cb387406dabb3548,dd6d6c3d18400300964f2ff0d21a4e18,ed4b175c87902110cb387406dabb3553,efbf3eb187bb11102f631f473cbb3571","table":"cmdb_ci_business_capability","listView":"business_capability_apm_view","icon":"exclamation Fill"} 
    
    } 
    ```

    Sample Configuration script to add a card in the Application Portfolio or Business Portfolio or Information Portfolio in the Insights section:

    ```
    months - selected upto months filter  
    
    showProd - show only production filter  
    
     
    
    responseFromScript(months, showProd); 
    
     
    
    function responseFromScript(months, showProd) { 
    
     
    
        var currentDateTime = new GlideDateTime(); 
    
        currentDateTime.addMonthsLocalTime(months); 
    
        var queryDate = currentDateTime.getLocalDate(); 
    
        var query = "technology_lifecycle.earliest_lifecycle_date<=javascript:gs.dateGenerate('" + queryDate + "','start')"; if (showProd) { 
    
            query = query + "^business_service.used_for=Production"; 
    
        } 
    
        var productInventoryGR = new GlideAggregate('sn_apm_tpm_discovered_technology'); 
    
        productInventoryGR.addEncodedQuery(query); 
    
        productInventoryGR.addAggregate("count(distinct", 'technology_lifecycle.hardware_model'); 
    
        productInventoryGR.setGroup(false); 
    
        productInventoryGR.query(); 
    
        if (productInventoryGR.next()) { 
    
            hwProductsCount = productInventoryGR.getAggregate("count(distinct", 'technology_lifecycle.hardware_model'); 
    
        } 
    
        if (hwProductsCount > 0) { 
    
            var hpRiskDesc = gs.getMessage("by {0}", [queryDate]); 
    
            return { 
    
                'title': { 
    
                    'label': gs.getMessage("Hardware models with lifecycle risk"), 
    
                    'size': "sm", 
    
                    'lines': 2 
    
                }, 
    
                'count': hwProductsCount, 
    
                'description': { 
    
                    'label': hpRiskDesc, 
    
                    'lines': 2 
    
                }, 
    
                'countLabel': gs.getMessage("Hardware models count"), 
    
                'buttonLabel': gs.getMessage("View list"), 
    
                'buttonTooltip': gs.getMessage("View list for hardware models with lifecycle risk"), 
    
                'border': this.cardDetails[3].border, 
    
                'highlightedHeader': this.cardDetails[3].header, 
    
                'navigation': { 
    
                    "route": "list", 
    
                    "title": gs.getMessage("Hardware models with lifecycle risk"), 
    
                    "fields": { 
    
                        "table": "sn_apm_tpm_discovered_technology", 
    
                        "listTitle": gs.getMessage("Hardware models with lifecycle risk") 
    
                    }, 
    
                    "params": { 
    
                        "query": query + "^ORDERBYtechnology_lifecycle.earliest_lifecycle_date", 
    
                        "listView": "" 
    
                    } 
    
                }, 
    
                'ariaLabel': { 
    
                    "aria-label": gs.getMessage("View list for hardware models with lifecycle risk") 
    
                } 
    
            }; 
    
        } 
    
        return false; 
    
    } 
    ```

4.  Click **Submit**.


**Parent Topic:**[Configure the Enterprise Architecture Workspace](customize-workspace.md)

