---
title: Handling import failures for large GCP resources
description: Manage the data source failure when importing resources from GCP.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [GCP, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Handling import failures for large GCP resources

Manage the data source failure when importing resources from GCP.

When importing large GCP resources, the data sources in the Service Graph Connector for GCP might fail because of a Direct REST response exceeding the 1024-MB limit. For more information, see [REST step](https://www.servicenow.com/docs/access?context=rest-request-action-designer&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

You can use one or more of the following options to handle the REST response size limitation error in the Service Graph Connector for GCP:

-   [Save the response as an attachment](sgc-cmdb-large-data-vol.md#section_jcj_2gt_bzb)
-   [Modify the batch size](sgc-cmdb-large-data-vol.md#section_aqx_5gt_bzb)

## Save the response as an attachment

With the save response as an attachment feature, the response of each data source is temporarily stored as an attachment and after the response is read, the attachment is deleted automatically. The save response as an attachment feature is activated by default and is triggered by the **sn\_gcp\_integ.save\_rest\_response\_as\_attachment** system property.

As a user with the admin role, you can deactivate the save response as an attachment feature by setting the **sn\_gcp\_integ.save\_rest\_response\_as\_attachment** property to `false`. When the feature is deactivated and the response size is within the limit, the data sources run normally.

## Modify the batch size

By default, the maximum batch size of the environment variable for a data source is set to 100 records. You can reduce or increase the batch size based on the data volume. To manage the batch size of a data source, you must add a system property of integer type for the data source as described in the following table.

|Data source|System property|
|-----------|---------------|
|SG-GCP Cloud Database|sg\_gcp\_cloud\_db\_batch\_size|
|SG-GCP Cloud Function|sg\_gcp\_cloud\_function\_batch\_size|
|SG-GCP Cloud Object Storage|sg\_gcp\_object\_storage\_batch\_size|
|SG-GCP Kubernetes Cluster|sg\_gcp\_kubernetes\_cluster\_batch\_size|
|SG-GCP Kubernetes Cluster Role|sn\_gcp\_integ.sg\_gcp\_kubernetes\_cluster\_role\_batch\_size|
|SG-GCP Kubernetes Cluster Role Binding|sn\_gcp\_integ.sg\_gcp\_kubernetes\_cluster\_role\_binding\_batch\_size|
|SG-GCP Kubernetes Deployment|sg\_gcp\_kubernetes\_deployment\_batch\_size|
|SG-GCP Kubernetes Namespace|sg\_gcp\_kubernetes\_namespace\_batch\_size|
|SG-GCP Kubernetes Node|sg\_gcp\_kubernetes\_node\_batch\_size|
|SG-GCP Kubernetes Pod|sg\_gcp\_kubernetes\_pod\_batch\_size|
|SG-GCP Kubernetes Replicaset|sg\_gcp\_kubernetes\_replicaset\_batch\_size|
|SG-GCP Kubernetes Service|sg\_gcp\_kubernetes\_service\_batch\_size|
|SG-GCP Load Balancer|sg\_gcp\_load\_balancer\_batch\_size|
|SG-GCP Load Balancer Health Service|sg\_gcp\_lb\_health\_service\_batch\_size|
|SG-GCP Load Balancer Pool|sg\_gcp\_lb\_pool\_batch\_size|
|SG-GCP Load Balancer Pool Member|sg\_gcp\_lb\_pool\_member\_batch\_size|
|SG-GCP Load Balancer Service|sn\_gcp\_integ.sg\_gcp\_lb\_service\_batch\_size|
|SG-GCP Network|sg\_gcp\_network\_batch\_size|
|SG-GCP Kubernetes Node Pool|sn\_gcp\_integ.sg\_gcp\_kubernetes\_node\_pool\_batch\_size|
|SG-GCP Security Group|sg\_gcp\_security\_group\_batch\_size|
|SG-GCP Software Inventory|sg\_gcp\_software\_inventory\_batch\_size|
|SG-GCP Storage Volume|sg\_gcp\_storage\_volume\_batch\_size|
|SG-GCP Storage Volume Snapshot|sg\_gcp\_storage\_vol\_snapshot\_batch\_size|
|SG-GCP Subnet|sg\_gcp\_subnet\_batch\_size|
|SG-GCP VM Instance|sg\_gcp\_vm\_instance\_batch\_size|

**Note:** You must add these system properties as they aren't available by default. You must have the admin role to add or modify a system property. For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

