---
title: Configuring Advanced Work Assignment
description: Quickly install the required and popular plugins through the plugin page after selecting any Get \[plugin\] button on the Advanced Work Assignment home page. Plan and configure Advanced Work Assignment \(AWA\).
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Advanced Work Assignment, Manage people and work, Conversational Interfaces]
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


-   **[Get started with Advanced Work Assignment](implement-awa.md)**  
To implement Advanced Work Assignment, complete these initial configuration and setup steps.
-   **[Install Conversational SMS service channel](install-conversational-sms.md)**  
You can install the Conversational SMS service channel application \(sn\_awa\_sms\_int\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Create or configure a service channel](awa-create-service-channel.md)**  
Create or configure a service channel that is used in Advanced Work Assignment \(AWA\).
-   **[Set up the Conversational SMS service channel](configure-conversational-sms.md)**  
Configure the Conversational SMS service channel store app.
-   **[Set up a custom service channel](setup-custom-channel.md)**  
Set up a custom service channel to expand the type and scope of work that is routed automatically to your agents.
-   **[Create a queue to route new change requests](queue-example.md)**  
Create a work item queue in Advanced Work Assignment that routes new change requests through the service channel that handles change requests.
-   **[Create an assignment pool of agents](assignment-pool-example.md)**  
Create an eligible assignment pool in Advanced Work Assignment that receives overflow work items, just in case you need more help from other agents to handle change requests.
-   **[Make your service channel available in Agent Workspace](presence-state-example.md)**  
Make your service channel available in Agent Workspace so that agents can receive change requests in their inbox.
-   **[Customize how change requests appear in an agent inbox](inbox-card-example.md)**  
Customize how change requests appear in an agent inbox so that agents receive enough information to decide whether to accept or reject the work item.
-   **[Create or change a work item size override](awa-modify-work-item-size.md)**  
Create a work item size override if you want Agent Affinity to calculate an agent's workload using a work item size other than the default.
-   **[Create a work item queue](awa-create-queue.md)**  
Define or change a queue so that you can determine which work items are routed automatically to agents through a given service channel.
-   **[Configure agent assignment rules](awa-create-assignment-rule.md)**  
Set the Advanced Work Assignment criteria for assigning work items to agents. Choose the assignment rule that considers the agent with the most capacity or the agent who has gone the longest without work. Establish the settings for the auto-assign handling, reject handling, and skill handling related lists.
-   **[Create or change an inbox layout](awa-modify-inbox-layout.md)**  
Create or change the card layout for inbox items for a given service channel. Card layouts are displayed in the agent inbox view of Agent Workspace.
-   **[Override agent capacity for selected agents](awa-change-agent-capacity.md)**  
Change the default number of work items that an agent can handle for a service channel.
-   **[Define agent pools eligible for assignment](awa-specify-assignment-eligibility.md)**  
Specify pools of agents eligible to receive overflow work assignments for a queue. An eligible assignment pool can consist of one or more groups of agents available to work on items in the queue. This feature enables Advanced Work Assignment to find a qualified agent from a wider pool of agents.
-   **[Set work item sort order](awa-set-work-sort-order.md)**  
Specify the order in which work items in a queue are sorted.
-   **[Create and manage queue triggers](awa-create-queue-triggers.md)**  
Create and manage queue triggers to set off multiple actions during customer wait times for a particular queue.
-   **[Create a connection Alias for third-party provider](create-cnctn-alias.md)**  
Create a connection Alias for your third-party provider to enable external routing on your instance.
-   **[Create a custom flow action](create-custom-action.md)**  
Create a custom flow action in Workflow Studio for enabling external routing.
-   **[Create a subflow](create-subflow-extrnl-route.md)**  
Create a subflow for the Workflow Studio for enabling external routing.
-   **[Create a payload for external third-party providers](create-payload-extrnl-provider.md)**  
Create a payload for external third-party providers to send your work items to the external queue.
-   **[Link Subflow and Payload to External Queues](link-subflow-payload-extrnl.md)**  
Link the subflow and the payload to your external queue to complete external routing.
-   **[Enable external routing for queues](enable-awa-external-routing.md)**  
Configure Advanced Work Assignment to route work items in the queue using external routing.
-   **[Configure External Routing events and payload](config-extrnlroute-event-payload.md)**  
Configure Advanced Work Assignment with external routing using AWA External Service API for CCaaS and third-party providers to enable them to submit events.
-   **[Define external routing test implementation](../concept/define-extrnl-routng-plugin.md)**  
Define the External Routing Test Tools plugin \[com.glide.awa.external.test\_tools\] with a simplified external-routing-provider sample Automated Test Framework \(ATF\) by using the demo data that is available with the plugin installation.
-   **[Configure Agent Affinity rules](awa-configure-agent-affinity.md)**  
Create or change the Agent Affinity rules that route work items in Advanced Work Assignment.
-   **[Set Agent Affinity rules](awa-set-agent-affinity-for-queue.md)**  
Specify the Agent Affinity rules to determine the order in which work items in a queue are sorted.
-   **[Deactivate Agent Affinity](awa-deactivate-agent-affinity.md)**  
Deactivate Agent Affinity if you do not want Agent Affinity to assign work assignments to agents.
-   **[Configure agent presence states](awa-configure-agent-presence.md)**  
Create or modify the availability states that agents use to indicate whether they can receive work or are offline or away. Agents set these states in their Workspace Inbox.
-   **[Configure reasons for rejecting work items](awa-configure-reject-reasons.md)**  
Define the reasons that agents can use to decline work assignments that they receive in their Agent Workspace inbox. A reject reason can apply to all service channels or a single channel that you specify.
-   **[Configure reassignable settings](../../workspace/task/reassign-rejected-timed-out-work-items.md)**  
Configure whether an agent who rejected a work item is eligible to be offered the same work item.
-   **[Wrap up configuration](wrap-up-configuration.md)**  
Set up the wrap up configuration.
-   **[Wrap up codes](wrap-up-codes.md)**  
Define the wrap up codes.
-   **[Wrap up segments](wrap-up-segments.md)**  
Define the wrap up segments.
-   **[Configure an agent's maximum universal capacity](awa-universal-capacity.md)**  
Prevent an agent from being assigned too many work items by configuring the agent's maximum universal capacity. If the agent's maximum universal capacity has been reached, additional work items won’t be assigned to the agent.
-   **[Create or change groups for Advanced Work Assignment queues](awa-groups.md)**  
Create or manage groups that have associated Advanced Work Assignment queues.
-   **[AWA post work item subflow](awa-post-work-item-subflow.md)**  
Configure the base system AWA post work item subflow by defining the input in Workflow Studio.
-   **[Configure messaging actions](../../virtual-agent/task/configure-messaging-actions.md)**  
Create or modify messaging actions that are performed when an event occurs. These actions apply only to messaging.
-   **[Enable logging for Advanced Work Assignment](awa-activate-logging.md)**  
Enable logging to monitor AWA routing and assignment.
-   **[Activate Agent Affinity](awa-activate-agent-affinity.md)**  
You can activate the Agent Affinity plugin \(com.glide.awa.agent\_affinity\) if you have the admin role.
-   **[Activate Conversational Messaging](../../virtual-agent/task/activate-messaging-actions.md)**  
You can activate the Conversational Messaging plugin \(com.glide.messaging.awa\) if you have the admin role.

**Parent Topic:**[Advanced Work Assignment](../concept/awa-application-landing-page.md)

