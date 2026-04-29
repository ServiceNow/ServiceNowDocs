---
title: Unused resources
description: The Unused resources feature analyzes usage data to identify resources that are wasting money because they aren’t used. Schedule Unused resources jobs to power off or terminate the resources that you specify.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Unused resources

The Unused resources feature analyzes usage data to identify resources that are wasting money because they aren’t used. Schedule Unused resources jobs to power off or terminate the resources that you specify.

## Recommendations

For AWS and GCP, database recommendations are fetched from the provider. For Azure, Cloud Cost Management generates recommendations for idle databases.

Storage volume recommendations are fetched for AWS, Azure, and GCP from the providers:

-   AWS \(AWS Elastic Block Store for Storage Volumes\)
-   Azure \(Azure Disk for Storage Volumes\)
-   GCP \(Persistent Disk for Storage Volumes\)

Cloud Cost Management generates aged snapshot recommendations for the following providers:

-   AWS \(Amazon EBS Snapshot\)
-   Azure \(Azure Snapshot for Storage Snapshots\)
-   GCP \(GCP Snapshot for Storage Snapshots\)

## How the Unused resources feature works

![Flow of the Unused resources project](../image/um-process-flow-diagram.png)

1.  On the Unused resources recommendations page, select the resources to terminate or power off based on your analysis of the recommendations. For more information, see [Manage unused resources](manage-unused-mac.md).
2.  Add the resources to an Unused resources job, either a new job or an already-defined job.
3.  Specify the date and time for the job to run.
4.  Specify the action to take on the selected resources:
    -   Power off the resource.
    -   Terminate the resource.
    -   Terminate the resource and delete storage. Only root or primary storage is deleted.
5.  Specify the type of approval required for the specified action. Unused resources operations are directly integrated with the ServiceNow Change Management feature.
    -   **Auto-approval**: Generates a Standard Change request and the change request is auto-approved.
    -   **Manual approval**: Generates a Normal Change request and the appropriate user approves the change request.
6.  Specify the Change template to use when generating the change requests.
7.  Save the job.

The system immediately generates the change requests. Later, at the scheduled time, the system runs the job to power off or terminate all resources for which the changes are approved. The instance updates Unused resources reports with new recommendations and with approved, successful, pending, rejected, and failed changes. For resources that failed power off or termination, you can reschedule the resources into another job.

## How Cloud Cost Management generates Unused resources recommendations

Cloud Cost Management uses an optimized process for each provider.

-   [Unused resources analysis for AWS](../reference/aws-how-um-works-cloudin.md)
-   [Unused resources analysis for Microsoft Azure](../reference/azure-how-um-works-cloudin.md)
-   [Unused resources analysis for Google Cloud](../reference/gcp-how-um-works-cloudin.md)

**Related topics**  


[Schedule unused resources to be powered off or terminated](../task/um-schedule-job-cloudin.md)

[Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

[Exclude a resource from all Cloud Cost Management reports](../task/exclusion-list-add-to-cloudin.md)

