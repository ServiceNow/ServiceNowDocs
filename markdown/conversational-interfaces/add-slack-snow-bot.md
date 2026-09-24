---
title: Integrate Virtual Agent with Slack
description: Add the Virtual Agent bot to your ServiceNow instance to integrate with Slack.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/add-slack-snow-bot.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Virtual Agent, Slack, Conversational Integration, sn\_va\_slack]
breadcrumb: [Integrate Virtual Agent with Slack, Slack, Integrate VA with messaging apps, Conversational Integration apps for Virtual Agent, Conversational Interfaces]
---

# Integrate Virtual Agent with Slack

Add the Virtual Agent bot to your ServiceNow® instance to integrate with Slack.

## Before you begin

Ensure that you have installed the Conversational Integration with Slack plugin \(sn\_va\_slack\) on your instance before adding any integrations.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, select **View All**.

    The Channels and integrations page opens.

3.  Under the Available Channels section in the Slack tile, select **Add Integrations**, and select **Integrate with ServiceNow Virtual Agent**.

    **Note:** The **Add Integrations** drop-down is available only after installing the Conversational Integration with Slack plugin \(sn\_va\_slack\) on your ServiceNow instance.

    \[Omitted image "add-slack-snow-integ.png"\] Alt text: Slack Add integration drop-down list. The Integrate with ServiceNow Virtual Agent option is highlighted.

4.  Enter your Slack workspace URL to sign into your Slack workspace, and select **Continue**.

    \[Omitted image "sign-into-slack-workspace.png"\] Alt text: Enter your workspace URL to sign in.

    **Note:** Ensure that you input the name of the Slack workspace for which you have access.

5.  Sign in to your ServiceNow® instance.

6.  Select **Allow** when Slack requests permission to access your workspace.

    \[Omitted image "va-request-permission.png"\] Alt text: Logging into the Slack workspace to integrate with your Now Virtual Agent requires you to accept the requested permissions to access the workspace.

7.  If the selected workspace has already been assigned to Virtual Agent, you must first uninstall from the previously associated instance.

    **Note:**

    Starting with the Utah release, if your Slack workspace is already associated with another ServiceNow instance, but you intend to associate it with a new instance, then you must reach out to the administrator to first uninstall it from the previously associated instance. For more information, see [Associate a Slack integration with a different instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/override-slack-install.md).

    \[Omitted image "slack-new-proceed-install.png"\] Alt text: A message appears when the Slack workspace is already associated with a ServiceNow instance.

    When Virtual Agent has been successfully installed on the Slack workspace, a completion message appears.

8.  Select **Go to Slack** to manage the Slack app.

9.  Select **Continue to manage channels and integrations** to manage the integration on your ServiceNow instance.

    The Slack application appears in the list of integrations.


## What to do next

If you want to integrate your ServiceNow instance with another Slack bot, select the plus icon in the Virtual Agent tile, or select the **Add integration** list on the Manage Slack channel page.

\[Omitted image "add-integration-icon-slck.png"\] Alt text: Manage Slack channel view in Conversational Interfaces General settings. The plus icon in the Virtual Agent tile and the Add Integration list are highlighted..

For more information, see [Manage the Virtual Agent integration with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-va-slack.md).

**Parent Topic:**[Integrating Virtual Agent with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-integ-slack.md)

