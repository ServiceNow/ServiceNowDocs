---
title: Get started with Advanced Work Assignment
description: To implement Advanced Work Assignment, complete these initial configuration and setup steps.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Get started with Advanced Work Assignment

To implement Advanced Work Assignment, complete these initial configuration and setup steps.

## Before you begin

Role required: awa\_admin and admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Home**.

2.  Select **Get Advanced Work Assignment plugin** to install the Advanced Work Assignment plugin for your instance.

    The All Applications page opens in a new window or tab.

3.  In the All Applications page, select **Install** and complete the installation prompts.

4.  Go back to the Advanced Work Assignment \(AWA\) home page, and then select **Done** on the Plugin page opened dialog box.

    The AWA home page experience refreshes and the Get targeted routing capabilities section appears.

5.  Select **Get plugin** to activate org-specific IT Service Management \(ITSM\), Customer Service Management, and HR Service Delivery \(HRSD\) plugins.

    The All Applications page opens in a new window or tab.

6.  In the All Applications page, select **Install** and complete the installation prompts.

7.  Go back to the Advanced Work Assignment \(AWA\) home page, and then select **Done** on the Plugin page opened dialog box.

    The AWA home page experience refreshes and the Get the most popular plugins section appears.

8.  Install additional plugins through various ways.

    -   Select **Get plugin** to install popular plugins.
    -   Select the plugin name from the Available Plugins sections.
    The All Applications page opens in a new window or tab.

9.  In the All Applications page, select **Install** and complete the installation prompts.

10. Go back to the Advanced Work Assignment \(AWA\) home page, and then select **Done** on the Plugin page opened dialog box.

    The plugin page opened dialog box only appears when you install plugins from the Get the most popular plugins section.

    The AWA home page experience refreshes and either the Get the most popular plugins section refreshes with the installed plugin or the plugin appears under the Installed Plugins section.

11. In the Essential settings section, select **Set up service channels** to configure the service channels that you activated.

    1.  Create or change an inbox layout.

    2.  Override agent capacity, as needed.

12. In the Essential settings section, select **Set up queues** to create work item queues for your service channels.

    Set the sort order for work items in the queue.

13. In the Essential settings section, select **Set up assignment rules** to configure the work assignment rules used to push work to the appropriate agents.

14. In the Additional settings section, consider configuring the following parameters to improve your AWA functionality.

    1.  Select **Set up presence states** to configure availability states that agents use to indicate whether they can receive work or are offline or away.

    2.  Select **Set up reject reasons** to define the reasons that agents can use to decline work assignments that they receive in their Agent Workspace inbox.

    3.  Select **Set up universal capacity** to configure your team's maximum universal capacity to prevent an agent from being assigned too many work items.

    4.  Select **Set up groups** to create groups of user sets who share a common purpose.

15. In the Advanced settings section, consider configuring the following parameters to improve your AWA functionality.

    **Note:** Advanced settings cards appear conditionally after installing their respective plugin.

    1.  Select **Set up Agent Affinity** to create or change the Agent Affinity rules that route work items in Advanced Work Assignment.

    2.  Select **Set up Shift-based Assignment** to assign work items to agents based on shifts.


-   **[Activate Advanced Work Assignment](awa-activate.md)**  
You can activate the Advanced Work Assignment plugin \(com.glide.awa\) if you have the admin role.
-   **[Activate related plugins for Advanced Work Assignment](../reference/awa-related-plugins.md)**  
After activating the Advanced Work Assignment plugin, activate related AWA plugins to enable other base system service channels and the Performance Analytics Solutions dashboard for AWA.
-   **[Move from Connect Support to Advanced Work Assignment and Agent Chat](migrate-from-connect-support.md)**  
Move from ServiceNow® Connect Support to Agent Chat \(live chat\), which is the messaging system that agents use in Agent Workspace to interact with customers. Moving from Connect Support also involves using Advanced Work Assignment \(AWA\) to create the chat queues for routing chat work items to agents.

**Parent Topic:**[Configuring Advanced Work Assignment](installing-awa.md)

**Related topics**  


[Advanced Work Assignment home page](../concept/awa-admin-console-home.md)

[Install Conversational SMS service channel](install-conversational-sms.md)

[Activate Agent Affinity](awa-activate-agent-affinity.md)

[Activate Conversational Messaging](../../virtual-agent/task/activate-messaging-actions.md)

[Service channels](../concept/awa-service-channels.md)

[Work items](../concept/awa-work-items.md)

[Work assignments](../concept/awa-assignment.md)

[Using Agent Affinity](../concept/awa-agent-affinity-concept.md)

[Agent Inbox controls](../concept/agent-experience.md)

[Advanced Work Assignment Inbox Sentiment display](../concept/awa-inbox-sentiment-display.md)

[Management](../concept/management.md)

[AWA group queue priorities](../concept/awa-group-queue-priorities.md)

[Configure messaging actions](../../virtual-agent/task/configure-messaging-actions.md)

[Enable logging for Advanced Work Assignment](awa-activate-logging.md)

