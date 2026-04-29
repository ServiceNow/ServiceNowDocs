---
title: Cloud Resources dashboard
description: The Cloud Resources dashboard shows the aggregated view of all your cloud resources, their combined analytical views, and a visual summary and detail of all your cloud resources.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Cloud discovery reporting, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Cloud Resources dashboard

The Cloud Resources dashboard shows the aggregated view of all your cloud resources, their combined analytical views, and a visual summary and detail of all your cloud resources.

![Animated gif of the four Cloud Resources dashboard tabs](../image/cloud-resources-dashboard.gif "Cloud Resources dashboard tabs")

## Use cases

For examples of how someone in your organization could use this dashboard, see the use cases.

|User|Dashboard use|
|----|-------------|
|Cloud user|Discovery customers have an enormous number of CIs obtained from Cloud Discovery which can be viewed in one place.|
|Cloud user with sn\_disco\_cd.admin role|Use the analytics tables that are available to build custom dashboards. These tables are specific baseline database views with resource tags. See [Customize the Cloud Resources dashboard](cloud-resources-dashboard.md#section_zcf_lvc_3nb) for more information.|

## Data visualizations

|Title|Type|Source table|
|-----|----|------------|
|Cloud Networks|Line|VMware Network Analytics \[sn\_disco\_cd\_vmware\_network\_analytics\]|
|Cloud Networks|Single Score|VMware Network Analytics \[sn\_disco\_cd\_vmware\_network\_analytics\]|
|Public Cloud Resources|Line|Cloud Analytics \[sn\_disco\_cd\_analytics\]|
|Clusters|Single Score|VMware Cluster Analytics \[sn\_disco\_cd\_vmware\_cluster\_analytics\]|
|Clusters|Line|VMware Cluster Analytics \[sn\_disco\_cd\_vmware\_cluster\_analytics\]|
|Compute Security Groups|Single Score|AWS Security Group Analytics \[sn\_disco\_cd\_aws\_sec\_group\_analytics\]|
|Databases|Single Score|Azure Database Analytics \[sn\_disco\_cd\_azure\_database\_analytics\]|
|Databases|Line|Azure Database Analytics \[sn\_disco\_cd\_azure\_database\_analytics\]|
|Datastore Disk|Single Score|VMWare Datastore Disk Analytics \[sn\_disco\_cd\_vmware\_ds\_disk\_analytics\]|
|Datastores|Single Score|VMware Datastore Analytics \[sn\_disco\_cd\_vmware\_datastore\_analytics\]|
|Disks|Line|Azure Disk Analytics \[sn\_disco\_cd\_azure\_disk\_analytics\]|
|Disks|Single Score|Azure Disk Analytics \[sn\_disco\_cd\_azure\_disk\_analytics\]|
|Distributed Virtual Port Groups|Single Score|VMware Distributed Virtual Port Group Analytics \[sn\_disco\_cd\_vmware\_dv\_port\_grp\_analytics\]|
|Distributed Virtual Switches|Single Score|VMWare Distributed Virtual Switch Analytics \[sn\_disco\_cd\_vmware\_dvs\_analytics\]|
|EC2 Instances|Single Score|AWS EC2 Instance Analytics \[sn\_disco\_cd\_aws\_ec2\_instance\_analytics\]|
|EC2 Instances|Line|AWS EC2 Instance Analytics \[sn\_disco\_cd\_aws\_ec2\_instance\_analytics\]|
|EC2 Instances|Pie|AWS EC2 Instance Analytics \[sn\_disco\_cd\_aws\_ec2\_instance\_analytics\]|
|ESX Servers|Single Score|ESX Server Analytics \[sn\_disco\_cd\_vmware\_esx\_analytics\]|
|ESX Servers|Line|ESX Server Analytics \[sn\_disco\_cd\_vmware\_esx\_analytics\]|
|Folders|Single Score|vCenter Folder Analytics \[sn\_disco\_cd\_vmware\_folder\_analytics\]|
|Functions|Single Score|Azure Function Analytics \[sn\_disco\_cd\_azure\_function\_analytics\]|
|Generic Cloud Resources|Single Score|AWS Generic Cloud Resource Analytics \[sn\_disco\_cd\_aws\_gen\_resource\_analytics\]|
|Generic Cloud Resources|Line|AWS Generic Cloud Resource Analytics \[sn\_disco\_cd\_aws\_gen\_resource\_analytics\]|
|Generic Cloud Resources|Single Score|Azure Generic Cloud Resource Analytics \[sn\_disco\_cd\_azure\_gen\_resource\_analytics\]|
|Images|Single Score|AWS Image Analytics \[sn\_disco\_cd\_aws\_image\_analytics\]|
|Images|Single Score|Azure Image Analytics \[sn\_disco\_cd\_azure\_image\_analytics\]|
|Lambdas|Single Score|AWS Lambda Analytics \[sn\_disco\_cd\_aws\_lambda\_analytics\]|
|Load Balancers|Line|AWS Load Balancer Analytics \[sn\_disco\_cd\_aws\_loadbalancer\_analytics\]|
|Load Balancers|Single Score|AWS Load Balancer Analytics \[sn\_disco\_cd\_aws\_loadbalancer\_analytics\]|
|Load Balancers|Single Score|Azure Load Balancer Analytics \[sn\_disco\_cd\_azure\_loadbalancer\_analytics\]|
|Load Balancers|Line|Azure Load Balancer Analytics \[sn\_disco\_cd\_azure\_loadbalancer\_analytics\]|
|Network Interfaces|Single Score|AWS Network Interface Analytics \[sn\_disco\_cd\_aws\_nw\_interface\_analytics\]|
|Network Interfaces|Single Score|Azure Network Interface Analytics \[sn\_disco\_cd\_azure\_nw\_interface\_analytics\]|
|Network Security Groups|Single Score|Azure Network Security Groups Analytics \[sn\_disco\_cd\_azure\_nw\_sec\_group\_analytics\]|
|Relational Database Services \(RDS\)|Line|AWS RDS Analytics \[sn\_disco\_cd\_aws\_rds\_analytics\]|
|Relational Database Services \(RDS\)|Single Score|AWS RDS Analytics \[sn\_disco\_cd\_aws\_rds\_analytics\]|
|S3 Buckets|Single Score|AWS S3 bucket Analytics \[sn\_disco\_cd\_aws\_s3\_bucket\_analytics\]|
|Storage Volumes|Single Score|AWS Storage Volume Analytics \[sn\_disco\_cd\_aws\_storage\_volume\_analytics\]|
|Storage Volumes|Line|AWS Storage Volume Analytics \[sn\_disco\_cd\_aws\_storage\_volume\_analytics\]|
|Virtual Machines|Line|Azure VM Analytics \[sn\_disco\_cd\_azure\_vm\_analytics\]|
|Virtual Machines|Single Score|Azure VM Analytics \[sn\_disco\_cd\_azure\_vm\_analytics\]|
|Virtual Machines|Pie|Azure VM Analytics \[sn\_disco\_cd\_azure\_vm\_analytics\]|
|Virtual Machines|Line|VMware VM Analytics \[sn\_disco\_cd\_vmware\_vm\_analytics\]|
|Virtual Machines|Pie|VMware VM Analytics \[sn\_disco\_cd\_vmware\_vm\_analytics\]|
|Virtual Machines|Single Score|VMware VM Analytics \[sn\_disco\_cd\_vmware\_vm\_analytics\]|
|All Virtual Machines|Line|VM Analytics \[sn\_disco\_cd\_vm\_analytics\]|
|Virtual Networks|Single Score|Azure Virtual Network Analytics \[sn\_disco\_cd\_azure\_virtual\_nw\_analytics\]|
|Virtual Private Clouds \(VPC\)|Line|AWS VPC Analytics \[sn\_disco\_cd\_aws\_vpc\_analytics\]|
|Virtual Private Clouds \(VPC\)|Single Score|AWS VPC Analytics \[sn\_disco\_cd\_aws\_vpc\_analytics\]|
|VM Templates|Single Score|VMWare VM Template Analytics \[sn\_disco\_cd\_vmware\_vm\_template\_analytics\]|

## Access the Cloud Resources dashboard

To access the Cloud Resources dashboard, navigate to **Discovery** &gt; **Cloud Resource Dashboard** or **Cloud Provisioning and Governance** &gt; **Cloud Resource Dashboard**.

## Customize the Cloud Resources dashboard

Customize your dashboard In each cloud provider tab by filtering these attributes:

-   Service Account: All the service accounts that are specific to the cloud provider tab selected are listed.
-   Datacenters: The datacenters are populated based on the cloud provider.
-   Resource Group: This filter is only applicable for Microsoft Azure and restricts objects and resources to the chosen resource group.

Use these database views with resource tags to create your own dashboard.

|Database View Table Name|Label|
|------------------------|-----|
|sn\_disco\_cd\_aws\_api\_gateway\_analytics\_tags\_db\_view|AWS API Gateway Analytics with Tags|
|sn\_disco\_cd\_aws\_ec2\_instance\_analytics\_tags\_db\_view|AWS EC2 Instance Analytics with Tags|
|sn\_disco\_cd\_aws\_gen\_resource\_analytics\_tags\_db\_view|AWS Cloud Resource Analytics with tags|
|sn\_disco\_cd\_aws\_image\_analytics\_tags\_db\_view|AWS Image Analytics with Tags|
|sn\_disco\_cd\_aws\_lambda\_analytics\_tags\_db\_view|AWS Lambda Analytics with Tags|
|sn\_disco\_cd\_aws\_loadbalancer\_analytics\_tags\_db\_view|AWS Load Balancer Analytics with Tags|
|sn\_disco\_cd\_aws\_nw\_interface\_analytics\_tags\_db\_view|AWS NW Interface Analytics with Tags|
|sn\_disco\_cd\_aws\_rds\_analytics\_tags\_db\_view|AWS RDS Analytics with Tags|
|sn\_disco\_cd\_aws\_s3\_bucket\_analytics\_tags\_db\_view|AWS S3 bucket Analytics with Tags|
|sn\_disco\_cd\_aws\_sec\_group\_analytics\_tags\_db\_view|AWS Security Group Analytics with Tags|
|sn\_disco\_cd\_aws\_storage\_volume\_analytics\_tags\_db\_view|AWS Storage Volume Analytics with Tags|
|sn\_disco\_cd\_aws\_vpc\_analytics\_tags\_db\_view|AWS VPC Analytics with Tags|
|sn\_disco\_cd\_aws\_zone\_analytics\_tags\_db\_view|AWS Zones Analytics with tags|

|Database View Table Name|Label|
|------------------------|-----|
|sn\_disco\_cd\_azure\_database\_analytics\_tags\_db\_view|Azure Database Analytics with Tags|
|sn\_disco\_cd\_azure\_disk\_analytics\_tags\_db\_view|Azure Disk Analytics with Tags|
|sn\_disco\_cd\_azure\_function\_analytics\_tags\_db\_view|Azure Function Analytics with Tags|
|sn\_disco\_cd\_azure\_gen\_resource\_analytics\_tags\_db\_view|Azure Cloud Resource Analytics with Tags|
|sn\_disco\_cd\_azure\_image\_analytics\_tags\_db\_view|Azure Image Analytics with Tags|
|sn\_disco\_cd\_azure\_loadbalancer\_analytics\_tags\_db\_view|Azure Load Balancer Analytics with Tags|
|sn\_disco\_cd\_azure\_nw\_interface\_analytics\_tags\_db\_view|Azure NW Interface Analytics with Tags|
|sn\_disco\_cd\_azure\_nw\_sec\_group\_analytics\_tags\_db\_view|Azure Security Group Analytics with Tags|
|sn\_disco\_cd\_azure\_virtual\_nw\_analytics\_tags\_db\_view|Azure Virtual NW Analytics with Tags|
|sn\_disco\_cd\_azure\_vm\_analytics\_tags\_db\_view|Azure VM Analytics with Tags|
|sn\_disco\_cd\_azure\_zone\_analytics\_tags\_db\_view|Azure Zones Analytics with Tags|

|Database View Table Name|Label|
|------------------------|-----|
|sn\_disco\_cd\_vmware\_cluster\_analytics\_tags\_db\_view|VMware Cluster Analytics with Tags|
|sn\_disco\_cd\_vmware\_datastore\_analytics\_tags\_db\_view|VMware Datastore Analytics with Tags|
|sn\_disco\_cd\_vmware\_ds\_disk\_analytics\_tags\_db\_view|VMware DatastoreDisk Analytics with Tags|
|sn\_disco\_cd\_vmware\_dvs\_analytics\_tags\_db\_view|VMware DVS Analytics with Tags|
|sn\_disco\_cd\_vmware\_dv\_port\_grp\_analytics\_tags\_db\_view|VMware DV Port Group Analytics with Tags|
|sn\_disco\_cd\_vmware\_esx\_analytics\_tags\_db\_view|VMware ESX Analytics with Tags|
|sn\_disco\_cd\_vmware\_folder\_analytics\_tags\_db\_view|VMware Folder Analytics with Tags|
|sn\_disco\_cd\_vmware\_network\_analytics\_tags\_db\_view|VMware Network Analytics with Tags|
|sn\_disco\_cd\_vmware\_vm\_analytics\_tags\_db\_view|VMware VM Analytics with Tags|
|sn\_disco\_cd\_vmware\_vm\_template\_analytics\_tags\_db\_view|VMware VM Template Analytics with Tags|

The below resources that are supported for GCP are populated by GCPResourcePopulateScheduledJob.

|Analytic Table|CMDB CI resources|
|--------------|-----------------|
|GCP VM Analytics \[sn\_disco\_cd\_gcp\_database\_analytics\]|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|GCP Storage Volume Analytics \[sn\_disco\_cd\_gcp\_storage\_volume\_analytics\]|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|GCP Database Analytics \[sn\_disco\_cd\_gcp\_database\_analytics\]|Cloud Database \[cmdb\_ci\_cloud\_database\]|
|GCP Virtual Network Analytics \[sn\_disco\_cd\_gcp\_virtual\_nw\_analytics\]|Cloud Network \[cmdb\_ci\_network\]|
|GCP Load Balancer Analytics \[sn\_disco\_cd\_gcp\_loadbalancer\_analytics\]|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|GCP Image Analytics \[sn\_disco\_cd\_gcp\_image\_analytics\]|Cloud OS Images \[cmdb\_ci\_cloud\_os\_images\]|
|GCP Generic Cloud Resource Analytics \[sn\_disco\_cd\_gcp\_gen\_resource\_analytics\]|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|
|GCP Network Interface Analytics \[sn\_disco\_cd\_gcp\_nw\_interface\_analytics\]|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|

## Scheduled jobs

|Job|Description|
|---|-----------|
|GCPResourcePopulateScheduledJob|Scheduled job that fetches and populates the GCP CI data in the analytics table.|
|AWSResourcePopulateScheduledJob|Scheduled job that fetches and populates the AWS CI data in the analytics table.|
|AzureResourcePopulateScheduledJob|Scheduled job that fetches and populates the Microsoft Azure CI data in the analytics table.|
|VMwareResourcePopulateScheduledJob|Scheduled job that fetches and populates the VMware CI data in the analytics table.|

Since a separate scheduled job is triggered every 30 minutes for each cloud provider, you can verify if the last job was successful. If the scheduled job was not successful, you can manually trigger the job by going to the **System Definition** &gt; **Scheduled Jobs**. Select the job for the affected cloud provide and click **Execute Now**.

The refresh jobs run every 30 minutes to populate and update the date in the analytics tables. You can increase this frequency to get more updated data.

Synchronization is needed if:

-   The Resource Status was updated from **installed** to another status \(for example, retired or canceled\).
-   Any new resources were recently discovered.

Synchronization is not needed if:

-   No resources were updated.
-   There are new resources which were not recently discovered.

**Important to note:**

-   Only one job can run at a time. For example, if an AWS job is already running, you cannot trigger another AWS job.
-   If the LDC and service account fields of a CI resource is empty, the resource may not be associated with any LDC in the CI Relationship \[cmdb\_rel\_ci\] table or the resource is a generic cloud resource of IAM type and the fields are empty.
-   Only the resources with installed status set to installed are counted and represented in the cloud resources dashboard widgets.
-   If a new resource is discovered after the scheduled job run, then the next scheduled job adds the resource details in the analytical tables.
-   If a job is marked as failed in the Cloud Dashboard Job Status \[sn\_disco\_cd\_cloud\_dashboard\_job\_status\] table, the reason for the failure is logged in the system logs. Filter the system log table by the job sys\_id to fetch the error message.
-   If IP-based discovery is used to discover the vCenter, the service account field of the VMware resource is left blank.
-   The System Administrator should not delete the records from the analytics table since records deleted from the analytics table are not populated again by the scheduled job. Deletion of records leads to data inconsistency in the analytics table.
-   To ensure complete refresh of the VMware records \(including the service accounts\) after changing the VMware resource discovery mechanism, delete the VMware records from the Cloud Dashboard Job Status \[sn\_disco\_cd\_cloud\_dashboard\_job\_status\] table and run the schedule job. In the Cloud Dashboard Job Status table, the provider field of all the VMware resources is set to **vmware**. You can use either vCenter IP discovery or service account discovery to discover the VMware resources.

