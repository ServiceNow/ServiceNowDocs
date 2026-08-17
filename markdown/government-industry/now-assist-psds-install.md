---
title: Install ServiceNow Otto for Public Sector Digital Services \(PSDS\)
description: Install required plugins and enable ServiceNow Otto for Public Sector Digital Services \(PSDS\) to configure and use generative AI skills in Configurable Workspace, Playbooks, and Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/now-assist-psds-install.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, ServiceNow Otto for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Install ServiceNow Otto for Public Sector Digital Services \(PSDS\)

Install required plugins and enable ServiceNow Otto for Public Sector Digital Services \(PSDS\) to configure and use generative AI skills in Configurable Workspace, Playbooks, and Core UI.

## Before you begin

Role required: admin

The following plug-ins and store apps are required for use of ServiceNow Otto for Public Sector Digital Services \(PSDS\) and its features, such as AI Search and summarization skills:

-   AI Admin Hub Console
-   ServiceNow Otto for Public Sector Digital Services \(PSDS\) \(sn\_psds\_gen\_ai\)
-   ServiceNow Otto for Customer Service Management \(CSM\) \(sn\_csm\_gen\_ai\)
-   Glide Virtual Agent \(com.glide.cs.chatbot\)
-   Glide Conversation Generative Al \(com.glide.cs.genai\)

## About this task

**Note:**

Now LLM Service is currently the only provider for this application's skills.

To get started with ServiceNow Otto, you must install at least one ServiceNow Otto application on your instance. The AI Admin Hub can guide your implementation, starting with installation. Use the AI Admin Hub console to configure ServiceNow Otto for Public Sector Digital Services \(PSDS\). This console contains everything that you must install the plugins and configure the generative AI skills. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md), and the [ServiceNow Otto Journey Checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

For information about CSM Configurable Workspace, see [Set up CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-config-workspace-set-up.md). For information about AI agents, see [Install AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-ai-agents-plugins.md).

To access AI agents in the ServiceNow Otto panel, you must [turn on the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md) and ensure that case summarization is active.

To install the ServiceNow Otto for PSDS plugin \(sn\_psds\_gen\_ai\), follow the procedure:

## Procedure

1.  Install the ServiceNow Otto for Public Sector Digital Services \(PSDS\) plugin \(com.sn\_psds\_gen\_ai\).

2.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Settings**.

    If you’re already in AI Admin Hub, select the **Settings** tab.

3.  On the **Settings** page, select **Plugins**.

    Plugins appear as cards. Review all ServiceNow Otto plugins on the **Available for you** tab. Plugins that you have already installed appear on the **Installed** tab.

4.  Select **Get plugins** on the ServiceNow Otto for Customer Service Management \(CSM\) and ServiceNow Otto for Public Sector Digital Services \(PSDS\) cards.

5.  In the confirmation window, select **Install Plugin** to open the ServiceNow Store page for the plugin in a new browser tab.

6.  Install the plugin from the ServiceNow Store page.

    Some applications may require you to request the app from the ServiceNow® Store first. After you've requested the application from the ServiceNow® Store page, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All** to finish the installation.

7.  Return to the AI Admin Hub console.

8.  In the dialog box, select **Refresh**.

    For more detailed information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).


## Result

Your AI Admin Hub console is successfully configured with the necessary plug-ins. Select **View all \(Plugin\) Assists and Skills** to review the features of your new plugin, or close the dialog box to return to the AI Admin Hub console.

## What to do next

[Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md)or [Activate a ServiceNow Otto Skill.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/now-assist-psds-configure-skill.md)

