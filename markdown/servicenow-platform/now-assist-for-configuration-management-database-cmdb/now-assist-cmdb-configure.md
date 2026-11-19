---
title: Configure Now Assist for CMDB
description: Configure the ServiceNow Otto for CMDB application so users can benefit from Agentic workflows, agents, and skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configure.html
release: yokohama
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, ServiceNow Otto for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Now Assist for CMDB

Configure the ServiceNow Otto for CMDB application so users can benefit from Agentic workflows, agents, and skills.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin** and then select the **Settings** tab.

2.  In the list, select **Plugins**.

    Plugins that have already been activated are listed on the **Installed** tab.

3.  Uninstall Now Assist for Service Graph Connectors \(SGC\).

4.  On the ServiceNow Otto for Configuration Management Database \(CMDB\) card, select **Get plugins** and then in the pop-up window, select **Install Plugin**.

    You install the ServiceNow Otto for CMDB \(com.snc.cmdb.gen.ai\) plugin.

    \[Omitted image "na-cmdb-plugins-install-page.png"\] Alt text: Accessing the ServiceNow Otto for CMDB \(com.snc.cmdb.gen.ai\) plugin from the Now Assist Admin console.

    You are redirected to the ServiceNow Store in a new browser tab so you can get the plugin.

5.  Install the ServiceNow Otto for CMDB plugin.

    For instructions on the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

6.  Confirm that ServiceNow Otto for CMDB is installed.

    1.  On the **Now Assist Admin** console, select the **Settings** tab and then select **Plugins** in the list.

    2.  On the **Installed** tab, verify that the **Status** value is **Installed**.

        \[Omitted image "na-cmdb-plugin-installed.png"\] Alt text: Verifying that the plugin is installed.

    Now that you have installed the plugin, you set up the skills for ServiceNow Otto for CMDB.

7.  On the **Now Assist Skills** tab, expand **Technology** and then select **CMDB**.

    \[Omitted image "na-cmdb-turn-on-skill-page.png"\] Alt text: Activating the ServiceNow Otto for CMDB skills.

8.  On the Now Assist skills for CMDB page, select **Turn on** for the Manage duplicate CIs skill.

    No configuration is required for the skill. On the pop-up, select **Back to skills** to set up the other skills.

9.  On the Now Assist skills for CMDB page, select **Activate skill** for the CI summarization skill.

    The skill requires configuration as described in [Configure the CI summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-config-ci-summary.md).

10. On the Now Assist skills for CMDB page, select **Activate skill** for the Service Graph Connector diagnosis skill.

    The skill requires configuration as described in [Configure the Service Graph Connector diagnosis skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown).

11. Configure property settings.

    See [Property settings for Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-data-fdn-properties.md).


## What to do next

To start using ServiceNow Otto for CMDB skills, see [Using agentic workflows in ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md).

To deactivate a skill, select the menu icon \[Omitted image "menu-icon.png"\] Alt text:for the skill and then select **Deactivate skill**.

Admins might be interested in Query Generation. Query Generation is an AI-powered service that translates user questions into an executable query. An executable query contains the data source, filter, aggregation, and visualization instructions that best answer the user's question. For more information, see [Exploring Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/exploring-query-generation.md).

**Parent Topic:**[Configuring Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

**Related topics**  


[CMDB Workspace store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md)

