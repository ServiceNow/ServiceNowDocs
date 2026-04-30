---
title: Install Atlassian Jira Integration for Agile Development
description: Install the Atlassian Jira Integration for Agile Development \(sn\_agile\_jira\_int\) application v2.0.1 from ServiceNow Store.
locale: en-US
release: zurich
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Atlassian Jira Integration for Agile Development, Integrate, Agile Development 2.0, Strategic Portfolio Management]
---

# Install Atlassian Jira Integration for Agile Development

Install the Atlassian Jira Integration for Agile Development \(sn\_agile\_jira\_int\) application v2.0.1 from ServiceNow Store.

## Before you begin

Ensure that the application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Complete the following setup tasks for a smooth installation and configuration.

1.  Navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.
2.  Verify that Agile Development 2.0 \(com.snc.sdlc.agile.2.0\) is activated.
3.  Verify that ServiceNow Integration Hub Starter Pack Installer \(com.glide.hub.integrations\) is activated.
4.  Verify that Jira Spoke 2.6.8 \(sn\_jira\_spoke\) is activated.
5.  Verify that Integrations - External Authentication Framework \(com.glide.external.app\) is activated.

Role required: admin

**Note:** Activation of the Agile Development 2.0, ServiceNow Integration Hub Starter Pack Installer, Jira Spoke, and Integrations - External Authentication Framework plugins on production instances may require separate licenses. Contact ServiceNow Customer Support for details.

## Procedure

1.  Navigate to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9e8488a8c703330024f6612827c2601b/2.1.0?referer=/store/search?listingtype=allintegrations%253Bancillary_app%253Bcertified_apps%253Bcontent%253Bindustry_solution%253Boem&q=atlassian%20jira%20integration%20for%20agile&sl=sh).

2.  In the ServiceNow Store, search for Atlassian Jira Integration for Agile Development.

3.  Click the application tile.

    You can view detailed information about the application. Consider reading the Other Requirements and Dependencies sections, as applicable.

4.  Click **Get** and enter your Now Support login credentials.

5.  Click **Request Install**.

6.  In the **Instance Name** field, enter your details and click **Validate Instance**.

7.  In the **Reason for the Instance** field, enter your details and click **Request**.

    You receive an email with detailed installation instructions.

8.  Log in to the instance on which you want to install the Atlassian Jira Integration for Agile Development application.

9.  Select **System Applications** &gt; **All Available Applications** &gt; **All**.

10. Locate the application using the filter criteria and search bar, select it, and click **Install**.


## Result

The following components are installed with installation of the application:

-   Roles
-   Scheduled Jobs
-   Tables

For more information, see [Components installed with Atlassian Jira integration for Agile Development](components-installed-with-atlassian-jira-integration-for-agile-development.md).

