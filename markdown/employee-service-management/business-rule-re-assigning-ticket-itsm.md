---
title: Configure business rule for reassigning tickets
description: Configure the business rule for reassigning the tickets.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [IT Service Management integration, Customize Integrations for Employee Experience, Manage, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Configure business rule for reassigning tickets

Configure the business rule for reassigning the tickets.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

    ![Business rules](../images/business-rules.png)

2.  Click **New**.

3.  On the form, fill in the fields.

    ![Business rule to re-assign ticket](../images/buisness-rule-re-assigning-itsm.png)

    In the **Advanced** tab, update the **Script** fields.

    ![Script for re assigning ticket](../images/business-rule-re-assignment-itsm02.png)

<table id="table_gpx_p1z_vqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the business rule

</td></tr><tr><td>

Table

</td><td>

Table to which the ticket should be re-assigned.

</td></tr><tr><td>

Active

</td><td>

Check this box

</td></tr><tr><td>

Advanced

</td><td>

Check this box

</td></tr><tr><td>

Where to run

</td><td>

-   When: **async**
-   Update: Check this box
-   Filter Conditions: Apply the filter condition of the reassigning the ticket business rule.

Select the fields to which the ticket should be re-assigned. Ex: Assigned to field.

</td></tr><tr><td>

Advanced

</td><td>

Script: Copy and paste the script. Modify the values as required.Update the field name in the `assigned_to` if you are using a different value.

 ```

var importChatUtils = new sn_tcm_collab_hook.MSTeamsImportChatUtils();	
var chatUtil = new sn_tcm_collab_hook.MSTeamsChatUtil();
	
var azureIds = chatUtil.getAzureIds([current.getValue('assigned_to')]); //Update the assigned_to field if required 
var credentialAlias = chatUtil.getTeamsChatCredentialsAliasGr();
var chats = importChatUtils.getChatsofADocument(current.sys_id);
var azureId = '';
	
if (azureIds && azureIds.azureUserIds && azureIds.azureUserIds.length > 0) 
	azureId = azureIds.azureUserIds[0];
	
if(gs.nil(azureId)){
	gs.addErrorMessage(gs.getMessage('Invalid Azure Id, cannot add user to Chat'));
	return;
}
	
chats.forEach( function(chat) {
	importChatUtils.addMemberToChat(chat,azureId,credentialAlias, current.getValue('assigned_to')); //Update the assigned_to field if required
});
```

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Customize IT Service Management integration with ServiceNow](../concept/customize-sn-ms-teams.md)

