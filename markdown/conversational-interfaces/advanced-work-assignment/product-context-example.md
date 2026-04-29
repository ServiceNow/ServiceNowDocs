---
title: Create a queue for product issues
description: Create a queue for the Chat service channel that routes product issues.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tutorial: Route interactions by context, Configure reasons for rejecting work items, Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create a queue for product issues

Create a queue for the Chat service channel that routes product issues.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select **New**.

3.  Enter the following information in the fields listed:

    -   Name: Product Support
    -   Service channel: Chat
    -   Condition mode: Advanced
4.  In the **Script** field, enter this script:

    ```
    (function executeCondition(/* glide record */ current) {  
    	var contextTable = current.getValue('context_table');
    	var interactionBlobRecord = new GlideRecord(contextTable);
    	interactionBlobRecord.addQuery('sys_id',current.getValue('context_document'));
    	interactionBlobRecord.query();
    
    	if(interactionBlobRecord.next()){
    		var jsonBlob = JSON.parse(interactionBlobRecord.getValue('value'));
    		if(jsonBlob.liveagent_csp_category == 'product')
    			return true;
    	}
    	return false;
    })(current);
    ```

5.  Click **Submit**.


