---
title: Configuring Cloud Cost Management
description: Plan and configure Cloud Cost Management to gain visibility into your total cloud consumption, reduce costs, and optimize the operations of your cloud platforms.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Cloud Cost Management, IT Asset Management]
---

# Configuring Cloud Cost Management

Plan and configure Cloud Cost Management to gain visibility into your total cloud consumption, reduce costs, and optimize the operations of your cloud platforms.

## Configuration overview

Here's an overview of the process for configuring Cloud Cost Management.

<table id="table_skx_43l_vwb"><thead><tr><th>

Step

</th><th>

Action

</th><th>

Resource

</th></tr></thead><tbody><tr><td>

![Install Cloud Cost Management](../../../reuse/icons/brand-icons/bus-download.svg)Install Cloud Cost Management

</td><td>

Get the Cloud Cost Management application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

[Install Cloud Cost Management](../task/install-ci.md)

</td></tr><tr><td>

![Install Cloud Cost Management Infra Stack](../../../reuse/icons/brand-icons/bus-download.svg)Install Cloud Cost Management Infra Stack

</td><td>

Get the Cloud Cost Management Infra Stack application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).**Important:** The Cloud Cost Management Infra stack application is available with Cloud Cost Management version 8.1 and later. Installing the Cloud Cost Management Infra Stack application is optional. However, if you've activated this application, you can't deactivate it later.

</td><td>

[Install Cloud Cost Management Infra Stack](../task/install-ccm-infra.md)

</td></tr><tr><td>

![Assign Cloud Cost Management roles](../../../reuse/icons/brand-icons/bus-3-person.svg)Assign roles

</td><td>

Assign Cloud Cost Management roles to user groups and to individual users based on user activities and responsibilities.

</td><td>

[Cloud Cost Management roles](../reference/cloud-insights-roles.md)

</td></tr><tr><td>

![Install MID servers](../../../reuse/icons/brand-icons/bus-server.svg)Install MID servers

</td><td>

Install the MID servers to enable the movement of data between the Discovery application and your cloud platform.

</td><td>

[Installing the MID Server](https://www.servicenow.com/docs/access?context=mid-server-installation&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td>

![Configure MID servers](../../../reuse/icons/brand-icons/bus-server.svg)Configure MID Servers

</td><td>

Configure the MID Servers for enabling the Discovery application to communicate with your cloud provider accounts.

</td><td>

-   [Configuring access to CI data on your AWS account](../reference/aws-midserver-config-cloudin.md)
-   [Configuring access to CI data on your Microsoft Azure account](../reference/azure-midserver-config-cloudin.md)
-   [Configuring access to CI data on your Google Cloud account](../reference/cloud-in-midserver-config-gcp.md)

</td></tr><tr><td>

![Discover cloud resources](../../../reuse/icons/brand-icons/bus-discover.svg)Discover your cloud resources

</td><td>

Discover the service accounts, the credentials for accessing the accounts, and the MID Servers that scan the resources using one of the mentioned approaches.

</td><td>

-   [Using the Cloud Discovery application](aws-discovery-cloudin.md)
-   [Using the Service Graph Connectors](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td>

![Download billing data](../../../reuse/icons/brand-icons/bus-datasheet.svg)Schedule and manage jobs to download billing data for Cloud Cost Management

</td><td>

Provide the Cloud Cost Management application access to the billing and usage data of the used cloud platforms.

</td><td>

-   [Set up access to AWS billing and usage data](aws-billing-usage-data.md)
-   [Set up access to Microsoft Azure billing and usage data](azure-billing-usage-data.md)
-   [Set up access to Google Cloud billing and usage data](google-cloud-billing-data.md)

</td></tr><tr><td>

![Download and store price sheet data](../../../reuse/icons/brand-icons/bus-dollar-sign.svg)Schedule and manage jobs to download price sheets for Cloud Cost Management

</td><td>

Enable Cloud Cost Management to download and store price sheet data of the used cloud platforms.

</td><td>

-   [Schedule and manage the Cloud Cost Management jobs that download AWS price sheets](../task/aws-pricesht-sched-dwnld-cloudin.md)
-   [Schedule and manage the Cloud Cost Management jobs that download Microsoft Azure price sheets](../task/azure-pricesht-sched-dwnld-cloudin.md)
-   [Schedule and manage the Cloud Cost Management jobs that download Google Cloud price sheets](../task/gcp-pricesht-sched-dwnld-cloudin.md)

</td></tr><tr><td>

![Configure Cloud Cost Management](../../../reuse/icons/brand-icons/bus-sdlc.svg)Configure the Cloud Cost Management features

</td><td>

Configure the Cloud Cost Management features to rightsize, identify, assign, manage, and analyze usage data of your cloud resources.

</td><td>

-   [Reservation or Saving plans](ri-cloudin.md)
-   [Rightsizing resources](rs-cloudin.md)
-   [Unused resources](um-cloudin.md)
-   [Business hours](bh-cloudin.md)
-   [Unassigned resources](ur-cloudin.md#)

</td></tr><tr><td>

![Use Cloud Cost Management](../../../reuse/icons/brand-icons/bus-rocketship.svg)Use Cloud Cost Management

</td><td>

Gain visibility into your total cloud consumption, reduce costs, and optimize operations of your cloud platforms.

</td><td>

[Using Cloud Cost Management](using-cloud-insights.md)

</td></tr></tbody>
</table>