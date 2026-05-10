---
title: Configure Cloud Cost Management for Google Cloud
description: The Cloud Cost Management application is available on the ServiceNow Store.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Configure Cloud Cost Management for Google Cloud

The Cloud Cost Management application is available on the ServiceNow Store.

## General requirements and limitations

-   Cloud Cost Management isn't supported on mobile devices.
-   Values in reports might vary slightly from provider billing values due to currency conversion or rounding.

## Requirements and limitations for Google Cloud

You must have Google Cloud administrator permissions to work in the Google Cloud Console

## Download and activate Cloud Cost Management

Role required: sys\_admin

<table id="table_myg_bq3_lfb"><thead><tr><th>

Step

</th><th>

Description

</th><th>

Action

</th></tr></thead><tbody><tr><td>

![](../../../reuse/icons/brand-icons/bus-cloud-download.svg) Get the app.

</td><td>

Get the Cloud Cost Management app from the ServiceNow Store.

</td><td>

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to get the Cloud Cost Management app and supporting apps.

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-sdlc.svg) Activate all supporting plugins and applications.

</td><td>

Activate the plugins listed on the ServiceNow Store page for Cloud Cost Management. You might need to request some of the plugins from your ServiceNow representative.

</td><td>

For instructions, see:-   [Request as plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_RequestAPlugin.md)
-   [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md)

</td></tr></tbody>
</table>## Overview: Setting up Cloud Cost Management

Here's an overview of your set up process. Detailed instructions appear in the table that follows.

![Setup process for the Cloud Cost Management app](../image/setup-procedure-cloudin.png)

When you first open the app, the home page enables you set up a provider and to assign the insights\_owner role.

![Initial home page of the Cloud Cost Management app](../image/cloud_insights_home.png)

After you set up a provider and assign the insights\_owner role, the page displays additional setup activities.

**Note:** The Configure and Run Discovery card appears only if you use the Discovery application to discover cloud resources.

![Home page after you set up a provider and assign insights_owner](../image/homepage-second-config.png)

-   When you select the **Set up and Run Discovery** button in the Configure and Run Discovery section, the Discover Schedules form opens.
-   When you select the **Set up Billing Download** button in the Download Billing and Usage Data section, the Billing Download Jobs form opens.
-   When you select the **Set up Price Sheet Download** button in the Download Price Sheets section, the Price Sheets Download Jobs form opens.

After you finish all configuration, the page will show overview data and give quick access to reports.

## Tasks: Setting up Cloud Cost Management

<table id="table_zqr_2l1_zhb"><thead><tr><th>

Step

</th><th>

Description

</th><th>

Action

</th></tr></thead><tbody><tr><td>

![](../../../reuse/icons/brand-icons/bus-3-person.svg) Assign roles to Cloud Cost Management users and groups.

</td><td>

You assign Cloud Cost Management roles to user groups and to individual users based on user activities and responsibilities.

</td><td>

[Cloud Cost Management roles](../reference/cloud-insights-roles.md)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-compliance.svg) Set up access to Google Cloud.

</td><td>

To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery, you first create Google Cloud credentials in the Google Cloud portal. You then securely store the credentials in a service account in your instance.

</td><td>

[Set up access to Google Cloud billing and usage data](google-cloud-billing-data.md)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-proxy.svg) Configuring MID Servers to access CI data on provider accounts for Cloud Cost Management.

</td><td>

To ensure secure and reliable communications, the Discovery process communicates with your cloud provider accounts and cloud resources through one or more MID Servers. You can set up the MID Servers on your network or in one of your cloud networks.

</td><td>

[Configuring access to CI data on your Google Cloud account](../reference/cloud-in-midserver-config-gcp.md)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-discover.svg)Discover your cloud resources.

</td><td>

**Note:** The Configure and Run Discovery card appears only if you use the Discovery application to discover cloud resources.

When you select the **Set up and Run Discovery** button on the Configure and Run Discovery card, the Discover Schedules form opens. You schedule the Discovery process to ensure that the CMDB data on resources remains current.

</td><td>

[Discovering your cloud resources for use](aws-discovery-cloudin.md)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-automated-testing-framework.svg) Schedule and manage the jobs that download billing data for Cloud Cost Management.

</td><td>

When you select the **Set up Billing Download** button in the Download Billing and Usage Data section, the Billing Download Jobs form opens. Billing Download jobs download, organize, and store billing data for your payer account on the schedule that you specify. The system analyzes the data to generate reports and to make recommendations for changes in your cloud operations that can lead to cost savings.

</td><td>

[Schedule and manage the jobs that download Google Cloud billing data](../task/gcp-bill-dwnld-job-cloudin.md)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-automated-testing-framework.svg) Schedule and manage the Cloud Cost Management jobs that download price sheets.

</td><td>

When you select the **Set up Price Sheets Download** button in the Download Price Sheets section, the Price Sheets Download Jobs form opens. A Price Sheet Download job downloads and stores price sheet data. The Rightsizing and Unused resources processes use price sheet data when generating recommendations.

</td><td>

[Schedule and manage the Cloud Cost Management jobs that download Google Cloud price sheets](../task/gcp-pricesht-sched-dwnld-cloudin.md)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-sdlc.svg) Configure the Cloud Cost Management features:

 -   Rightsizing
-   Unused Machines
-   Business Hours
-   Unassigned Resources

</td><td>

-   The feature analyzes resource usage to recommend better sizes for resources that are wasting money by being over-provisioned or underused. A confidence rating and predicted savings support each recommendation. You schedule Rightsizing jobs to resize the resources you specify.
-   The Unused Machines feature analyzes usage data to identify resources that are wasting money because they are not used. You schedule Unused Machines jobs to power-off or terminate the resources that you specify.
-   A Business Hours job applies policies to identify resources that are running when they should be powered off, reports them, and can start and stop them on a schedule that you specify. Running only during specified business hours can significantly reduce your cloud spend.
-   Unassigned Resources policies help you to identify the resources that are not associated with a change group and to assign them appropriately. When a resource is assigned to the correct group, the resource can be appropriately governed even as it goes through stages such as patching, upgrading, and reconfiguring.

</td><td>

-   [Rightsizing resources](rs-cloudin.md)
-   [Unused resources](um-cloudin.md)
-   [Business hours](bh-cloudin.md)
-   [Unassigned resources](ur-cloudin.md#)

</td></tr></tbody>
</table>