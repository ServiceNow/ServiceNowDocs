---
title: Customize the on-call support group recommendations
description: Configure the support group recommendations that should be displayed in the Experts on-call panel for an incident.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Contextual side panel configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Customize the on-call support group recommendations

Configure the support group recommendations that should be displayed in the **Experts on-call** panel for an incident.

## Before you begin

Role required: sn\_sow\_admin.sn\_sow\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  From the Script Includes list, select **OnCallUtilsSow**.

3.  To configure the support group recommendations, modify the **Script** field.

    For information about how these groups are available for an incident, see [Experts on-call in Service Operations Workspace](../concept/on-call-sow.md#).

    ```
    getRecommendedGroups: function(table, sysId, fieldWatchList) {
    		if(!table || !sysId) {
    			return {};
    		}
    		
    		var recommendedGroups = {};
    		var gr = new GlideRecord(table);
    		if (gr.get(sysId)) {
    			var self = this;
    			
    			if (table == this.TABLES.INCIDENT) {	
    				fieldWatchList.forEach(function(watchField) {
    					if (watchField.field == "assignment_group" && !recommendedGroups[watchField.value + ""] && self._isOnCallDefinedForTheGroup(watchField.value)) {
    						recommendedGroups[watchField.value + ""] = gs.getMessage("Recommended based on assignment group");
    					} else if (watchField.field == "cmdb_ci") {
    						var cmdbCiGr = new GlideRecord(self.TABLES.CMDB_CI);
    						if (cmdbCiGr.get(watchField.value + "")) {
    							if (cmdbCiGr.support_group && !recommendedGroups[cmdbCiGr.support_group + ""] && self._isOnCallDefinedForTheGroup(cmdbCiGr.support_group + "")) {
    								recommendedGroups[cmdbCiGr.support_group + ""] = gs.getMessage("Recommended based on affected CI");
    							}
    						}
    					} else if (watchField.field == "business_service") {
    						var businessServiceGr = new GlideRecord(self.TABLES.CMDB_CI_SERVICE);
    						if (businessServiceGr.get(watchField.value + "")) {
    							if (businessServiceGr.support_group && !recommendedGroups[businessServiceGr.support_group + ""] && self._isOnCallDefinedForTheGroup(businessServiceGr.support_group + "")) {
    								recommendedGroups[businessServiceGr.support_group + ""] = gs.getMessage("Recommended based on impacted service");
    							}
    						}
    					}
    				});
    			}
    		}
    		
    		return recommendedGroups;
    	}
    ```

4.  Click **Update**.


**Parent Topic:**[Contextual side panel configurations in Service Operations Workspace for ITSM](../concept/contextual-side-panel-configurations-sow-itsm.md)

