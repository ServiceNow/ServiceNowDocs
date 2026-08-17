---
title: Install plugins for ServiceNow Otto
description: Install plugins for ServiceNow Otto to enable generative AI on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/install-now-assist-feature-plugins.html
release: australia
topic_type: task
last_updated: "2026-05-20"
reading_time_minutes: 4
keywords: [Install, ServiceNow Otto, plugins, Admin, console, Journey Checklist]
breadcrumb: [Configuring AI skills, AI Admin Hub, Enable AI experiences]
---

# Install plugins for ServiceNow Otto

Install plugins for ServiceNow Otto to enable generative AI on your instance.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

Follow these instructions to get started with AI Admin Hub:

1.  To get started with ServiceNow Otto, you must install at least one generative AI application on your instance.
2.  License any ServiceNow generative AI software from the ServiceNow Store and install it through the Application Manager to access AI Admin Hub.
3.  The AI Admin Hub console guides your implementation, starting with installation.
4.  Check out the [ServiceNow Otto Journey Checklist for more information.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)

## About this task

Deactivate switch in AI Admin Hub

Note, that certain out-of-box skills are automatically enabled by default with plugin activation. You can turn off the toggle switch before installing the plugin to disable the default 'on' setting. With this feature you can prevent skills configured for default activation from auto-activating when installed or updated.

Explore 'View default-active skills' to find the list of skills currently activated by default. You can review them, activate or deactivate them individually. Hidden skills are displayed and accessible within the Additional Details section.

\[Omitted image "activate-plugin-toggle.png"\] Alt text: Deactivate auto activation of skills with product plugins installation

Generative AI applications often function interdependently. ServiceNow Otto Suites help reduce runtime errors and update issues by bundling compatible versions of generative AI applications together during installation and updates.

For more information about how ServiceNow Otto Suites work, see [Now Assist suite versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-suites-app-mgr.md).

For details about available ServiceNow Otto Suites and their compatibility with ServiceNow AI Platform versions, see [Now Assist Suite release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-now-assist-suite-release-notes.html).

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Settings**.

    If you’re already in AI Admin Hub, select the **Settings** tab.

2.  On the **Settings** page, select **Plugins**.

    Plugins appear as cards. Review all ServiceNow Otto plugins on the **Available for you** tab. Plugins that you have already installed appear on the **Installed** tab.

    \[Omitted image "config-now-assist-plugin-card.png"\] Alt text: Example plugin card reads "ServiceNow Otto for Creator: Helping creators build with the power of generative AI." Select Get plugins on the card to install it.

3.  If you don't already have a license for the plugin, request a license from the ServiceNow® Store.

    1.  Select **Get plugins** on the card for the plugin that you want to install.

    2.  In the confirmation window, select **Install Plugin** to open the ServiceNow Store page for the plugin in a new browser tab.

    3.  Request the license.

        For additional information, see [Getting apps and trials from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/getting-apps-trials.md).

4.  Navigate to **Admin** &gt; **Application Manager** &gt; **Available for you**.

5.  Find and select the ServiceNow Otto application you want to install.

6.  Select **Install**.

7.  In the **Select suite version** drop-down menu, select a ServiceNow Otto Suite version.

    The available suite versions are compatible with your instance. If you have other generative AI applications already installed on your instance, they might require update for suite compatibility. For more information about ServiceNow Otto Suite compatibility, see [Now Assist suite versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-suites-app-mgr.md).

    If you haven't installed a ServiceNow Otto Suite version yet, you have the option to choose **none** in the version selector. This option enables you to begin using ServiceNow Otto Suites at a time that works best for your organization.

8.  If you have available application customizations, use the **Customized ver.** drop-down menu to select which customization to use.

    Your customizations might not be compatible with a new application version. Update the application in a non-production instance, then make any necessary changes to your customization and validate compatibility before making updates in production instances. For more information about managing customizations, see [Manage customizations to applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/manage-customizations-store-apps.md).

9.  Include demo data if it's desired and available.

    1.  Select the option to install demo data next to each ServiceNow Otto application you want demo data for.

        The option to install demo data isn't available for all applications.

    2.  Turn on the **Load demo data for selected apps** toggle switch.

10. Select **Continue** to review the installation details.

    If any applications display "Installation blocked," it means that application version isn't licensed yet. Either uninstall the application or license the required version.

11. Install the application now or schedule installation for a later time.

<table><thead><tr><th align="left" id="d113992e455">

Installation option

</th><th align="left" id="d113992e458">

Procedure

</th></tr></thead><tbody><tr><td id="d113992e464">

**Install now**

</td><td>

1.  Leave the default option to **Install now** selected.
2.  Select **Install**.


</td></tr><tr><td id="d113992e488">

**Install later**

</td><td>

1.  Select the option to **Install later**.
2.  Enter a start date and start time.
3.  Select **Schedule**.


</td></tr></tbody>
</table>12. Return to the AI Admin Hub console.

13. In the dialog box, select **Refresh**.

14. Either close the dialog box to review all of your plugins or select **View all \(Plugin\) Assists and Skills** to review the features of your new plugin.


## Result

Your plugin is successfully installed.

If you encounter issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) for steps that may address your issue. Otherwise, you can make a Support case.

## What to do next

[Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md) or [Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-a-now-assist-skill.md).

