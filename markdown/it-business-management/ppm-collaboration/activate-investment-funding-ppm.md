---
title: Activate Investment Funding for projects and demands
description: Activate the Investment Funding \(com.snc.investment\_funding\) plugin if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: australia
product: PPM Collaboration
classification: ppm-collaboration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PPM Standard \(Project Portfolio Management\), Explore Project Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Activate Investment Funding for projects and demands

Activate the Investment Funding \(com.snc.investment\_funding\) plugin if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Ensure that the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin is installed.

Role required: admin

## About this task

The Investment Funding \(com.snc.investment\_funding\) plugin enables you to request or allocate funds for your projects and demands.

The plugin activates the related plugins if they are not already active. It also adds the sn\_invst\_pln\_investment\_user role to the following roles:

-   project\_manager
-   demand\_manager
-   portfolio\_manager
-   program\_manager

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[PPM Standard \(Project Portfolio Management\)](../../project-portfolio-suite-with-financials/concept/c_ProjectPortfolioSuiteWithFinancials.md)

**Related topics**  


[Currencies and budget reference rates](../../project-management/concept/c_BudgetReferenceRates.md)

[Install Investment Funding](activate-investment-funding.md)

[List of plugins \(Australia\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

