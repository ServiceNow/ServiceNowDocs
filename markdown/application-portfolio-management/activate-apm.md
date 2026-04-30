---
title: Activate Enterprise Architecture - Legacy
description: An administrator can activate the Enterprise Architecture plugin \(com.snc.apm\).
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Activate Enterprise Architecture - Legacy

An administrator can activate the Enterprise Architecture plugin \(com.snc.apm\).

## Before you begin

Role required: admin

## About this task

The Enterprise Architecture \(com.snc.apm\) plugin is the basic plugin for the application.

The Enterprise Architecture plugin activates the following related plugins if they are not already active:

<table id="table_zzn_kx4_rx"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise Architecture – Predictive Intelligence \(com.snc.apm.predictive\_intelligence\)

</td><td>

To predict application category by applying algorithms like similarity on business applications related data.

</td></tr><tr><td>

Business Planner \(com.snc.apm.business\_planner\)

</td><td>

To access the Business Planning portal.

</td></tr><tr><td>

Demand Core \(com.snc.demand\_core\)

</td><td>

To activate the basic core components of Demand Management.

</td></tr><tr><td>

Fiscal Calendar \(com.snc.fiscal\_calendar\)

</td><td>

To create and manage the fiscal calendar.**Note:** Only the Fiscal Calendar Type, Standard is supported.

</td></tr><tr><td>

Performance Analytics – Content Pack – Enterprise Architecture \(com.snc.pa.apm\) plugin

</td><td>

To view the following that are developed using Performance Analytics:-   Analyses of applications in a landscape page
-   Application indicator scores in a dashboard
-   Application 360

 This plugin activates the following two PA plugins:

-   Performance Analytics – Content Pack – Enterprise Architecture and Change Management \(com.snc.pa.apm.change\_request\) plugin: To access performance analytics metrics of business applications associated with Change requests.
-   Enterprise Architecture, Performance Analytics, Performance Analytics – Content Pack – Problem Management \(com.snc.pa.apm.problem\) plugin: To access performance analytics metrics of business applications associated with Problem Management.

</td></tr><tr><td>

Bubble Chart widget for Service Portal \(com.snc.sp\_workbench\_widgets\)

</td><td>

To access service portal components \(widget and dependency\) for Bubble Chart.

</td></tr><tr><td>

Tree map \(com.snc.treemap\)

</td><td>

Enables support for tree map view on any applications.

</td></tr></tbody>
</table>You require the following plugins for specific features in the APM module:

-   **Enterprise Architecture – ATF Tests plugin \(com.snc.apm.atf\) plugin**

    To validate whether Enterprise Architecture works after you make any configuration change such as apply an upgrade or develop an application.

-   **Read only roles for Enterprise Architecture plugin \(com.snc.apm\_read\_roles\)**

    To view or read records of tables that are used to retrieve data for reports and dashboards.

-   **Enterprise Architecture Core plugin \(com.snc.apm\_core\)**

    To register a new business application. The plugin is in base application and activating the Enterprise Architecture plugin \(com.snc.apm\) enhances the Register a Business Application feature to predict and suggest an application category using the machine-learning solution when you on-board an application in to the Enterprise Architecture inventory.

-   **Domain Support – Domain Extensions Installer system plugin**

    To enable the domain separation feature for Enterprise Architecture.

-   **Performance Analytics Premium for APM \(com.snc.pa.premium.apm\) plugin**

    To retrieve historic data that are older than six months.


Activate the following plugins for additional features:

-   **PPM Standard \(com.snc.financial\_planning\_pmo\)**

    To activate an integrated set of applications for project portfolio management and IT software development.

-   **Financial Management For APM \(com.snc.financial\_management\_for\_apm\)**

    To integrate Financial Management with Enterprise Architecture providing preconfigured Business Application Costing cost model and cost indicators.

    This plugin also activates the following plugin to enable Performance Analytics dashboards for Financial Management associated with Enterprise Architecture:

    Performance Analytics — Content Pack — Financial Management for Application Portfolio Management \(com.snc.pa.fm.apm\).


## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

Use the **APM Guided Setup** to set up Enterprise Architecture.

**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/configure-apm.md)

