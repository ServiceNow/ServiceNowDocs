---
title: Integrate ServiceNow Virtual Agent with Slack
description: Add the Virtual Agent bot to your ServiceNow instance to integrate with Slack.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Virtual Agent, Slack, Conversational Integration, sn\_va\_slack]
breadcrumb: [Integrating ServiceNow Virtual Agent with Slack, Integrating Virtual Agent with Slack, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrate ServiceNow Virtual Agent with Slack

Add the Virtual Agent bot to your ServiceNow® instance to integrate with Slack.

## Before you begin

Ensure that you have installed the Conversational Integration with Slack plugin \(sn\_va\_slack\) on your ServiceNow instance before adding any integrations.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, select **View All**.

    The Channels and integrations page opens.

3.  Under the Available Channels section in the Slack tile, select **Add Integrations**, and select **Integrate with ServiceNow Virtual Agent**.

    **Note:** The **Add Integrations** drop-down is available only after installing the Conversational Integration with Slack plugin \(sn\_va\_slack\) on your ServiceNow instance.

    ![Slack Add integration drop-down list. The Integrate with ServiceNow Virtual Agent option is highlighted.](../images/add-slack-snow-integ.png)

4.  Enter your Slack workspace URL to sign into your Slack workspace, and select **Continue**.

    ![Enter your workspace URL to sign in.](../images/sign-into-slack-workspace.png)

    **Note:** Ensure that you input the name of the Slack workspace for which you have access.

5.  Sign in to your ServiceNow® instance.

6.  Select **Allow** when Slack requests permission to access your workspace.

    ![Logging into the Slack workspace to integrate with your Now Virtual Agent requires you to accept the requested permissions to access the workspace.](../images/va-request-permission.png)

7.  If the selected workspace ant has already been assigned to Virtual Agent, you must first uninstall from the previously associated instance.

    **Note:**

    Starting from Utah release, if your Slack workspace is already associated with another ServiceNow instance, but if you intend to associate it with a new instance, then you're asked to reach out to the administrator to first uninstall it from the previously associated instance. For more information, see [Override Slack integration](override-slack-install.md).

    ![A message appears when the Slack workspace is already associated with a ServiceNow instance.](../images/slack-new-proceed-install.png)

    When Virtual Agent has been successfully installed on the Slack workspace, a completion message appears.

8.  Select **Go to Slack** to manage the Slack app.

9.  Select **Continue to manage channels and integrations** to manage the integration on your ServiceNow instance.

    The Slack application appears in the list of integrations.


## What to do next

If you would like to integrate your ServiceNow instance with another Slack bot, select the plus icon in the ServiceNow Virtual Agent tile, or select the **Add integration** list on the Manage Slack channel page.

![Manage Slack channel view in Conversational Interfaces General settings. The plus icon in the ServiceNow Virtual Agent tile and the Add Integration list are highlighted.](../images/add-integration-icon-slck.png).

For more information, see [Manage the ServiceNow Virtual Agent integration with Slack](configure-va-slack.md).

**Parent Topic:**[Integrating ServiceNow Virtual Agent with Slack](../concept/va-integ-slack.md)

