---
title: Unused resources
description: The Unused resources feature analyzes usage data to identify resources that are wasting money because they aren’t being used. You can schedule Unused resources jobs to power off or terminate the resources that you specify.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/um-cloudin.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Unused resources

The Unused resources feature analyzes usage data to identify resources that are wasting money because they aren’t being used. You can schedule Unused resources jobs to power off or terminate the resources that you specify.

## Recommendations

The Cloud Cost Management application generates or fetches recommendations based on the cloud provider. The following table summarizes the recommendation types and sources for each provider.

|Recommendation type|AWS|Azure|GCP|
|-------------------|---|-----|---|
|Database recommendations|Fetched from provider|Cloud Cost Management identifies idle databases and generates recommendations|Fetched from provider|
|Storage volume recommendations|AWS Elastic Block Store \(EBS\)|Azure Disk|Persistent Disk|
|Aged snapshot recommendations|Amazon EBS Snapshot|Azure Snapshot|GCP Snapshot|

Cloud Cost Management uses an optimized process for each provider.

-   [Unused resources analysis for AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-how-um-works-cloudin.md)
-   [Unused resources analysis for Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/azure-how-um-works-cloudin.md)
-   [Unused resources analysis for Google Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/gcp-how-um-works-cloudin.md)

## How the Unused resources feature works

\[Omitted image "um-process-flow-diagram.png"\] Alt text: Flow of the Unused resources project

1.  On the Unused resources recommendations page, review the recommendations generated for your cloud accounts.
2.  Identify and select the resources you want to power off or terminate. For more information, see [Manage unused resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/manage-unused-mac.md).
3.  Create an Unused resources job, or select an existing job.
4.  Schedule the job by specifying the date and time for the job to run.
5.  Confirm the action to take on the selected resources:
    -   Power off the resource.
    -   Terminate the resource.
    -   Terminate the resource and delete storage. Only the root or primary storage is deleted.
6.  Specify the type of approval required for the action. Unused resources operations are directly integrated with the ServiceNow Change Management feature.
    -   **Auto-approval**: Generates a Standard Change request and the change request is auto-approved.
    -   **Manual approval**: Generates a Normal Change request and the appropriate user approves the change request.
7.  Specify the Change template to use when generating the change requests.
8.  Save the job.

The system immediately generates the change requests. Later, at the scheduled time, the system runs the job to power off or terminate all resources for which the changes are approved. The instance updates Unused resources reports with new recommendations and with approved, successful, pending, rejected, and failed changes. For resources that failed power off or termination, you can reschedule the resources into another job.

**Related topics**  


[Schedule unused resources to be powered off or terminated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/um-schedule-job-cloudin.md)

[Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/c_ITILChangeManagement.md)

[Exclude a resource from all Cloud Cost Management reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/exclusion-list-add-to-cloudin.md)

