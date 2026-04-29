---
title: Enable Virtual Agent for mobile applications
description: Give your users the ability to chat with a virtual agent through a ServiceNow mobile application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure a contextual link to Virtual Agent, Action functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Enable Virtual Agent for mobile applications

Give your users the ability to chat with a virtual agent through a ServiceNow mobile application.

## Before you begin

Role required: admin

To include virtual agent functionality in your mobile applications, you first must activate and configure Virtual Agent. For details on this process see [Planning and configuring Virtual Agent](https://www.servicenow.com/docs/access?context=configure-virtual-agent&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder

3.  Select the **Functions** category, and then select **New**.

4.  In the **Name** field, enter the name of the data parameter.

    You can have multiple parameters with the same name, so choose a name that you can distinguish easily.

5.  From the **Type** list, select **Chat Launcher**.

6.  In the **Context** field, select **Global**.

7.  Select **Save**.

8.  Navigate to the **Screens** category on the Mobile App Builder home screen and select the launcher screen where you want to add your Virtual Agent quick action or select **New** and choose **New launcher** to create a new launcher screen.

9.  In the **Quick action function** instance field, select the function created in the previous steps.

10. Select **Save**.


**Parent Topic:**[Configure a contextual link to Virtual Agent](sg-av-context-action.md)

