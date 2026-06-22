---
title: Install Now Assist plugins
description: Install Now Assist plugins to enable generative AI on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-05-20"
reading_time_minutes: 4
keywords: [Install, Now Assist, plugins, Admin, console, Journey Checklist]
breadcrumb: [Configuring Now Assist Admin features, Now Assist, Enable AI experiences]
---

# Install Now Assist plugins

Install Now Assist plugins to enable generative AI on your instance.

## Before you begin

Role required: admin

Follow these instructions to get started with Now Assist Admin:

1.  To get started with Now Assist, you must install at least one Now Assist application on your instance.
2.  License any Now Assist software from the ServiceNow Store and install it through the Application Manager to access Now Assist Admin.
3.  The Now Assist Admin console guides your implementation, starting with installation.
4.  Check out the [Now Assist Journey Checklist for more information.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configuring-now-assist.md)

## About this task

Now Assist applications often function interdependently. Now Assist Suites help reduce runtime errors and update issues by bundling compatible versions of Now Assist applications together during installation and updates.

For more information about how Now Assist Suites work, see [Now Assist suite versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/now-assist-suites-app-mgr.md).

For details about available Now Assist Suites and their compatibility with ServiceNow AI Platform versions, see [Now Assist Suite release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-now-assist-suite-release-notes.html).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

    If you’re already in Now Assist Admin, select the **Settings** tab.

2.  On the **Settings** page, select **Plugins**.

    Plugins appear as cards. Review all Now Assist plugins on the **Available for you** tab. Plugins that you have already installed appear on the **Installed** tab.

    \[Omitted image "config-now-assist-plugin-card.png"\] Alt text: Example plugin card reads "Now Assist for Creator: Helping creators build with the power of Generative AI." Select Get plugins on the card to install it.

3.  If you don't already have a license for the plugin, request a license from the ServiceNow® Store.

    1.  Select **Get plugins** on the card for the plugin that you want to install.

    2.  In the confirmation window, select **Install Plugin** to open the ServiceNow Store page for the plugin in a new browser tab.

    3.  Request the license.

        For additional information, see [Getting apps and trials from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/getting-apps-trials.md).

4.  Navigate to **Admin** &gt; **Application Manager** &gt; **Available for you**.

5.  Find and select the Now Assist application you want to install.

6.  Select **Install**.

7.  In the **Select suite version** drop-down menu, select a Now Assist Suite version.

    The available suite versions are compatible with your instance. If you have other Now Assist applications already installed on your instance, they might require update for suite compatibility. For more information about Now Assist Suite compatibility, see [Now Assist suite versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/now-assist-suites-app-mgr.md).

    If you haven't installed a Now Assist Suite version yet, you have the option to choose **none** in the version selector. This option enables you to begin using Now Assist Suites at a time that works best for your organization.

8.  If you have available application customizations, use the **Customized ver.** drop-down menu to select which customization to use.

    Your customizations might not be compatible with a new application version. Update the application in a non-production instance, then make any necessary changes to your customization and validate compatibility before making updates in production instances. For more information about managing customizations, see [Manage customizations to applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/application-repository-self-hosted/manage-customizations-store-apps.md).

9.  Include demo data if it's desired and available.

    1.  Select the option to install demo data next to each Now Assist application you want demo data for.

        The option to install demo data isn't available for all applications.

    2.  Turn on the **Load demo data for selected apps** toggle switch.

10. Select **Continue** to review the installation details.

    If any applications display "Installation blocked," it means that application version isn't licensed yet. Either uninstall the application or license the required version.

11. Install the application now or schedule installation for a later time.

<table><thead><tr><th align="left" id="d37147e446">

Installation option

</th><th align="left" id="d37147e449">

Procedure

</th></tr></thead><tbody><tr><td id="d37147e455">

**Install now**

</td><td>

1.  Leave the default option to **Install now** selected.
2.  Select **Install**.


</td></tr><tr><td id="d37147e479">

**Install later**

</td><td>

1.  Select the option to **Install later**.
2.  Enter a start date and start time.
3.  Select **Schedule**.


</td></tr></tbody>
</table>12. Return to the Now Assist Admin console.

13. In the dialog box, select **Refresh**.

14. Either close the dialog box to review all of your plugins or select **View all \(Plugin\) Assists and Skills** to review the features of your new plugin.


## Result

Your plugin is successfully installed.

If you encounter issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) for steps that may address your issue. Otherwise, you can make a Support case.

## What to do next

[Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/activate-now-assist-panel.md) or [Activate a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configure-a-now-assist-skill.md).

