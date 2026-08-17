---
title: Configure ServiceNow Otto for CMDB
description: Configure the ServiceNow Otto for CMDB application so users can benefit from Agentic workflows, agents, and skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configure-3.0.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-07-30"
reading_time_minutes: 2
breadcrumb: [Configure, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure ServiceNow Otto for CMDB

Configure the ServiceNow Otto for CMDB application so users can benefit from Agentic workflows, agents, and skills.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub** and then select the **Settings** tab.

2.  In the list, select **Plugins**.

    Plugins that have already been activated are listed on the **Installed** tab.

3.  On the ServiceNow Otto for CMDB card, select **Get plugins** and then in the pop-up window, select **Install Plugin**.

    You install the ServiceNow Otto for CMDB \(com.snc.cmdb.gen.ai\) plugin.

    \[Omitted image "na-cmdb-plugins-install-page.png"\] Alt text: Accessing the ServiceNow Otto for CMDB \(com.snc.cmdb.gen.ai\) plugin from the AI Admin Hub console.

    You're redirected to the ServiceNow Store in a new browser tab so you can get the plugin.

4.  Install the ServiceNow Otto for CMDB plugin.

    For instructions on the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

5.  Confirm that ServiceNow Otto for CMDB is installed.

    1.  On the **AI Admin Hub** console, select the **Settings** tab and then select **Plugins** in the list.

    2.  On the **Installed** tab, verify that the **Status** value is **Installed**.

        \[Omitted image "na-cmdb-plugin-installed.png"\] Alt text: Verifying that the plugin is installed.

    Now that you have installed the plugin, you set up the skills for ServiceNow Otto for CMDB.

6.  On the **AI Skills** tab, expand **Technology** and then select **CMDB**.

    \[Omitted image "na-cmdb-turn-on-skill-page.png"\] Alt text: Activating the ServiceNow Otto for CMDB skills.

7.  Configure property settings.

    See [Property settings for ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-data-fdn-properties.md).


## What to do next

To start using ServiceNow Otto for CMDB skills, see [Using ServiceNow Otto skills in ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using-skills.md).

To deactivate a skill, select the menu icon \[Omitted image "menu-icon.png"\] Alt text:for the skill and then select **Deactivate skill**.

Admins might be interested in Query Generation. Query Generation is an AI-powered service that translates user questions into an executable query. An executable query contains the data source, filter, aggregation, and visualization instructions that best answer the user's question. For more information, see [Exploring Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/exploring-query-generation.md).

**Parent Topic:**[Configuring ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

**Related topics**  


[CMDB Workspace store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md)

[Service Graph Workspace store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/sg-workspace.md)

