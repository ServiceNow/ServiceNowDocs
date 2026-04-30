---
title: Configuring Advanced Work Assignment
description: Quickly install the required and popular plugins through the plugin page after selecting any Get \[plugin\] button on the Advanced Work Assignment home page. Plan and configure Advanced Work Assignment \(AWA\).
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring Advanced Work Assignment

Quickly install the required and popular plugins through the plugin page after selecting any **Get \[plugin\]** button on the Advanced Work Assignment home page. Plan and configure Advanced Work Assignment \(AWA\).

## Before you begin

The AWA home page appears after you have installed and updated the Omni-Experience Standard Feature Set to the latest version through the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

Role required: admin

## About this task

After installing the Advanced Work Assignment plugin and any relevant org-specific plugins, the following list outlines the basic planning and configuration steps that you must determine for AWA:

-   Determine what to route – Configure the base service channels to be used.
-   Determine where to route – Define the work item queues and the routing rules, execution order, work item sort order, and strategy.
-   Determine how to assign work items – Define the assignment rules that determine the work items pushed to agents.
-   Determine what the agent sees – Set the inbox card layouts and presence \(availability\) states that agents use in their Agent Workspace inbox.

## Procedure

1.  Navigate to **Advanced Work Assignment** &gt; **Home**, and then select the **Get Advanced Work Assignment plugin** button from the First, install a required plugin section.

    **Note:** Only users with the sys\_admin role can install a plugin from the Advanced Work Assignment home page. For example, if a user with the awa\_admin role tried to install the Advanced Work Assignment plugin, they're prompted to contact their administrator for installation. After the Advanced Work Assignment plugin is installed, all AWA home page options are available in the application navigator for users with the admin and awa\_admin roles.

    The All Applications page opens in a new window or tab.

2.  In the All Applications page, select **Install** and complete the installation prompts.

    The AWA home page experience refreshes and the Get targeted routing capabilities section appears.

3.  Install org-specific AWA plugins through the **Get plugin** button for ServiceNow® IT Service Management \(ITSM\), ServiceNow® Customer Service Management, and/or ServiceNow® HR Service Delivery \(HRSD\) plugins.

    The AWA home page experience refreshes and the Get the most popular plugins section appears.

4.  Install popular plugins, such as Agent Chat, Walk-up Experience, and/or Performance Analytics, to boost your AWA experience.

5.  In the Essential settings section, select **Set up service channels** to [configure the service channels](awa-create-service-channel.md) that you activated.

    1.  [Create or change an inbox layout](awa-modify-inbox-layout.md).

    2.  [Override agent capacity](awa-change-agent-capacity.md), as needed.

6.  In the Essential settings section, select **Set up queues** to [create work item queues](awa-create-queue.md) for your service channels.

    1.  [Set the sort order for work items](awa-set-work-sort-order.md) in the queue.

7.  In the Essential settings section, select **Set up assignment rules** to [configure the work assignment rules](awa-create-assignment-rule.md) used to push work to the appropriate agents.

8.  In the Additional settings section, consider configuring the following parameters to improve your AWA functionality.

    1.  Select **Set up presence states** to [configure availability states](awa-configure-agent-presence.md) states that agents use to indicate whether they can receive work or are offline or away.

    2.  Select **Set up reject reasons** to [define the reject reasons](awa-configure-reject-reasons.md) that agents can use to decline work assignments that they receive in their Agent Workspace inbox.

    3.  Select **Set up universal capacity** to [configure your team's maximum universal capacity](awa-universal-capacity.md) to prevent an agent from being assigned too many work items.

    4.  Select **Set up groups** to [create groups of user sets](awa-groups.md) who share a common purpose.

9.  In the Advanced settings section, consider configuring the following parameters to improve your AWA functionality.

    **Note:** Advanced settings cards appear conditionally after installing their respective plugin.

    1.  Select **Set up Agent Affinity** to [create or change the Agent Affinity rules](awa-configure-agent-affinity.md) that route work items in Advanced Work Assignment.

    2.  Select **Set up Shift-based Assignment** to [assign work items to agents based on shifts](awa-create-assignment-rule.md).


-   **[Advanced Work Assignment home page](../concept/awa-admin-console-home.md)**  
Explore, implement, and maintain ServiceNow® Advanced Work Assignment using a home-page experience. Discover AWA, install relevant plugins, and configure settings for AWA through the Advanced Work Assignment home page available to admins.
-   **[Get started with Advanced Work Assignment](implement-awa.md)**  
To implement Advanced Work Assignment, complete these initial configuration and setup steps.
-   **[Install Conversational SMS service channel](install-conversational-sms.md)**  
You can install the Conversational SMS service channel application \(sn\_awa\_sms\_int\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Activate Agent Affinity](awa-activate-agent-affinity.md)**  
You can activate the Agent Affinity plugin \(com.glide.awa.agent\_affinity\) if you have the admin role.
-   **[Activate Conversational Messaging](../../virtual-agent/task/activate-messaging-actions.md)**  
You can activate the Conversational Messaging plugin \(com.glide.messaging.awa\) if you have the admin role.
-   **[Service channels](../concept/awa-service-channels.md)**  
Provide customer support by automatically routing incoming work to agents through service channels.
-   **[Work items](../concept/awa-work-items.md)**  
View Advanced Work Assignment work items using the Work Items menu options.
-   **[Work assignments](../concept/awa-assignment.md)**  
After routing work items to the appropriate queues and corresponding agent groups, Advanced Work Assignment \(AWA\) pushes work to the most qualified agent using the assignment criteria that you specify. Assignment criteria revolve around the type of assignment rule \(most capacity or last assigned\) and whether skills are defined.
-   **[Using Agent Affinity](../concept/awa-agent-affinity-concept.md)**  
Agent Affinity is an Advanced Work Assignment feature that lets you assign work items by an agent's work history, related task, or account team affinity.
-   **[Agent Inbox controls](../concept/agent-experience.md)**  
Control certain elements of the agent experience in Agent Workspace. Define the agent presence \(availability\) states and the work item rejection reasons used by agents to decline work assignments in their Agent Workspace inbox.
-   **[Advanced Work Assignment Inbox Sentiment display](../concept/awa-inbox-sentiment-display.md)**  
Surface the sentiment in AWA Inbox for agents to get the visibility of requester sentiment \( if available\) during live agent handoff or agent transfer for all channels.
-   **[Wrap up overview](../concept/wrap-up-overview.md)**  
When agents close an interaction, the wrap up feature enables them to enter closing details and wrap up codes for future reference.
-   **[Management](../concept/management.md)**  
Configure Advanced Work Assignment properties using the Management menu options.
-   **[AWA group queue priorities](../concept/awa-group-queue-priorities.md)**  
Use the group queue priority feature to set a queue or work item preference for a given group of agents. For a given group or agent with limited capacity, this feature controls which queues should be preferred if matching work items are found in both.
-   **[Configure messaging actions](../../virtual-agent/task/configure-messaging-actions.md)**  
Create or modify messaging actions that are performed when an event occurs. These actions apply only to messaging.
-   **[Enable logging for Advanced Work Assignment](awa-activate-logging.md)**  
Enable logging to monitor AWA routing and assignment.

**Parent Topic:**[Advanced Work Assignment](../concept/awa-application-landing-page.md)

