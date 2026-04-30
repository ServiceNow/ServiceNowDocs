---
title: Advanced Work Assignment home page
description: Explore, implement, and maintain ServiceNow Advanced Work Assignment using a home-page experience. Discover AWA, install relevant plugins, and configure settings for AWA through the Advanced Work Assignment home page available to admins.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Advanced Work Assignment home page

Explore, implement, and maintain ServiceNow® Advanced Work Assignment using a home-page experience. Discover AWA, install relevant plugins, and configure settings for AWA through the Advanced Work Assignment home page available to admins.

## Advanced Work Assignment home page advantages

The Advanced Work Assignment home page makes it easy for you to get started and work toward achieving positive outcomes with your implementation. The Advanced Work Assignment home is ideal for first-time users who have never installed or configured Advanced Work Assignment \(AWA\), to experienced users looking to expand capabilities and maintain existing implementations.

AWA home provides the following features:

-   Cards that guide you through the order of essential settings, like creating service channels, configuring queues, and adding assignment rules. Cards that redirect you to additional and advanced settings, such as configuring presence states, setting up reject reasons, determining universal capacity, setting up agent affinity, and establishing shift-based assignments.
-   Lists of installed and available plugins.
-   Quickly install plugins through the plugin page. The plugin page appears in either a new window or tab after selecting any **Get \[plugin\]** button. The plugin page opened dialog box appears on the home page, where you can select **Not Now** to continue with your current home page experience or **Done** to refresh the home page after your plugin's installation.
-   Access to helpful resources and videos to help you learn more about configuring and managing AWA.

Navigate to **Advanced Work Assignment** &gt; **Home** to start exploring AWA features.

**Important:** The AWA home page appears after you have installed and updated the Omni-Experience Standard Feature Set to the latest version through the ServiceNow Store. Existing customers don't need to install it from the store. However, subsequent updates are available there. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Planning, installing, and exploring AWA

If you've never installed AWA, the Advanced Work Assignment home page prompts you to do so first. Before implementing AWA, take some time to reflect on a few important questions in the Think through these questions with your team Think through these questions with your team list. These questions are meant to help you envision the AWA experience that you need and want for your business. Expand the available questions to explore more thoughtful considerations, such as what queues would work best for your team and what skills does your team have.

The layout of the home page may vary, depending on which features you've installed and configured.

-   **First, install the required plugin**

    Install the Advanced Work Assignment plugin to begin. Select **Get Advanced Work Assignment plugin** to install it.

    **Note:** Only users with the sys\_admin role can install a plugin from the Advanced Work Assignment home page. For example, if a user with the awa\_admin role tried to install the Advanced Work Assignment plugin, they're prompted to contact their administrator for installation. After the Advanced Work Assignment plugin is installed, all AWA home page options are available in the application navigator for users with the admin and awa\_admin roles.

    ![Install AWA from the Advanced Work Assignment home page](../image/awa-home-install-awa-plugin.png)

-   **Get targeted routing capabilities**

    Activate org-specific AWA plugins through the **Get plugin** button to route work items to the right agents for ServiceNow® IT Service Management \(ITSM\), ServiceNow® Customer Service Management, and ServiceNow® HR Service Delivery \(HRSD\) plugins. These plugins enable org-specific service channels in AWA including configured data and demo data.

    ![Get targeted routing capabilities three plugin options](../image/awa-home-get-targeted-routing-capabilities.png)

-   **Get the most popular plugins**

    After installing any of the targeted routing capabilities plugins, install these popular plugins to boost your AWA experience.

    -   Agent Chat: The Agent Chat plugin enables the Chat service channel in AWA and chat monitoring in Agent Workspace.
    -   Walk-up Experience: The Walk-up Experience plugin activates the walk-up contact service channel for pre-built technology lounges.
    -   Performance Analytics: The Performance Analytics plugin activates the Performance Analytics Content Pack for AWA.
    ![Get the most popular plugins after installing targeted routing capabilities plugins](../image/awa-home-get-popular-plugins.png)

-   **Watch and learn**

    Watch the embedded AWA implementation guide for more information about installing and implementing AWA directly from the right side of the home page.

-   **Helpful Resources**

    Explore the helpful AWA resources such as release notes, product documentation, and ServiceNow Community forums and content directly from the right side of the home page. These resources give you information to understand the configuration process and the benefits of setting up AWA features.

-   **Installed Plugins**

    View a list of installed plugins. Admin role users can select a plugin's link to have that application's plugins page appear in a separate window or tab.

