---
title: Install Scenario Planning for PPM
description: Install the Scenario Planning for PPM application from ServiceNow Store applications. Visit the ServiceNow Store website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.
locale: en-US
release: zurich
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Scenario Planning for PPM, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Install Scenario Planning for PPM

Install the Scenario Planning for PPM application from ServiceNow Store applications. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Before you begin

Complete the following setup checklist for a smooth installation and configuration.

<table id="table_vpg_zst_5jb"><thead><tr><th>

Setup tasks

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is activated.

</td><td>

Navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.

</td></tr><tr><td>

Verify that the Investment Funding for PPM \(com.snc.investment\_planning\_pmo\) plugin is activated.**Note:** This plugin needs to be activated only when you want to retrieve the target amount for a portfolio for annual type of planning from Investment Funding.

</td><td>

Navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.

</td></tr></tbody>
</table>Role required: admin

## About this task

Activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) in your ServiceNow instance before you install Scenario Planning for PPM. For more information see, [Activate PPM Standard \(Project Portfolio Management\)](../../project-portfolio-suite-with-financials/task/t_ActivateProjectPortfolioSuiteWithFinancials.md).

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name \(Scenario Planning for PPM\) or ID \(sn\_pw\_scenario\). If you cannot find an application, you may have to request it from ServiceNow store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Scenario Planning for PPM.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Click **Install**.


-   **[Components installed with Scenario Planning for PPM](../reference/installed-with-scenario-planning.md)**  
Several types of components are installed with the installation of the Scenario Planning for PPM application, including tables and demo data.

**Parent Topic:**[Scenario Planning for PPM](../concept/portfolio-planning-overview.md)

**Related topics**  


[List of plugins \(Zurich\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

