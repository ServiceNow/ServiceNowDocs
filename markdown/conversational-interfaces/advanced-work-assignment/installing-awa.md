---
title: Configuring Advanced Work Assignment
description: Quickly install the required and popular plugins through the plugin page after selecting any Get \[plugin\] button on the Advanced Work Assignment home page. Plan and configure Advanced Work Assignment \(AWA\).
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
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


