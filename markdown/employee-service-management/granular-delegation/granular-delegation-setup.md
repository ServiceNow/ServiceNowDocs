---
title: Setting up Granular Delegation
description: Set up Granular Delegation so your employees can delegate their tasks to other employees.
locale: en-US
release: yokohama
product: Granular Delegation
classification: granular-delegation
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Granular Delegation, Employee Service Management]
---

# Setting up Granular Delegation

Set up Granular Delegation so your employees can delegate their tasks to other employees.

Activate the Granular Delegation plugin \(com.glide.granular\_service\_delegation\) for the ServiceNow AI Platform if you have the admin role. For more information, see [Activate Granular Delegation](../task/activate-granular-delegation.md).

Granular delegation has separate records for specifying a delegate and specifying what content the delegate can access. You create a Delegate record each time you want to delegate your service tasks to another user.

Administrators create delegation rules to allow the delegation of specific records. Access Control Rules \(ACLs\) determine if a delegate can access the records that match the delegation rules assigned to them. Creating delegation rules requires an administrator to be familiar with the data model of the delegated services.

|Role|Description|Contains roles|
|----|-----------|--------------|
|Delegation admin \[delegation\_admin\]|Manages granular delegation, setting up delegation rules.|N/A|

-   **User Criteria \(user\_criteria\)**

    Granular delegation can use the User Criteria \(user\_criteria\) table to determine who can be a delegate or a delegator. For more information, see [Create delegation rules](../task/create-delegation-rules.md).

-   **System properties**

    The **com.glide.delegation.default\_days\_since\_update** system property determines how many days to retain inactive delegation records for users or delegates. The default is seven \(7\) days and can be changed to a maximum of 30 days.

    Any delegate record that was created before the start date and hasn't been updated within the last seven days \(or the value entered in the sys property\) is not assigned to a delegate until the delegate record is updated. For example, approval tasks that were created before the number of days in the sys property are not visible to the assigned user. You can create a work note to update the delegate record to make the approval visible to the assigned user.

    **Note:** Changing the value in the sys property does not affect delegate records created before the original value entered.

-   **Scheduled jobs**

    The **Clean Granular Delegation Records** scheduled job runs daily and deletes inactive delegation records based on the **com.glide.delegation.default\_days\_since\_update** system property value.

    The **Notify new delegates** scheduled job runs every 10 minutes and triggers a notification to delegates that their delegation period is starting.


