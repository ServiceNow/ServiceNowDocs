---
title: Manage unused resources
description: Reduce cost by identifying the unused resources and scheduling jobs to power-off or terminate the unused resources.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Cloud Cost Management, IT Asset Management]
---

# Manage unused resources

Reduce cost by identifying the unused resources and scheduling jobs to power-off or terminate the unused resources.

You can [configure Unused resources operations](../task/um-settings-config-cloudin.md) by selecting **Settings**.

![Unused resources recommendations in Cloud Cost Management Workspace.](../image/unused-res-ws.png)

|Chart|Description|
|-----|-----------|
|Total potential savings by service category|Total savings to expect if all Unused resources recommendations are applied by service category such as Compute, Database, and Storage.|
|Total potential savings by change group|Total savings to expect if all Unused resources recommendations are applied by change group such as Change Management and Application Development.|

<table id="table_i2d_zct_vxb"><thead><tr><th>

Recommendation tab

</th><th>

Description

</th><th>

Available actions on selected recommendations

</th></tr></thead><tbody><tr><td>

New

</td><td>

Resources that are candidates for Unused resources. Each successful execution of a Billing Download job triggers the Budget Forecast, Business Hours, Reservation Plans, Rightsizing, and Unused resources jobs to analyze the spend and usage data of resources and to update the actionable recommendations in reports.**Note:** Microsoft Azure only: The Azure Advisor service generates the recommendations that appear in Rightsizing and Unused resources reports. Cloud Cost Management doesn’t generate the recommendations.

</td><td>

-   Schedule
-   Exclude

</td></tr><tr><td>

Scheduled

</td><td>

Resources that are scheduled in Unused resources jobs.

</td><td>

-   Reschedule
-   Remove from Job

</td></tr><tr><td>

Completed

</td><td>

Resources that the Unused resources job terminated or stopped.

</td><td>

None

</td></tr><tr><td>

Declined

</td><td>

Resources for which owners didn’t want to perform any action or declined the change request.

</td><td>

-   Reschedule
-   Exclude

</td></tr><tr><td>

Failed

</td><td>

Resources for which the Unused resources operation wasn’t successful.

</td><td>

-   Reschedule
-   Exclude

 **Note:** If you perform any action on the terminated or stopped virtual machines, the recommendations get completed but don't show up in the Failed recommendations tab.

</td></tr><tr><td>

Excluded

</td><td>

Resources that are configured not to be considered for Unused resources.

</td><td>

Remove from exclusion

</td></tr></tbody>
</table><table id="table_rl5_4dt_vxb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration item

</td><td>

Unique identifier of the resource.

</td></tr><tr><td>

Monthly savings

</td><td>

Potential savings if the resource is resized to the recommended size.

</td></tr><tr><td>

Provider

</td><td>

The provider that hosts the resource.

</td></tr><tr><td>

Service category

</td><td>

Lists all service categories from the instance sorted by name.

</td></tr><tr><td>

Cloud service

</td><td>

Lists all cloud categories sorted by  name.​

</td></tr><tr><td>

Current size

</td><td>

Size of the resource that was analyzed for.

</td></tr><tr><td>

Rationale

</td><td>

The reason that the system recommends terminating or stopping.-   AWS: Cloud Cost Management analysis of provisioning and usage levels over the last 14 days.
-   Microsoft Azure: Recommendation from the Azure Advisor service.

</td></tr><tr><td>

Confidence

</td><td>

The confidence level in a recommendation.-   High confidence requires the following conditions:
    -   The system has at least 10 days of usage data for the resource.
    -   The current and recommended family or generation is identical.
-   Medium confidence requires the following conditions:
    -   The system has less than 10 days of usage data for the resource.
    -   The current and recommended family or generation is identical.
-   Low confidence: The current and recommended family/generation are different.

</td></tr><tr><td>

Change Group

</td><td>

Change group for the resource.

</td></tr><tr><td>

Account

</td><td>

The service account that includes the resource. A service account represents a group of related regions in your provider account.

</td></tr><tr><td>

Region

</td><td>

If appropriate for the provider, region in the service account that hosts the resource.

</td></tr><tr><td>

Owned by

</td><td>

Owner of the resource.

</td></tr><tr><td>

Source

</td><td>

Source of the recommendations.-   AWS / Azure / GCP: Provider-generated recommendations
-   ServiceNow: Custom-generated recommendations

</td></tr></tbody>
</table>-   **[Configure Unused resources operations](../task/um-settings-config-cloudin.md)**  
The Unused resources feature recommends termination or power-off for resources that are wasting money because they aren’t being used. Configure Unused resources processes and specify the potential savings that trigger notifications.
-   **[Schedule unused resources to be powered off or terminated](../task/um-schedule-job-cloudin.md)**  
To terminate or power off an unused resource, add it to an Unused resources job, specify whether to terminate or power off, and specify when the job should run. You can also move resources from one scheduled job to a different job.
-   **[Move a resource to a different Unused resources job](../task/um-change-job-cloudin.md)**  
You can add resources to a currently scheduled job, move resources from one job to another, or remove resources from a job.
-   **[Exclude a resource from Unused resources analysis](../task/um-exclude-resource-cloudin.md)**  
To ensure that a particular resource is not considered or recommended for Unused resources, add the resource to the Excluded Resources list. The system continues to collect cost and usage data but does not consider the resource for the processes of Unused resources.
-   **[View or edit scheduled and completed Unused resources jobs](../task/view-um-scheduled-jobs.md)**  
View and manage the upcoming and completed Unused resources jobs.

**Parent Topic:**[Using Cloud Cost Management](using-cloud-insights.md)

