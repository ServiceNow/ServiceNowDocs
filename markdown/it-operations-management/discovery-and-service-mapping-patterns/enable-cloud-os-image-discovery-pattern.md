---
title: Enable Cloud OS Image discovery
description: Enable the Cloud OS Image \[cmdb\_ci\_cloud\_os\_image\] table to store the cloud OS image records for Amazon AWS Cloud, Microsoft Azure Cloud, Google Cloud Platform \(GCP\), Oracle Cloud Infrastructure \(OCI\), and IBM Cloud.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Discovery, Patterns, AWS, Azure, GCP, Cloud, Machine, Image]
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Enable Cloud OS Image discovery

Enable the Cloud OS Image \[cmdb\_ci\_cloud\_os\_image\] table to store the cloud OS image records for Amazon AWS Cloud, Microsoft Azure Cloud, Google Cloud Platform \(GCP\), Oracle Cloud Infrastructure \(OCI\), and IBM Cloud.

## Before you begin

-   Ensure that the latest versions of the following applications are installed:
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
-   Ensure that the application scope is the CMDB CI Class Models application.

**Note:** Cloud Provisioning and Governance \(CPG\) doesn’t support the New Cloud Image \(cmdb\_ci\_cloud\_os\_image\) table. If you’re currently utilizing CPG Provisioning flows or have intentions to do so, don’t migrate to the new Image Model.

Role required: admin

## About this task

Each cloud service provider offers OS images to launch a Compute/VM instance. Cloud Discovery stores the discovered Image \[cmdb\_ci\_os\_template\] table. This table is a dependent class on \[cmdb\_ci\_logical\_datacenter\] or \[cmdb\_ci\_cloud\_service\_account\]. The new Image model creates one record for each public Image \(object id\) irrespective of the service account and populates them in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. There for, the new model reduces the number of records in the CMDB

**Note:** If you have Discovery and Service Mapping Patterns version 1.10.0- November 2023, proceed to the following procedure. If you have an earlier version, see the Knowledge Base article [KB1000183](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1000183).

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** field, search for `sn_cmdb_ci_class.use_single_cloud_os_image`.

3.  Select the **sn\_cmdb\_ci\_class.use\_single\_cloud\_os\_image** property.

4.  In the **Value** field, enter `true`.

5.  Select **Update**.


## What to do next

1.  Clean up the Image records. For more information, see the Knowledge Base article [KB1537376](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1537376).
2.  Rerun the Cloud Discovery.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](../../service-mapping/concept/c_MappingPatternsCustomization.md)

**Previous topic:**[Activate a disabled pattern](../../service-mapping/task/activate-disabled-pattern.md)

**Next topic:**[ITOM Content Service](../concept/discovery-content-services.md)

