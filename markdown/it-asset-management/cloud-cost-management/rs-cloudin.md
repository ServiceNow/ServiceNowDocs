---
title: Rightsizing resources
description: The Rightsizing feature analyzes resource usage to recommend better sizes for resources that are wasting money by being over-provisioned or underused. A confidence rating and predicted savings support each recommendation. Schedule Rightsizing jobs to resize the resources you specify.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Rightsizing resources

The Rightsizing feature analyzes resource usage to recommend better sizes for resources that are wasting money by being over-provisioned or underused. A confidence rating and predicted savings support each recommendation. Schedule Rightsizing jobs to resize the resources you specify.

## How Rightsizing works

![Flow of the Rightsizing process](../image/rs-process-flow-diagram.png)

The system updates Rightsizing recommendations each time that billing and usage data are updated.

Follow this process to define a Rightsizing job:

1.  On the Rightsizing recommendations page, select the resources to rightsize based on your analysis of the recommendations. For more information, see [Resize resources with Rightsizing](resize-res-ci.md).
2.  Add the resources to a Rightsizing job. The job can be a new or an already-defined one.
3.  Specify the date and time for the job to run.
4.  Specify the type of approval required for the Rightsizing action.

    Rightsizing operations are directly integrated with the ServiceNow Change Management feature.

    -   **Auto-approval**: Generates a Standard Change request and the change request is auto-approved.
    -   **Manual approval**: Generates a Normal Change request and the appropriate user approves the change request.
5.  Save the job.

When you save the job, the system immediately generates the change requests. Later, at the scheduled time, the system runs the job. The job performs the following operations:

-   For each approved change, resize the resource. For a resource in the ON state, stop the resource, resize it, and then restart it. If the attempt to resize fails, perform a rollback. For more information, see [AWS only – Rollback on failed Rightsizing attempts](rs-rollback-cloudin.md).
-   Update the Rightsizing reports with new recommendations and with approved, successful, pending, rejected, and failed changes.

For pending, rejected, and failed change requests, you can reschedule the resources into another job.

**Note:** Rightsizing operation on a stopped AWS Relational Database Service \(RDS\) database isn’t supported from the AWS provider. If you try to perform Rightsizing on stopped databases, the resize operation fails with the error `InvalidDBInstanceState - You can't modify a stopped DB instance. Start the DB instance, and then modify it.`.

## How Cloud Cost Management generates Rightsizing recommendations

Cloud Cost Management uses a process that is optimized for each provider.

-   [Rightsizing analysis for AWS](../reference/aws-how-rs-works-cloudin.md)
-   [Rightsizing analysis for Microsoft Azure](../reference/azure-how-rs-works-cloudin.md)
-   [Rightsizing analysis for Google Cloud](../reference/gcp-how-rs-works-cloudin.md)

## Recommendations

The Cloud Cost Management application can generate recommendations for Virtual Machines \(AWS, Azure, GCP\), SQL Databases \(Azure, GCP\), and RDS Databases \(AWS\). CPU, memory, and network usage metrics are used to generate database rightsizing recommendations for the database resources.

The Cloud Cost Management application generates recommendations for storage volumes for AWS and Azure providers:

-   Cloud category - AWS Elastic Block Store for Storage Volumes: Service category is storage.
-   Cloud category - Azure Disk for Storage Volumes: Service category is storage.

## Confidence levels in recommendations

Each recommendation that the system makes to rightsize a resource has an associated confidence level. You consider the confidence level while deciding whether to rightsize a resource. Confidence levels reflect the following factors:

-   High confidence requires the following conditions:
    -   The system has 10 or more days of usage data for the resource.
    -   The current and recommended family/generation are identical.
-   Medium confidence requires the following conditions:
    -   The system has less than 10 days of usage data for the resource.
    -   The current and recommended family/generation are identical.
-   Low confidence: The current and recommended family/generation are different.

