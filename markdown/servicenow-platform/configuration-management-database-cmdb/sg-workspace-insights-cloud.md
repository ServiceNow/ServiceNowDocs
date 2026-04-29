---
title: Cloud vs Non-cloud insights dashboard in Service Graph Workspace
description: Charts showing counts and details for resources that are hosted on various cloud services versus those resources that aren't, with breakdown by key CI classes such as applications, databases, and datacenters.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Insights view, Explore, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Cloud vs Non-cloud insights dashboard in Service Graph Workspace

Charts showing counts and details for resources that are hosted on various cloud services versus those resources that aren't, with breakdown by key CI classes such as applications, databases, and datacenters.

Resources can be deployed on cloud services such as the Microsoft Azure Cloud, or on the local instance or other non-cloud solutions. For some ongoing operations in the organization, it might be necessary to have those details that can be difficult to obtain.

The following conditions must be met for the Cloud vs Non-cloud resources charts to appear and to show meaningful data:

-   The table Cloud Service Accounts \[cmdb\_ci\_cloud\_service\_account\] must exist.
-   The Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] table must contain at least one record for a cloud datacenter.
-   The Datacenter Types \[sn\_cmdb\_ws\_datacenter\_type\] table must contain at least one record for a datacenter that is classified as cloud storage in the organization. In the base system, this table is pre-populated with several records for common cloud services such as the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] class. The chart calculates and shows data only for cloud services for which there's a record in the Datacenter Types \[sn\_cmdb\_ws\_datacenter\_type\] table.

    For details about adding datacenters in your organization, with the cloud or non-cloud classification, see [Configure datacenters for Cloud vs Non-cloud resources in Service Graph Workspace](../task/sg-workspace-config-datacenter.md).


The following cloud vs Non-cloud charts are available:

-   CI classes bar chart:

    Each bar in the CI classes chart represents a pair of a CI class and a storage type \(cloud, non-cloud\), such as the bar for Applications/Cloud. For each bar, there's a scheduled job that runs every 24 hours to collect and calculate the data for the bar. The running time depends on the amount and complexity of the data that a job collects, which can be different for each scheduled job. Also, the schedules of the jobs are staggered so that they don't all run at the same time and exhaust resources. For details about the class-specific criteria used for the chart calculations, see [Class criteria in Cloud vs Non-cloud resources chart in Service Graph Workspace](../reference/sg-criteria-cloud-resources-chart.md).

    If there’s a CI class/type pair that isn't important in the organization, you can exclude that pair from the CI classes chart. For more details, see [Configure classes for Cloud vs Non-cloud resources in Service Graph Workspace](../task/sg-workspace-config-classes-cloud.md).

    On the CI classes chart, you can:

    -   Select a bar to open the Cloud vs Non-cloud resources pane. Then, select either of the following tabs to drill down into further details for the bar:

        -   **Cloud vs Non-cloud CIs**

            Shows a bar chart for CIs stored on a cloud service and those CIs that aren't, per CI class. For each CI class, select the cloud or the non-cloud bar to show the CIs that are associated with the selected bar, in a list view. You can then select a CI from the list to further drill down to the CI details pane.

        -   **CI Classes by Cloud Providers**

            Pie charts per CI class with more granular details for those CIs that are hosted on cloud providers. Pie slices have randomly-selected colors, and they show a breakdown by cloud providers for various CI classes. For each pie, select a slice to show the CIs that are associated with the pie slice, in a list view. You can then select a CI from the list to further drill down to the CI details pane.

    -   Select **Latest updates** to see updated status for the scheduled jobs that produce the data for the chart. Status is color-coded to indicate whether the job has completed successfully \(green\), or failed to complete \(red\).

-   Application Services pie chart:

    The Application Services pie chart uses the Service Configuration Item Associations \[svc\_ci\_assoc\] table and checks the cloud/non-cloud status of application service CIs in the CI classes chart. Application services in the Application Services pie chart are classified as follows:

    -   Cloud: All of the CIs in the application service have been determined to be hosted on a cloud service.
    -   Non-cloud: All of the CIs in the application service have been determined not to be hosted on a cloud service.
    -   Hybrid: The application service contains a mixture of CIs where some are hosted and some aren't hosted on cloud services.
    -   Unknown: The cloud/non-cloud classification couldn't be determined because some of the application service CIs aren't classified as cloud or non-cloud CIs.
    **Note:** Because classification of Application Services depends on the classification of CIs in the CI classes chart, there might be some discrepancy between the two charts. This can occur if an application service CI changed its cloud/non-cloud status, and the Application Services chart hasn't refreshed yet to reflect that change.

    Select the Application Services chart to access the list views of the associated application services, grouped by cloud/non-cloud classifications. From those list views, you can drill down to the [Dependency Views](../../business-service-management-map-ng/concept/c_BusinesssServiceManagementMaps.md) map for application services.


The scheduled jobs associated with the charts are set up with several hard-coded limits that if exceeded, result in failure conditions that are reflected in the job status. Timing out is set to two hours and the maximum number of records to collect is set to 500,000. If a job exceeds any of those limits, it's automatically stopped.

A scheduled job that can't complete for 3 \(default\) consecutive days is automatically disabled for future runs. You can manage the disabling of scheduled jobs, in the following ways:

-   Modify the default number of consecutive days that are counted by adding the **sn\_cmdb\_ws.insight.category.disable\_after\_failure** system property to the System Properties \[sys\_properties\] table and then setting its value. For more details, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).
-   [Resume a disabled Cloud vs Non-cloud resources scheduled job](../task/sg-workspace-resume-cloud-job.md).

