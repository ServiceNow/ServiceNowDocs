---
title: Configure Now Assist for CMDB
description: Configure the Now Assist for CMDB application so users can benefit from Agentic workflows, agents, and skills.
locale: en-US
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Now Assist for CMDB

Configure the Now Assist for CMDB application so users can benefit from Agentic workflows, agents, and skills.

## Before you begin

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Role required: sn\_nowassist\_admin.nsa\_admin

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin** and then select the **Settings** tab.

2.  In the list, select **Plugins**.

    Plugins that have already been activated are listed on the **Installed** tab.

3.  Uninstall Now Assist for Service Graph Connectors \(SGC\).

4.  On the Now Assist for Configuration Management Database \(CMDB\) card, select **Get plugins** and then in the pop-up window, select **Install Plugin**.

    You install the Now Assist for CMDB \(com.snc.cmdb.gen.ai\) plugin.

    ![Accessing the Now Assist for CMDB (com.snc.cmdb.gen.ai) plugin from the Now Assist Admin console.](../../now-assist-cmdb/image/na-cmdb-plugins-install-page.png)

    You are redirected to the ServiceNow Store in a new browser tab so you can get the plugin.

5.  Install the Now Assist for CMDB plugin.

    For instructions on the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

6.  Confirm that Now Assist for CMDB is installed.

    1.  On the **Now Assist Admin** console, select the **Settings** tab and then select **Plugins** in the list.

    2.  On the **Installed** tab, verify that the **Status** value is **Installed**.

        ![Verifying that the plugin is installed.](../../now-assist-cmdb/image/na-cmdb-plugin-installed.png)

    Now that you have installed the plugin, you set up the skills for Now Assist for CMDB.

7.  On the **Now Assist Skills** tab, expand **Technology** and then select **CMDB**.

    ![Activating the Now Assist for CMDB skills.](../../now-assist-cmdb/image/na-cmdb-turn-on-skill-page.png)

8.  On the Now Assist skills for CMDB page, select **Turn on** for the Manage duplicate CIs skill.

    No configuration is required for the skill. On the pop-up, select **Back to skills** to set up the other skills.

9.  On the Now Assist skills for CMDB page, select **Activate skill** for the CI summarization skill.

    The skill requires configuration as described in [Configure the CI summarization skill](now-assist-cmdb-config-ci-summary.md).

10. On the Now Assist skills for CMDB page, select **Activate skill** for the Service Graph Connector diagnosis skill.

    The skill requires configuration as described in [Configure the Service Graph Connector diagnosis skill](now-assist-cmdb-config-sgc-diagnose.md).

11. Configure property settings.

    See [Property settings for Now Assist for CMDB](../../now-assist-cmdb/reference/na-data-fdn-properties.md).


## What to do next

To start using Now Assist for CMDB skills, see [Using agentic workflows in Now Assist for CMDB](../concept/now-assist-cmdb-using.md).

To deactivate a skill, select the menu icon ![](../image/menu-icon.png)for the skill and then select **Deactivate skill**.

Admins might be interested in Query Generation. Query Generation is an AI-powered service that translates user questions into an executable query. An executable query contains the data source, filter, aggregation, and visualization instructions that best answer the user's question. For more information, see [Exploring Query Generation](https://www.servicenow.com/docs/access?context=exploring-query-generation&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

**Parent Topic:**[Configuring Now Assist for CMDB](../concept/now-assist-cmdb-configuring.md)

**Related topics**  


[CMDB Workspace store app](../concept/cmdb-workspace.md)

