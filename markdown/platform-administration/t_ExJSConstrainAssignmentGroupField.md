---
title: Constrain the assignment group field
description: This example shows how to use an advanced reference qualifier with JavaScript and a script include to restrict the incident Assignment group choices to only the groups that contain the user specified in the Assigned to field.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure reference qualifiers, Reference qualifiers, Reference field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Constrain the assignment group field

This example shows how to use an advanced reference qualifier with JavaScript and a script include to restrict the incident **Assignment group** choices to only the groups that contain the user specified in the **Assigned to** field.

## Before you begin

Role required: personalize\_dictionary or admin

## Procedure

1.  Open an incident.

2.  Right-click the **Assignment group** label and select **Configure Dictionary**.

3.  If the form appears in **Default view**, under **Related Links**, click **Advanced view**.

4.  In the **Use reference qualifier** field, ensure that the **Advanced** option is selected.

5.  In the **Reference qual** field, enter `javascript:new ReferenceQualifierHelper().backfillAssignmentGroup()`.

6.  Save the record.

7.  Navigate to **System Definitions** &gt; **Script Includes**.

8.  Click **New**.

9.  Name your script includes as `ReferenceQualifierHelper` to match the Javascript in the following step.

    This name ensures the API Name is generated correctly, based on the Name field.

10. [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) with the following JavaScript code.

    Ensure that the **Accessible form** field is properly set for the environment.

    ```
    var ReferenceQualifierHelper = Class.create();
    ReferenceQualifierHelper.prototype = {
    	
    	backfillAssignmentGroup:function() {
    		var assigneeGroupsQualifier = '';
    		var assignee = current.assigned_to;
    		
    		//return if the assigned_to value is empty (this causes all groups to be returned)
    		if(!assignee)
    			return;
    		
    		//sys_user_grmember has the user to group relationship
    		var grAssigneeGroups = new GlideRecord('sys_user_grmember');
    		
    		grAssigneeGroups.addQuery('user',assignee);
    		grAssigneeGroups.query();
    		
    		while(grAssigneeGroups.next()) {
    			if (assigneeGroupsQualifier.length == 0) {
    				// Create the beginning of the qualifier and add the 1st group
    				assigneeGroupsQualifier = 'sys_idIN' + grAssigneeGroups.getValue('group');
    			}
    			else {
    				// build a comma separated string of groups if there is more than one
    				assigneeGroupsQualifier += (',' + grAssigneeGroups.group);
    			}
    		}
    		// return Groups where assigned to is in those groups we use IN for lists
    		
    		gs.log('DP: RefQual = ' + assigneeGroupsQualifier);
    		
    		return assigneeGroupsQualifier;
    	},
    	type: 'ReferenceQualifierHelper'
    };
    
    ```


## What to do next

To test, create an incident and select a user in the **Assigned to** field. Click the **Assignment group** lookup icon. Only the groups that contain the user you selected appear. For example, you assign an incident to Bob Smith, who belongs to the **Database** group and the **Networking** group. The only options that appear in the assignment group are **Database** and **Networking**.

