---
title: Activate ITSM Predictive Intelligence Workbench
description: ITSM Predictive Intelligence Workbench is available with activation of the core Predictive Intelligence Workbench \(com.sn\_piwb\_ml\) plugin and the Predictive Intelligence Workbench ITSM content \(com.sn\_piwb\_itsm\_content\) plugin.
locale: en-US
release: yokohama
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ITSM Predictive Intelligence Workbench administration, ITSM Predictive Intelligence Workbench, IT Service Management]
---

# Activate ITSM Predictive Intelligence Workbench

ITSM Predictive Intelligence Workbench is available with activation of the core Predictive Intelligence Workbench \(com.sn\_piwb\_ml\) plugin and the Predictive Intelligence Workbench ITSM content \(com.sn\_piwb\_itsm\_content\) plugin.

## Before you begin

Role required: admin

## About this task

**Important:**

Starting with the yokohama release, the ITSM Predictive Intelligence Workbench will reach its end of life \(EOL\) as part of its deprecation process. It will be completely deprecated and no longer deployed, enhanced, or supported from the yokohama release. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\) plugin. For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md)

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

The ITSM Predictive Intelligence Workbench -related plugins require activation of the Predictive Intelligence application. Predictive Intelligence is available with activation of the Predictive Intelligence \(com.glide.platform\_ml\) plugin and the Predictive Intelligence Reports \(com.glide.platform\_ml\_pa\) plugin, which require an ITSM Pro package subscription. For more details, refer to [Install Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


