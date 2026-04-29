---
title: \(Legacy\) Quickly configure Performance Analytics for a task table
description: The configuration generator enables you to quickly configure Performance Analytics to display data from any task table.As an administrator, you can enable the Performance Analytics configuration generator plugin \(com.snc.pa.configurationgenerator\).
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# \(Legacy\) Quickly configure Performance Analytics for a task table

The configuration generator enables you to quickly configure Performance Analytics to display data from any task table.

**Note:** The configuration generator is a legacy feature.

You can specify a Task-based table to report on, and the configuration generator automatically creates indicators, breakdowns, formulas, data collection jobs, and dashboards. This configuration provides the same elements as the Performance Analytics incident solution, but for any Task table. When using domain separation, all records are created in the domain of the current user.

**Note:** You can use the configuration generator only with tables that extend Task. You may need to tweak the configuration before you start using the files that are created by the generator.

You can access the configuration generator by navigating to **Performance Analytics** &gt; **Configuration Generator**.

After generating a configuration for the selected table, you can view the created records using the **Go to the configuration record**, **Generated Indicators**, and **Generated Jobs** related links. You can modify the generated records as needed using standard Performance Analytics configuration options.

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

## Activate the Performance Analytics configuration generator

As an administrator, you can enable the Performance Analytics configuration generator plugin \(com.snc.pa.configurationgenerator\).

### Before you begin

Role required: admin

Before starting this procedure, you must have a subscription to Performance Analytics.

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


