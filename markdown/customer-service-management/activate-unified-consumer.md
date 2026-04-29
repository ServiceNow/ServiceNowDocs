---
title: Activate Unified Consumer
description: Activate the Unified Consumer functionality within the Customer Service Management \(CSM\) application by updating the Consumer script include. This modification enables you to display the other sys\_user extension records in the reference list for the users in the csm\_consumer table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up a user as a Unified Consumer, Configuring a user as a Unified Consumer, Configuring a Unified User, User management, Set up your environment, Configure, Customer Service Management]
---

# Activate Unified Consumer

Activate the Unified Consumer functionality within the Customer Service Management \(CSM\) application by updating the Consumer script include. This modification enables you to display the other sys\_user extension records in the reference list for the users in the csm\_consumer table.

## Before you begin

Role required: admin

## About this task

To enable access to sys\_users \(internal users\), add the sys\_user to the user extension in the Consumer script include.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Open the Consumer script include and modify the script as follows:

    Add the **initialize** method to the Consumer script include and set **this.userExtensions** value.

    ```
    var Consumer = Class.create();
    
    Consumer.prototype = Object.extendsObject(ConsumerImpl, {
        initialize: function() {
            ConsumerImpl.prototype.initialize.call(this);
            this.userExtensions = ["csm_consumer_user", "sys_user"];
        },
    
        type: 'Consumer',
    
    });
    ```

    **Note:** While creating a consumer user from the consumer form, you’re redirected to the interceptor form to select the user type.

3.  Select **Update**.


## What to do next

Add a user to your instance. For more information, see [Creating and associating a Unified Consumer user to a consumer record](../concept/associating-users-to-a-consumer-record.md#).

