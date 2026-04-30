---
title: Analytics and Reporting for Cloud Resources
description: Platform Analytics Solutions contain prepackaged Performance Analytics and Reporting content for use with other ServiceNow AI Platform products. Finish the following sentence with a short statement on the business use case for this Solution. For example: This Analytics and Reporting Solution helps you track trends in incidents and plan your incident management strategy going forward.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Cloud discovery reporting, Discovery Platform Analytics Solutions, Discovery, ITOM Visibility, IT Operations Management]
---

# Analytics and Reporting for Cloud Resources

Platform Analytics Solutions contain prepackaged Performance Analytics and Reporting content for use with other ServiceNow AI Platform products.

## Performance Analytics Content Pack for Cloud Resources overview

The Performance Analytics Content Pack for Cloud Resources shows the aggregated view of all your Cloud Resources. You can filter on specific information for more details. There are also analytics tables and views that associate tags with resources so that you can build your own custom dashboards and reports.

The Performance Analytics Content Pack for Cloud Resources works with Discovery and Cloud Provisioning and Governance and it supports the following cloud providers:

-   Amazon Web Services
-   Microsoft Azure public clouds
-   VMware vCenter
-   Google Cloud Platform \(GCP\) \(Supported with Performance Analytics Content Pack for Cloud Resources version 1.2.1 and higher\).

The aggregate count of each cloud resource and the latest Cloud Discovery error logs are displayed on the dashboard. You can filter the cloud resources by the service account, datacenter, or resource group \(only for Microsoft Azure\) under a specific provider and view the resource count and the resources.

The base-system Performance Analytics Content Pack for Cloud Resources dashboard doesn’t contain any widget for the GCP resources. You can create the reports and widgets by consuming data from the appropriate tables. For more information on the tables that contain the GCP resources data, see [Cloud Resources dashboard](cloud-resources-dashboard.md). Alternatively, you can install the Cloud Discovery Workspace application to view the GCP reports and widgets. For more information, see [Cloud Discovery Workspace](../../../product/cloud-operations-workspace/reference/cow-landing-page.md).

For each cloud provider, a separate scheduled job is triggered every 30 minutes. The latest CI data is updated in the cloud resource analytic tables, which allows the dashboard to be more realistic and have the updated count. The information about each scheduled job is available in the Cloud Dashboard Job Status \[sn\_disco\_cd\_cloud\_dashboard\_job\_status\] table. The job details including the provider type, status, start time, end time, and duration are stored in this table.

The reports for the cloud dashboard widgets are generated from the cloud resource analytical tables. The analytical tables are populated through the scheduled job. The scheduled job queries the new database views, and inserts and updates the records into the analytical tables.

The scheduled job can run for a maximum of 360 minutes. The maximum job timeout value is set using the system property \(sn\_disco\_cd.scheduled\_job\_time\_out\_in\_mins\). If the scheduled job exceeds 360 minutes, or the time set in this property, then the job is canceled.

## Required roles

The following roles and tasks are associated with this solution:

-   ServiceNow AI Platform administrator \(admin\): Install and activate this Analytics and Reporting Solution and can make any necessary changes to system properties.
-   Performance Analytics administrator \(pa\_admin\): Review the indicators, breakdowns, widgets, and dashboards. Set up and start data collection and share the dashboards with appropriate stakeholders.
-   Cloud Dashboard user \(sn\_disco\_cd.user\): Crew the cloud resource widgets in the Cloud Dashboard and has read-only access on the Cloud Resource analytics tables and the dashboard reports.
-   Cloud Dashboard administrator \(sn\_disco\_cd.admin\): View, add, or edit the dashboard widgets and reports and has read-only access on the Cloud Resource analytics tables. By default \(sn\_disco\_cd.admin\) contains the \(sn\_disco\_cd.user\) role and \(discovery\_admin\) contains the \(sn\_disco\_cd.admin\) role.

