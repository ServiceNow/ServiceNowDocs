---
title: Install Strategic Spend Tracking for PPM
description: Install the Strategic Spend Tracking for PPM application from ServiceNow Store applications. Visit the ServiceNow Store website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.
locale: en-US
release: zurich
product: PPM Collaboration
classification: ppm-collaboration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Strategic spend tracking, Project Portfolio Management, Strategic Portfolio Management]
---

# Install Strategic Spend Tracking for PPM

Install the Strategic Spend Tracking for PPM application from ServiceNow Store applications. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Before you begin

Complete the following setup checklist for a smooth installation and configuration.

|Setup tasks|Description|
|-----------|-----------|
|Verify that PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is activated.|Navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.|

Role required: admin

## About this task

Activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) in your ServiceNow instance before you install Strategic Spend Tracking for PPM. For more information see, [Activate PPM Standard \(Project Portfolio Management\)](../../project-portfolio-suite-with-financials/task/t_ActivateProjectPortfolioSuiteWithFinancials.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


-   **[Components installed with Strategic Spend Tracking for PPM](../reference/installed-with-ppm-strategic-spend-tracking.md)**  
Several types of components are installed with activation of Strategic Spend Tracking for PPM, including tables and scheduled jobs.

**Parent Topic:**[Strategic Spend Tracking for PPM](../concept/ppm-strategic-spend-tracking-overview.md)

**Related topics**  


[List of plugins \(Zurich\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

