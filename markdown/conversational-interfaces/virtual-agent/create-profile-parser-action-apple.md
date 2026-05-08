---
title: Create a profile parser action for Apple Messages for Business
description: Create an action to parse the user information response and find the corresponding user on the ServiceNow instance for Conversational Integration with Apple Messages for Business using the information provided here.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OAuth setup for Apple Messages for Business, Configure, Conversational Integration with Apple Messages for Business, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a profile parser action for Apple Messages for Business

Create an action to parse the user information response and find the corresponding user on the ServiceNow® instance for Conversational Integration with Apple Messages for Business using the information provided here.

## Before you begin

Role required: admin

## Procedure

1.  Refer to the following procedure to create a new action. Create an action in Workflow Studio.

2.  In the Workflow Studio integration hub, set the **Input** field to `response_body (string)`.

    ![Workflow Studio integration hub page, showing profile parser action with code snippet example.](../images/flowdesigner-action.png "Workflow Studio example")

3.  You can use the following example script to help create your script for the action.

    ```
    (function execute(inputs, outputs) { 
        try { 
            var profile = JSON.parse(inputs.response_body); 
            var email = profile[0]['profile']['email']; 
            var user_sys_id = ""; 
            var result = { 
                "auth_success": false, 
                "user_sys_id": "" 
            }; 
            if (email) { 
                result['auth_success'] = true; 
                var userGr = new GlideRecord("sys_user"); 
                userGr.addQuery("email", email); 
                userGr.query(); 
                if (userGr.getRowCount() == 1) 
                    if (userGr.next()) 
                        user_sys_id = userGr.getUniqueValue(); 
    
                result['user_sys_id'] = user_sys_id; 
            } 
            outputs.result = result; 
        } catch (e) { 
            gs.error("Error in Virtual Agent - Parse User Profile: " + e.message); 
            throw e; 
        } 
    })(inputs, outputs);
    ```

4.  Set the **Output** field to the following:

    ```
    result = {  
        "auth_success": false,  
        "user_sys_id": "1234" 
        };
    ```


