---
title: Create a queue for billing issues
description: Create a queue for the Chat service channel that routes billing issues.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tutorial: Route interactions by context, Configure reasons for rejecting work items, Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create a queue for billing issues

Create a queue for the Chat service channel that routes billing issues.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  From the Queues list view, click **New**.

2.  Enter the following information in the fields listed:

    -   Name: Billing Support
    -   Service channel: Chat
    -   Condition mode: Advanced
3.  In the **Script** field, enter this script:

    ```
    (function executeCondition(/* glide record */ current) {  
    	var contextTable = current.getValue('context_table');
    	var interactionBlobRecord = new GlideRecord(contextTable);
    	interactionBlobRecord.addQuery('sys_id',current.getValue('context_document'));
    	interactionBlobRecord.query();
    
    	if(interactionBlobRecord.next()){
    		var jsonBlob = JSON.parse(interactionBlobRecord.getValue('value'));
    		if(jsonBlob.liveagent_csp_category == 'billing')
    			return true;
    	}
    	return false;
    })(current);
    ```

4.  Click **Submit**.


