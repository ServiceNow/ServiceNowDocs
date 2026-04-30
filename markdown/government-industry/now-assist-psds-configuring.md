---
title: Install and configure Now Assist for Public Sector Digital Services \(PSDS\)
description: If you have the admin role, you can install and configure the Now Assist for Public Sector Digital Services \(PSDS\) application so that your agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Install and configure Now Assist for Public Sector Digital Services \(PSDS\)

If you have the admin role, you can install and configure the Now Assist for Public Sector Digital Services \(PSDS\) application so that your agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for Public Sector Digital Services \(PSDS\). This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

<table id="table_ipf_bbd_wyb"><thead><tr><th>

Public Sector Digital Services features

</th><th>

Skills

</th></tr></thead><tbody><tr><td>

Chat

</td><td>

-   Chat summarization
-   Chat recommendation
-   Sidebar recommendation

</td></tr><tr><td>

Case

</td><td>

-   Case summarization
-   Resolution notes generation

</td></tr><tr><td>

Search

</td><td>

-   Legislation summarization
-   Search summarization
-   Extract Q&amp;A answers from knowledge base articles upon search

</td></tr></tbody>
</table>**Note:**

Now LLM Service is currently the only provider for this Now Assist application's skills.

To get started with Now Assist, you must install at least one Now Assist application on your instance. The Now Assist Admin console can guide your implementation, starting with installation. Check out the [Now Assist Journey Checklist](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

The following plug-ins and store apps are required for use of Now Assist for Public Sector Digital Services \(PSDS\) and its features, such as AI Search and summarization skills:

-   Now Assist Admin Console \(sn\_nowassist\_admin\)
-   Now Assist for Public Sector Digital Services \(PSDS\) \(sn\_psds\_gen\_ai\)
-   Now Assist for Customer Service Management \(CSM\) \(sn\_csm\_gen\_ai\)
-   Glide Virtual Agent \(com.glide.cs.chatbot\)
-   Glide Conversation Generative Al \(com.glide.cs.genai\)

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

    Some applications might require you to request the app from the ServiceNow® Store first. After you have requested the application from the ServiceNow® Store page, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All** to finish the installation.

7.  Return to the Now Assist Admin console.

8.  In the dialog box, select **Refresh**.


## Result

Your Now Assist Admin console is successfully configured with the necessary plug-ins. Select **View all \(Plugin\) Assists and Skills** to review the features of your new plugin, or close the dialog box to return to the Now Assist Admin console.

## What to do next

[Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) or [Activate a Now Assist Skill.](now-assist-psds-configure-skill.md)

