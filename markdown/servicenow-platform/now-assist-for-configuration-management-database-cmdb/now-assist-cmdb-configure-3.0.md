---
title: Configure Now Assist for CMDB 3.0
description: Configure the Now Assist for CMDB application so users can benefit from Agentic workflows, agents, and skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configure-3.0.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Now Assist for CMDB 3.0

Configure the Now Assist for CMDB application so users can benefit from Agentic workflows, agents, and skills.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin** and then select the **Settings** tab.

2.  In the list, select **Plugins**.

    Plugins that have already been activated are listed on the **Installed** tab.

3.  Uninstall Now Assist for Service Graph Connectors \(SGC\).

4.  On the Now Assist for Configuration Management Database \(CMDB\) card, select **Get plugins** and then in the pop-up window, select **Install Plugin**.

    You install the Now Assist for CMDB \(com.snc.cmdb.gen.ai\) plugin.

    \[Omitted image "na-cmdb-plugins-install-page.png"\] Alt text: Accessing the Now Assist for CMDB \(com.snc.cmdb.gen.ai\) plugin from the Now Assist Admin console.

    You're redirected to the ServiceNow Store in a new browser tab so you can get the plugin.

5.  Install the Now Assist for CMDB plugin.

    For instructions on the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

6.  Confirm that Now Assist for CMDB is installed.

    1.  On the **Now Assist Admin** console, select the **Settings** tab and then select **Plugins** in the list.

    2.  On the **Installed** tab, verify that the **Status** value is **Installed**.

        \[Omitted image "na-cmdb-plugin-installed.png"\] Alt text: Verifying that the plugin is installed.

    Now that you have installed the plugin, you set up the skills for Now Assist for CMDB.

7.  On the **Now Assist Skills** tab, expand **Technology** and then select **CMDB**.

    \[Omitted image "na-cmdb-turn-on-skill-page.png"\] Alt text: Activating the Now Assist for CMDB skills.

8.  Configure property settings.

    See [Property settings for Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-data-fdn-properties.md).


## What to do next

To start using Now Assist for CMDB skills, see [Using Now Assist skills in Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using-skills.md).

To deactivate a skill, select the menu icon \[Omitted image "menu-icon.png"\] Alt text:for the skill and then select **Deactivate skill**.

Admins might be interested in Query Generation. Query Generation is an AI-powered service that translates user questions into an executable query. An executable query contains the data source, filter, aggregation, and visualization instructions that best answer the user's question. For more information, see [Exploring Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/exploring-query-generation.md).

**Parent Topic:**[Configuring Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

**Related topics**  


[CMDB Workspace store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md)

[Service Graph Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace.md)

