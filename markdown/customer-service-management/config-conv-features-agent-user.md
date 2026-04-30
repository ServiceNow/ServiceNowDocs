---
title: Update the service portal chat configuration
description: Configure the Now Assist in Virtual Agent chat configuration to ensure Now Assist in Virtual Agent loads on your Customer and Consumer Service Portals when CSM chat is enabled.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Virtual Agent in service portals, Automate and optimize, Use, Customer Service Management]
---

# Update the service portal chat configuration

Configure the Now Assist in Virtual Agent chat configuration to ensure Now Assist in Virtual Agent loads on your Customer and Consumer Service Portals when CSM chat is enabled.

## Before you begin

Role required: workspace\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Agent Chat**.

2.  To configure Now Assist in Virtual Agent loading on your Customer Service Portal:

    1.  On the Service Portal Agent Chat Configuration page, select **Now Assist in Virtual Agent - CSM Chat Config** in the **Name** column.

    2.  On the form, enter a value in the **Order** field.

        **Note:** To display Now Assist in Virtual Agent chat configuration prominently on the portals, set the **Order** value to be either lower or better compared to the old CSM chat configuration.

    3.  In the script box, replace the current script with the following script.

        ```
        (function($sp) {
        	var configObj = {portal: $sp.getValue('url_suffix')},
        		isVAActive = GlidePluginManager.isActive('com.glide.cs.chatbot');
        	
        	configObj.liveagent_application = 'csm';
        	configObj.live_agent_only = !isVAActive;
        	configObj.liveagent_queue = $sp.getDisplayValue('sp_chat_queue');
        
        	var cc = new GlideRecord('customer_contact');
        	cc.addQuery('sys_id', gs.getUserID());
        	cc.query();
        	if (cc.next()) {
        		configObj.liveagent_interaction_contact = cc.getUniqueValue();
        		configObj.liveagent_interaction_account = cc.getValue('account');
        	}
        
        	if (gs.isLoggedIn() && GlidePluginManager.isActive('com.sn_csm_b2b_consumers')) {
        		var consumer = new GlideRecord('csm_consumer');
        		consumer.addQuery('user', gs.getUserID());
        		consumer.query();
        		if (consumer.next()) {
        			var accounts = new sn_acct_consumer.AccountConsumerUtil().getAccountFromConsumer(consumer.getUniqueValue());
        			if (accounts.length > 0) {
        				if (accounts.length == 1) {
        					configObj.liveagent_interaction_account = accounts[0];
        				}
        				configObj.liveAgent_interaction_consumer = consumer.getUniqueValue();
        			}
        		}
        	}
        
        	return configObj;
        })($sp);
        ```

    4.  Select **Update**.

3.  To configure Now Assist in Virtual Agent on your Consumer Service Portal:

    1.  On the Service Portal Agent Chat Configuration page, select **Now Assist in Virtual Agent - CSP Chat Config** in the **Name** column.

    2.  On the form, enter a value in the **Order** field.

        **Note:** To display Now Assist in Virtual Agent chat configuration prominently on the portals, set the **Order** value to be either lower or better compared to the old CSM chat configuration.

    3.  In the script box, replace the current script with the following script.

        ```
        (function($sp) {
        	var configObj = {portal: $sp.getValue('url_suffix')},
        		isVAActive = GlidePluginManager.isActive('com.glide.cs.chatbot');
        	
        	configObj.liveagent_application = 'csm';
        	configObj.live_agent_only = !isVAActive;
        	configObj.liveagent_queue = $sp.getDisplayValue('sp_chat_queue');
        
        	if (gs.isLoggedIn()) {
        		var consumer = new GlideRecord('csm_consumer');
        		consumer.addQuery('user', gs.getUserID());
        		consumer.query();
        		if (consumer.next()) {
        			configObj.liveAgent_interaction_consumer = consumer.getUniqueValue();
        		}
        	}
        	
        	return configObj;
        })($sp);
        ```

    4.  Select **Update**.


## Result

Now Assist in Virtual Agent configuration takes precedence over the standard Virtual Agent chat configuration for the portal.

