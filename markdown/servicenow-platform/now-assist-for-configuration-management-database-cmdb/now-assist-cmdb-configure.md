---
title: Configure Now Assist for Configuration Management Database \(CMDB\)
description: Configure the Now Assist for Configuration Management Database \(CMDB\) application so users can benefit from its generative AI skills.
locale: en-US
release: xanadu
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Now Assist for Configuration Management Database \(CMDB\), Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Now Assist for Configuration Management Database \(CMDB\)

Configure the Now Assist for Configuration Management Database \(CMDB\) application so users can benefit from its generative AI skills.

## Before you begin

The following scheduled jobs support the manage duplicate CIs skill:

-   The Populate Duplicate Task Data scheduled job must be enabled. For more information, see [Components installed for duplicate CI remediation](../reference/components-installed-with-dup-ci.md).
-   The Populate Duplicate Task Group Daily scheduled job must be enabled to provide analysis of the root cause of remediation tasks. For more information, see [Components installed with CMDB Workspace](../reference/installed-with-cmdb-workspace.md).
-   The Correctness Score Calculation scheduled job improves the accuracy of summary details on the CMDB Health Dashboard. For more information, see [Enable and configure a CMDB Health Dashboard job](t_EnableCMDBHealthDashboardJob.md).

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin** and then select the **Settings** tab.

2.  In the list, select **Plugins**.

3.  On the Now Assist for Configuration Management Database \(CMDB\) card, select **Get plugins** and then in the pop-up window, select **Install Plugin**.

    ![Accessing the Now Assist for CMDB (com.snc.cmdb.gen.ai) plugin from the card.](../image/na-cmdb-plugins-install-page.png)

    For instructions on the activation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

    **Note:** The plugins that have already been activated are listed on the **Installed** tab.

4.  Navigate to **All** &gt; **Now Assist Admin** and then activate and configure the skills.

    1.  On the **Now Assist Features** tab, expand **Technology** and then select **CMDB**.

        ![List of available and activated skills.](../image/na-cmdb-avail-skills-page.png)

    2.  On the Now Assist Skills for CMDB page, review the skills, and then select **View details**.

    3.  On the Configuration Management Database \(CMDB\) page, select **Turn on** for the manage duplicate CIs skill.

        No configuration is required.

    4.  Select **Activate skill** for the CI summarization skill.

        **Note:** The CI summarization skill requires configuration. For more information, see [Configure the CI summarization skill](now-assist-cmdb-config-ci-summary.md).

        ![Activating the Now Assist for CMDB skills.](../image/na-cmdb-turn-on-skill-page.png)


## What to do next

To start using Now Assist for CMDB skills, see [Using Now Assist for CMDB](../concept/now-assist-cmdb-using-1.md).

To deactivate a skill, select the menu icon \(![menu icon.](../image/menu-icon.png)\) for the skill and then select **Deactivate skill**.

**Related topics**  


[CMDB Workspace store app](../concept/cmdb-workspace.md)