-   **Available Plugins**

    View a list of available plugins that help save time setting up AWA. Admin role users can select a plugin's link to have that application's plugins page or ServiceNow Store site appear in a separate window or tab. Awa\_admin role users can view a store app's plugin page to learn about the plugin, but only admin role users can install plugins.


## Configuring essential AWA settings

Follow the order of the guided configuration setup to establish your AWA settings in the most logical order.

|Card|Feature|Description|
|----|-------|-----------|
|![Set up service channels in the AWA home page](../image/awa-home-create-service-channels.png)|[Create Service Channels](../task/awa-create-service-channel.md)|Give customer support by automatically routing incoming work to agents through service channels. Service channels assign a specific type and scope of work to agents.|
|![Set up queues in the AWA home page](../image/awa-home-configure-work-item-queues.png)|[Configure work item queues](../task/awa-create-queue.md)|Determine routing conditions and destinations for queues.|
|![Set up assignment rules in the AWA home page](../image/awa-home-add-assignment-rules.png)|[Add assignment rules](../task/awa-create-assignment-rule.md)|Establish assignment criteria to agents who either have gone the longest without being assigned a work item, have the most work availability, or have the needed skills.|

## Configuring additional and advanced AWA settings

The additional card settings expand your organization's ability to maximize productivity with AWA.

<table id="table_rks_5pm_jvb"><thead><tr><th>

Card

</th><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Set up presence states in the AWA home page](../image/awa-home-customize-presence-states.png)

</td><td>

[Customize presence states](../task/awa-configure-agent-presence.md)

</td><td>

Configure availability states that agents use to indicate whether they can receive work or are offline or away.

</td></tr><tr><td>

![Set up reject reasons in the AWA home page](../image/awa-home-configure-reject-reasons.png)

</td><td>

[Configure reasons for rejections](../task/awa-configure-reject-reasons.md)

</td><td>

Define the reasons that agents can use to decline work assignments that they receive in their Agent Workspace inbox.

</td></tr><tr><td>

![Set up universal capacity in the AWA home page](../image/awa-home-determine-agent-capacity.png)

</td><td>

[Determine agent capacity](../task/awa-universal-capacity.md)

</td><td>

Configure your team's maximum universal capacity to prevent an agent from being assigned too many work items. If the agent's maximum universal capacity has been reached, additional work items aren't assigned to the agent.

</td></tr><tr><td>

Select **See More** to view this card.

 ![Set up groups in the AWA home page](../image/awa-home-define-assignment-group.png)

</td><td>

[Define assignment groups](../task/awa-groups.md)

</td><td>

Create groups of user sets who share a common purpose.

</td></tr></tbody>
</table>Advanced settings cards appear conditionally after installing their respective plugin.

<table id="table_sld_cqm_jvb"><thead><tr><th>

Card

</th><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Set up Agent Affinity in the AWA home page](../image/awa-home-advanced-agent-affinity.png)

</td><td>

[Set up Agent Affinity](../task/awa-configure-agent-affinity.md)

</td><td>

Install the Agent Affinity plugin for this card to conditionally appear. Create or change the Agent Affinity rules that route work items in Advanced Work Assignment.

</td></tr><tr><td>

![Set up Shift-based Assignment in the AWA home page](../image/awa-home-advanced-shift-based-assignment.png)

</td><td>

[Set up shift-based assignment](../task/awa-create-assignment-rule.md)

</td><td>

Install either one or both of the following plugins for this card to conditionally appear:

-   Workforce Optimization for Customer Service
-   Workforce Optimization for ITSM

 Assign work items to agents based on shifts.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Advanced Work Assignment](../task/installing-awa.md)

**Related topics**  


[Get started with Advanced Work Assignment](../task/implement-awa.md)

[Install Conversational SMS service channel](../task/install-conversational-sms.md)

[Activate Agent Affinity](../task/awa-activate-agent-affinity.md)

[Activate Conversational Messaging](../../virtual-agent/task/activate-messaging-actions.md)

[Service channels](awa-service-channels.md)

[Work items](awa-work-items.md)

[Work assignments](awa-assignment.md)

[Using Agent Affinity](awa-agent-affinity-concept.md)

[Agent Inbox controls](agent-experience.md)

[Advanced Work Assignment Inbox Sentiment display](awa-inbox-sentiment-display.md)

[Management](management.md)

[AWA group queue priorities](awa-group-queue-priorities.md)

[Configure messaging actions](../../virtual-agent/task/configure-messaging-actions.md)

[Enable logging for Advanced Work Assignment](../task/awa-activate-logging.md)

