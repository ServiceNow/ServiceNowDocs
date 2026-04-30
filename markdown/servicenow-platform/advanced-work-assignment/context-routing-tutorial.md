---
title: Tutorial: Route interactions by context
description: Learn how you can configure Advanced Work Assignment to route conversations to agents according to the context of the conversation.Create a queue for the Chat service channel that routes product issues.Create a queue for the Chat service channel that routes billing issues.Create a queue for the Chat service channel that routes order issues.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [External routing overview, Work item queues, Work items, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Tutorial: Route interactions by context

Learn how you can configure Advanced Work Assignment to route conversations to agents according to the context of the conversation.

Activate the Customer Service Management Demo Data \(com.snc.customerservice.demo\) plugin.

A basic understanding of context variables is required. For more information on context variables, see [Virtual Agent scripts](https://www.servicenow.com/docs/access?context=virtual-agent-scripts&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

The **What can we help you with?** record producer is available by default with the Customer Service Management Demo Data \(com.snc.customerservice.demo\) plugin. In the record producer, chat requesters can specify one of three issue categories that they need help with:

-   Product
-   Billing
-   Order

Whichever category they select passes a value through the *liveagent\_csp\_category* context variable. Learn how to create queues that route conversations to agents according to the values passed through this context variable.

**Parent Topic:**[External routing overview](../concept/awa-external-routing-overview.md)

## Create a queue for product issues

Create a queue for the Chat service channel that routes product issues.

### Before you begin

Role required: awa\_admin or admin

### Procedure

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


## Create a queue for billing issues

Create a queue for the Chat service channel that routes billing issues.

### Before you begin

Role required: awa\_admin or admin

### Procedure

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


## Create a queue for order issues

Create a queue for the Chat service channel that routes order issues.

### Before you begin

Role required: awa\_admin or admin

### Procedure

1.  From the Queues list view, click **New**.

2.  Enter the following information in the fields listed:

    -   Name: Order Support
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
    		if(jsonBlob.liveagent_csp_category == 'order')
    			return true;
    	}
    	return false;
    })(current);
    ```

4.  Click **Submit**.


