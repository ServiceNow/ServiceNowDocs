---
title: Configuring Cloud Cost Management
description: Plan and configure Cloud Cost Management to gain visibility into your total cloud consumption, reduce costs, and optimize the operations of your cloud platforms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/configuring-cloud-insights.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
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

\[Omitted image "bus-download.svg"\] Alt text:Install Cloud Cost Management

</td><td>

Get the Cloud Cost Management application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

[Install Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/install-ci.md)

</td></tr><tr><td>

\[Omitted image "bus-download.svg"\] Alt text:Install Cloud Cost Management Infra Stack

</td><td>

Get the Cloud Cost Management Infra Stack application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).**Important:** The Cloud Cost Management Infra Stack application is available with Cloud Cost Management version 8.1 and later. Installing the Cloud Cost Management Infra Stack application is optional. However, if you have activated this application, you can't deactivate it later.

</td><td>

[Install Cloud Cost Management Infra Stack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/install-ccm-infra.md)

</td></tr><tr><td>

\[Omitted image "bus-3-person.svg"\] Alt text:Assign roles

</td><td>

Assign Cloud Cost Management roles to user groups and to individual users based on user activities and responsibilities.

</td><td>

[Cloud Cost Management roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/cloud-insights-roles.md)

</td></tr><tr><td>

\[Omitted image "bus-server.svg"\] Alt text:Install MID Servers

</td><td>

Install the MID Servers to enable the movement of data between the Discovery application and your cloud platform.

</td><td>

[Installing the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-installation.md)

</td></tr><tr><td>

\[Omitted image "bus-server.svg"\] Alt text:Configure MID Servers

</td><td>

Configure the MID Servers for enabling the Discovery application to communicate with your cloud provider accounts.

</td><td>

-   [Configuring access to CI data on your AWS account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-midserver-config-cloudin.md)
-   [Configuring access to CI data on your Microsoft Azure account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/azure-midserver-config-cloudin.md)
-   [Configuring access to CI data on your Google Cloud account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/cloud-in-midserver-config-gcp.md)

</td></tr><tr><td>

\[Omitted image "bus-discover.svg"\] Alt text:Discover your cloud resources

</td><td>

Discover the service accounts, the credentials for accessing the accounts, and the MID Servers that scan the resources using one of the mentioned approaches.

</td><td>

-   [Using the Cloud Discovery application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-discovery-cloudin.md)
-   [Using the Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-sgc-available.md)

</td></tr><tr><td>

\[Omitted image "bus-datasheet.svg"\] Alt text:Schedule and manage jobs to download billing data for Cloud Cost Management

</td><td>

Provide the Cloud Cost Management application access to the billing and usage data of the used cloud platforms.

</td><td>

-   [Set up access to AWS billing and usage data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-billing-usage-data.md)
-   [Set up access to Microsoft Azure billing and usage data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/azure-billing-usage-data.md)
-   [Set up access to Google Cloud billing and usage data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/google-cloud-billing-data.md)

</td></tr><tr><td>

\[Omitted image "bus-dollar-sign.svg"\] Alt text:Schedule and manage jobs to download price sheets for Cloud Cost Management

</td><td>

Enable Cloud Cost Management to download and store price sheet data of the used cloud platforms.

</td><td>

-   [Schedule and manage the Cloud Cost Management jobs that download AWS price sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-pricesht-sched-dwnld-cloudin.md)
-   [Schedule and manage the Cloud Cost Management jobs that download Microsoft Azure price sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/azure-pricesht-sched-dwnld-cloudin.md)
-   [Schedule and manage the Cloud Cost Management jobs that download Google Cloud price sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/gcp-pricesht-sched-dwnld-cloudin.md)

</td></tr><tr><td>

\[Omitted image "bus-sdlc.svg"\] Alt text:Configure the Cloud Cost Management features

</td><td>

Configure the Cloud Cost Management features to rightsize, identify, assign, manage, and analyze usage data of your cloud resources.

</td><td>

-   [Reservation or Saving plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/ri-cloudin.md)
-   [Rightsizing resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/rs-cloudin.md)
-   [Unused resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/um-cloudin.md)
-   [Business hours](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/bh-cloudin.md)
-   [Unassigned resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/ur-cloudin.md)

</td></tr><tr><td>

\[Omitted image "bus-rocketship.svg"\] Alt text:Use Cloud Cost Management

</td><td>

Gain visibility into your total cloud consumption, reduce costs, and optimize operations of your cloud platforms.

</td><td>

[Using Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/using-cloud-insights.md)

</td></tr></tbody>
</table>