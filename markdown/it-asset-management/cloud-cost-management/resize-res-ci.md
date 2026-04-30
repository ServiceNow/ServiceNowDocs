---
title: Resize resources with Rightsizing
description: Gain better visibility of resource usage by identifying your over-provisioned or underused resources, configuring rightsizing operations, implementing rightsizing recommendations, and performing various rightsizing operations.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Resize resources with Rightsizing

Gain better visibility of resource usage by identifying your over-provisioned or underused resources, configuring rightsizing operations, implementing rightsizing recommendations, and performing various rightsizing operations.

You can [configure Rightsizing operations](../task/rs-settings-config-cloudin.md) by selecting **Settings**.

![Rightsizing recommendations in Operations view.](../image/rightsizing-ws.png)

|Chart|Description|
|-----|-----------|
|Total potential savings by service category|Total savings to expect if all rightsizing recommendations are applied by service category such as Compute, Database, and Storage.|
|Total potential savings by change group|Total savings to expect if all rightsizing recommendations are applied by change group such asChange Management and Application Development.|

<table id="table-rs-recommendations-tab"><thead><tr><th>

Recommendations tab

</th><th>

Description

</th><th>

Available actions on selected recommendations

</th></tr></thead><tbody><tr><td>

New

</td><td>

Resources that are candidates for Rightsizing. Each successful execution of a Billing Download job triggers the Rightsizing jobs to analyze spend and usage data and to update the actionable recommendations in reports.

</td><td>

-   Exclude
-   Schedule

</td></tr><tr><td>

Scheduled

</td><td>

Resources that are scheduled in Rightsizing jobs.

</td><td>

-   Reschedule
-   Remove

</td></tr><tr><td>

Declined

</td><td>

Resources that owners didn’t want to resize \(declined the change request\).

</td><td>

-   Exclude
-   Reschedule

</td></tr><tr><td>

Completed

</td><td>

Resources that were rightsized by the Rightsizing job.

</td><td>

None

</td></tr><tr><td>

Failed

</td><td>

Resources for which the Rightsizing operation wasn’t successful. For failed attempts, the Rightsizing operation performs a rollback as described in [AWS only – Rollback on failed Rightsizing attempts](rs-rollback-cloudin.md).

</td><td>

-   Exclude
-   Reschedule

</td></tr><tr><td>

Excluded

</td><td>

Resources that are configured not to be considered for Rightsizing.

</td><td>

Remove from exclusion

</td></tr></tbody>
</table><table id="table_qkd_sg2_qxb"><thead><tr><th>

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

Potential savings if the resource is resized to the Recommended size.

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

Size of the resource that was analyzed for Rightsizing, the size that you’re currently paying for.

</td></tr><tr><td>

Recommended size

</td><td>

-   AWS: The size that is operationally and cost-wise most appropriate for the resource, based on the analysis of provisioning and usage levels over the last 14 days.
-   Microsoft Azure: Recommendation from the Azure Advisor service.

</td></tr><tr><td>

Override size

</td><td>

Size to use instead of the recommended size. By default, the system uses the Recommended size when Rightsizing. Specify a different size by specifying an Override size.

</td></tr><tr><td>

Rationale

</td><td>

The reason that the system recommends resizing.-   AWS: Based on Cloud Cost Management analysis of provisioning and usage levels over the last 14 days.
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

Change group

</td><td>

Change group for the resource.

</td></tr><tr><td>

Source

</td><td>

Source of the recommendations.-   AWS / Azure / GCP: Provider-generated recommendations
-   ServiceNow: Custom-generated recommendations

</td></tr><tr><td>

State

</td><td>

For resources that match an Auto-approval \(Standard Change\) approval type, status of the change request.

</td></tr><tr><td>

Job

</td><td>

Name of the Rightsizing job that the resource is part of.

</td></tr><tr><td>

Planned date

</td><td>

Date that the job is scheduled to run.

</td></tr><tr><td>

Change request

</td><td>

The change request that is associated with the recommendation.

</td></tr></tbody>
</table>-   **[Configure Rightsizing operations](../task/rs-settings-config-cloudin.md)**  
Configure Rightsizing processes and specify the amount of potential rightsizing savings that triggers notifications.
-   **[Schedule resources to be rightsized](../task/rs-schedule-job-cloudin.md)**  
To rightsize a resource, add it to a Rightsizing job and specify when the job should run. You can also move resources out of one scheduled job into a different job or remove a resource from a job.
-   **[Move a resource to a different Rightsizing job](../task/rs-change-job-cloudin.md)**  
You can add resources to a currently scheduled job, move resources from one job to another, or remove resources from a job.
-   **[Exclude a resource from Rightsizing analysis](../task/rs-exclude-resource-cloudin.md)**  
To ensure that a particular resource is not considered or recommended for Rightsizing, add the resource to the Excluded Resources list. The system continues to collect cost and usage data but does not consider the resource for Rightsizing.
-   **[View or edit scheduled and completed Rightsizing jobs](../task/view-rs-scheduled-jobs.md)**  
View and manage the upcoming and completed Rightsizing jobs.

**Parent Topic:**[Using Cloud Cost Management](using-cloud-insights.md)

