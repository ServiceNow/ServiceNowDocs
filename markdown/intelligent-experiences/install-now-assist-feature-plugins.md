---
title: Install AI plugins in AI Admin Hub
description: Install plugins in AI Admin Hub to enable AI applications on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/install-now-assist-feature-plugins.html
release: australia
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 5
keywords: [Install, ServiceNow Otto, plugins, Admin, console, Journey Checklist]
breadcrumb: [Configuring plugins and skills in AI Admin Hub, AI Admin Hub, Generative AI skills, Enable AI Experiences]
---

# Install AI plugins in AI Admin Hub

Install plugins in AI Admin Hub to enable AI applications on your instance.

## Before you begin

-   To use AI Admin Hub, you must install at least one AI application on your instance. License any ServiceNow generative AI software from the ServiceNow Store and install it through the Application Manager. For more information, see the [ServiceNow Otto Journey Checklist.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/configuring-now-assist.md)
-   Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

**Note:** Starting with the Brazil release, AI Admin Hub is being prepared for deprecation and replacement by [AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-landing-page.md). Everything you manage here is available in AI Admin Center, plus more tools to manage and get the most from AI. You can continue to use AI Admin Hub for a limited time during the transition. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Installing plugins may automatically activate some skills contained in the plugins. You can control this skill activation behavior by using the toggle switch **Default activation of out-of-box skills** on the Plugins tab.

-   The default setting for the toggle switch is on. This setting means that some skills may be automatically activated when their plugins are installed.
-   If you turn off this toggle switch, no skills are automatically activated when plugins are installed. \(You can choose to activate skills later\).
-   Select the **View default-active skills** option to open a modal window that lists automatically activated skills. On this modal window you can review and activate \(or deactivate\) individual skills. Hidden skills are displayed and accessible within the Additional Details section.

To activate a skill separately, see [Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/configure-a-now-assist-skill.md).

\[Omitted image "activate-plugin-toggle.png"\] Alt text: The Plugins page of the Settings tab of AI Admin Hub. The toggle switch titled "Default activation of out-of-box skills" is set to on. Two example plugin cards are displayed.

AI applications often function interdependently. AI Suites help reduce runtime errors and update issues by bundling compatible versions of AI applications together during installation and updates. For more information, see [AI Suites versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-suites-app-mgr.md) and [AI Suites release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-now-assist-suite-release-notes.html).

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Settings**.

    If you’re already in AI Admin Hub, select the **Settings** tab.

2.  On the **Settings** tab, select **Plugins** on the navigation panel.

    Plugins appear as cards. Review all AI plugins on the **Available for you** tab. Plugins that you have already installed appear on the **Installed** tab.

    \[Omitted image "config-now-assist-plugin-card.png"\] Alt text: Example plugin card reads "ServiceNow Otto for Creator: Helping creators build with the power of Generative AI."

3.  If you don't already have a license for the plugin, request a license from the ServiceNow® Store.

    1.  Select **Get plugins** on the card for the plugin that you want to install.

    2.  In the confirmation window, select **Install Plugin** to open the ServiceNow Store page for the plugin in a new browser tab.

    3.  Request the license.

        For additional information, see [Getting apps and trials from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/getting-apps-trials.md).

4.  Navigate to **Admin** &gt; **Application Manager** &gt; **Available for you**.

5.  Find and select the AI application you want to install.

6.  Select **Install**.

7.  In the **Select suite version** drop-down menu, select an AI Suite version.

    The available AI Suites versions are compatible with your instance. If you have other AI applications already installed on your instance, they might require update for suite compatibility. For more information about AI Suites compatibility, see [AI Suites versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-suites-app-mgr.md).

    If you haven't installed an AI Suites version yet, you have the option to choose **none** in the version selector. This option enables you to begin using AI Suites at a time that works best for your organization.

8.  If you have available application customizations, use the **Customized ver.** drop-down menu to select which customization to use.

    Your customizations might not be compatible with a new application version. Update the application in a non-production instance, then make any necessary changes to your customization and validate compatibility before making updates in production instances. For more information about managing customizations, see [Manage customizations to applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/manage-customizations-store-apps.md).

9.  Include demo data if desired and available.

    1.  Select the option to install demo data next to each application you want demo data for.

        The option to install demo data isn't available for all applications.

    2.  Turn on the **Load demo data for selected apps** toggle switch.

10. Select **Continue** to review the installation details.

    Any applications displaying **Installation blocked** aren't licensed yet. Either uninstall the application or license the required version.

11. Install the application now or schedule installation for a later time.

<table><thead><tr><th align="left" id="d142094e463">

Installation option

</th><th align="left" id="d142094e466">

Procedure

</th></tr></thead><tbody><tr><td id="d142094e472">

**Install now**

</td><td>

1.  Leave the default option to **Install now** selected.
2.  Select **Install**.


</td></tr><tr><td id="d142094e496">

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

If you encounter issues installing or updating applications, see this [knowledge article \(KB1637452\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) for steps that may address your issue. Alternatively, you can submit a Support case.

## What to do next

[Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/activate-now-assist-panel.md) or [Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/configure-a-now-assist-skill.md).

