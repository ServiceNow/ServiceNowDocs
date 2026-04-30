---
title: Create deflection configurations and patterns
description: Set up deflection settings to create deflection configurations and deflection patterns that you can map to deflection topic blocks in Virtual Agent conversation topics. These deflections help you to track the issues that Virtual Agent helped to resolve or actually resolved for a user.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using the deflection topic block, Case and incident deflection, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create deflection configurations and patterns

Set up deflection settings to create deflection configurations and deflection patterns that you can map to deflection topic blocks in Virtual Agent conversation topics. These deflections help you to track the issues that Virtual Agent helped to resolve or actually resolved for a user.

## Before you begin

Review [Using the deflection topic block to track deflections in Virtual Agent](../concept/deflections-virtual-agent.md).

Watch this video for more information about deflection tracking. ![Video link to deflection tracking.](../../conversational-interfaces/image/icon-video-link.png)[Virtual Agent Academy: Measure success and user journey in Conversational Analytics](https://www.youtube.com/watch?v=YMAaTSzPhwM&list=PLkGSnjw5y2U79gjQuQW-2GBqzEccwFkWH&index=21)

**Note:** For information about configuring components of the Virtual Agent Analytics dashboard \(such as Performance Analytics widgets\), see [Add and configure components](https://www.servicenow.com/docs/access?context=add-components&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

    The **Conversational Interfaces Settings** page opens in a new tab.

2.  Navigate to **Virtual Agent** &gt; **Deflection metrics** &gt; **View all**.

3.  To enable tracking of deflection metrics, turn on the toggle under **Activate**.

4.  To create new Deflection Configurations, click **New**.

5.  In the Create Deflection Configuration form, enter these deflection configuration properties:

    |Field|Description|
    |-----|-----------|
    |Name|Short and meaningful name for the deflection configuration.|
    |Description|Short description about the deflection configuration.|

6.  Click **Save**.

    A new Deflection Configuration is created.

7.  To add new deflection patterns to a deflection configuration, select the deflection configuration in which you want to add the deflection pattern.

8.  Click **New**.

    In the Create Deflection Pattern form, enter these deflection pattern properties:

    |Field|Description|
    |-----|-----------|
    |Name|Short and meaningful name for the deflection pattern.|
    |Outcome|Result of the deflection in a Virtual Agent conversation.|
    |Primary Activity Table|Table that is associated with the activity that you are categorizing in the deflection pattern. For example, if the Virtual Agent is helping to prevent the creation of a task for the activity, then you can specify the task table.|

    **Note:** If you are creating a generic pattern that is used for tracking different deflections, you can leave the **Primary Activity Table** field empty.

    The primary activity table that is associated with each activity helps in calculating the deflection rate for a particular business area. For example, if Virtual Agent resolves 42 VPN issues and overall 100 VPN incidents are created, the deflection rate for VPN issues is 42/142 or 30 percent.

9.  Click **Save**.


**Parent Topic:**[Using the deflection topic block to track deflections in Virtual Agent](../concept/deflections-virtual-agent.md)

