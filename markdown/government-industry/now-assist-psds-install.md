---
title: Install Now Assist for Public Sector Digital Services \(PSDS\)
description: Install required plugins and enable Now Assist for Public Sector Digital Services \(PSDS\) to configure and use generative AI skills in Configurable Workspace, Playbooks, and Core UI.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Install Now Assist for Public Sector Digital Services \(PSDS\)

Install required plugins and enable Now Assist for Public Sector Digital Services \(PSDS\) to configure and use generative AI skills in Configurable Workspace, Playbooks, and Core UI.

## Before you begin

Role required: admin

The following plug-ins and store apps are required for use of Now Assist for Public Sector Digital Services \(PSDS\) and its features, such as AI Search and summarization skills:

-   Now Assist Admin Console \(sn\_nowassist\_admin\)
-   Now Assist for Public Sector Digital Services \(PSDS\) \(sn\_psds\_gen\_ai\)
-   Now Assist for Customer Service Management \(CSM\) \(sn\_csm\_gen\_ai\)
-   Glide Virtual Agent \(com.glide.cs.chatbot\)
-   Glide Conversation Generative Al \(com.glide.cs.genai\)

## About this task

**Note:**

Now LLM Service is currently the only provider for this Now Assist application's skills.

To get started with Now Assist, you must install at least one Now Assist application on your instance. The Now Assist Admin console can guide your implementation, starting with installation. Use the Now Assist Admin console to configure Now Assist for Public Sector Digital Services \(PSDS\). This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US), as well as the [Now Assist Journey Checklist](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

For information about CSM Configurable Workspace, see [Set up CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-config-workspace-set-up&version=australia&pubname=australia-customer-service-management&ft:locale=en-US). For information about Now Assist AI agents, see [Install Now Assist AI Agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

To access AI agents in the Now Assist panel, you need to [turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) .

To install the Now Assist for PSDS plugin \(sn\_psds\_gen\_ai\), follow the procedure below.

## Procedure

1.  Install the Now Assist for Public Sector Digital Services \(PSDS\) plugin \(com.sn\_psds\_gen\_ai\).

2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

    If you’re already in Now Assist Admin, select the **Settings** tab.

3.  On the **Settings** page, select **Plugins**.

    Plugins appear as cards. Review all Now Assist plugins on the **Available for you** tab. Plugins that you have already installed appear on the **Installed** tab.

    ![Example plugin card reads "Now Assist for Public Sector Digital Services (PSDS): GenAl related features for Public Sector Digital Services that are powered by Now Assist." Select Get plugins on the card to install it.](../image/na-psds-plugin-card-config.png)

4.  Select **Get plugins** on the Now Assist for Customer Service Management \(CSM\) and Now Assist for Public Sector Digital Services \(PSDS\) cards.

5.  In the confirmation window, select **Install Plugin** to open the ServiceNow Store page for the plugin in a new browser tab.

6.  Install the plugin from the ServiceNow Store page.

    Some applications may require you to request the app from the ServiceNow® Store first. After you've requested the application from the ServiceNow® Store page, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All** to finish the installation.

7.  Return to the Now Assist Admin console.

8.  In the dialog box, select **Refresh**.

    For more detailed information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


## Result

Your Now Assist Admin console is successfully configured with the necessary plug-ins. Select **View all \(Plugin\) Assists and Skills** to review the features of your new plugin, or close the dialog box to return to the Now Assist Admin console.

## What to do next

[Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)or [Activate a Now Assist Skill.](../concept/now-assist-psds-configure-skill.md)

