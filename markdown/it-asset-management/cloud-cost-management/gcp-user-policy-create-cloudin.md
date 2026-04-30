---
title: Setup roles for Google Cloud billing download
description: To perform billing download for Google Cloud, you need specific roles and permissions for various features.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Cloud Cost Management for Google Cloud, Configure, Cloud Cost Management, IT Asset Management]
---

# Setup roles for Google Cloud billing download

To perform billing download for Google Cloud, you need specific roles and permissions for various features.

## Before you begin

Roles required:

-   On the Google Cloud Console: Google Cloud administrator.
-   Cloud Cost Management: insights\_admin \[sn\_clin\_core.insights\_admin\] or admin.

## About this task

## Procedure

1.  Add the following required permissions for the Billing module in the Google Cloud provider console.

<table id="table_qxd_wfk_33c"><thead><tr><th>

Function and feature

</th><th>

APIs and permission

</th></tr></thead><tbody><tr><td>

Cost analysis and reporting-   Cost allocation and tracking
-   Cost trend analysis
-   Budget monitoring
-   Spend forecasting
-   Custom cost reports


</td><td>

**Note:** These permissions enable retrieving billing and spend data for cost analysis.

 BigQuery \(Billing data\)

-   bigquery.jobs.create: Create jobs to query billing data
-   bigquery.jobs.list: List query jobs
-   bigquery.tables.getData: Read billing export data
 Resource manager

-   resourcemanager.projects.get: Get project cost context
-   resourcemanager.projects.list: List projects for cost aggregation


</td></tr><tr><td>

Recommendations-   Identify under-used resources
-   Suggest optimal instance types
-   Recommend disk size adjustments
-   Cost optimization opportunities


</td><td>

**Note:** These permissions enable viewing the cost-saving recommendations. You must grant the permissions for retrieving billing and spend data before viewing the recommendations.

 BigQuery

-   bigquery.jobs.list: List BigQuery jobs
-   bigquery.tables.getData: Access table data for cost analysis
 Cloud SQL

-   cloudsql.instances.get: Retrieve Cloud SQL instance details
-   cloudsql.instances.list: List all Cloud SQL instances
-   cloudsql.databases.get: Get database details
-   cloudsql.databases.list: List databases
 Compute engine

-   compute.instances.get: Retrieve VM instance details
-   compute.instances.list: List all VM instances
-   compute.instances.getIamPolicy: Get IAM policies for instances
-   compute.disks.get: Retrieve disk details
-   compute.disks.list: List all disks
-   compute.autoscalers.get: Get autoscaler configurations
-   compute.autoscalers.list: List autoscalers
-   compute.regions.list: List available regions
-   compute.snapshots.get: List all snapshot
 Recommender - Compute Instance Recommendations

-   recommender.computeInstanceMachineTypeRecommendations.get
-   recommender.computeInstanceMachineTypeRecommendations.list
-   recommender.computeInstanceMachineTypeRecommendations.update
-   recommender.computeDiskIdleResourceRecommendations.get
-   recommender.computeDiskIdleResourceRecommendations.list
-   recommender.computeDiskIdleResourceRecommendations.update
-   recommender.computeInstanceIdleResourceRecommendations.get
-   recommender.computeInstanceIdleResourceRecommendations.list
-   recommender.computeInstanceIdleResourceRecommendations.update
 Recommender – Cloud SQL Recommendations

-   recommender.cloudsqlIdleInstanceRecommendations.get
-   recommender.cloudsqlIdleInstanceRecommendations.list
-   recommender.cloudsqlIdleInstanceRecommendations.update
-   recommender.cloudsqlOverprovisionedInstanceRecommendations.get
-   recommender.cloudsqlOverprovisionedInstanceRecommendations.list
-   recommender.cloudsqlOverprovisionedInstanceRecommendations.update
 Recommender - General

-   recommender.locations.get: Get recommender location details
-   recommender.locations.list: List available recommender locations


</td></tr><tr><td>

Resource Lifecycle Management-   Start/stop instances on schedule
-   Delete unused resources
-   Resize resources based on recommendations
-   Automated cost optimization actions


</td><td>

**Note:** These permissions enable active resource management to act on cost-saving measures across your cloud environments. You must grant the permissions for retrieving billing and spend data and viewing recommendations before granting permissions for resource management.

 Compute engine - Lifecycle operations

-   compute.instances.start: Start stopped instances
-   compute.instances.stop: Stop running instances
-   compute.instances.delete: Delete unused instances
-   compute.instances.update: Update instance configurations
-   compute.instances.setDiskAutoDelete: Configure disk auto-delete
-   compute.disks.delete: Delete unused disks
-   compute.disks.update: Update disk configurations
-   compute.snapshots.create: Create a new snapshot
 Cloud SQL - Lifecycle operations

-   cloudsql.instances.restart: Restart Cloud SQL instances
-   cloudsql.instances.delete: Delete unused SQL instances
-   cloudsql.instances.update: Update SQL instance configurations
-   cloudsql.databases.delete: Delete unused databases
-   cloudsql.databases.update: Update database configurations


</td></tr></tbody>
</table>2.  Set the roles at the Google Cloud organization level so that it is applicable for all the projects under that level.

    The following APIs should be enabled on the Google Cloud Console for each project.

    -   Compute Engine API
    -   Recommender API
    -   BigQuery API
    -   BigQuery Data Transfer API
    -   Cloud Resource Manager API
    -   Cloud SQL Admin API
    -   Batch API
3.  For details on policy creation see [Google Cloud docs](https://cloud.google.com/docs).


