---
title: Cloud class
description: Description, identification rule, and other important schema structures for the CMDB cloud classes.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CMDB schema model, Explore, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Cloud class

Description, identification rule, and other important schema structures for the CMDB cloud classes.

For descriptions of common CMDB tables in a base system, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

![AWS/Azure/OpenStack class model.](../image/CloudAWS_Azure_OpenStack.png "AWS/Azure/OpenStack class model​")

![IBM Datacenter Cloud Schema model.](../image/IBMDatacenterCloudSchemamodel.png "IBM Datacenter Cloud Schema model")

![Google Datacenter Schema Model.](../image/GoogleDatacenterModel.png "Google Datacenter Schema Model")

## Cloud schema description

ServiceNow has extensive models of cloud environments including Amazon Web Services \(AWS\), Microsoft Azure service, Google Cloud Platform \(GCP\), and IBM Cloud. Focusing on the compute side, the models for cloud environments and for Virtual Servers are similar. For example, instances of Amazon Elastic Compute Cloud \(EC2\) and Microsoft® Azure Cloud Compute, are an extension of Virtual Machine instances, where CIs are typically created by connecting directly to cloud inventory. However, Virtual Machine instances do not represent actual usage of the cloud instance.

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] is the main class for tracking cloud accounts such as AWS, GCP, and Azure \(replacing for example, use of the cmdb\_ci\_aws\_account table for AWS\).

For example, you can represent a Linux guest host running on Amazon EC2 by the Server \[cmdb\_ci\_server\] class, with the **IsVirtual** attribute set to **true** and with the relationship Runs on:Runs to the EC2 instance. Integrating the AWS Config Service or the Amazon CloudWatch application, provides information on the EC2 object ID. Running Discovery or another discovery program on the guest Linux host, provides the **hostname**.

Ensure the following:

-   Getting the correct UUID which gets stored in the Serial Number \[cmdb\_serial\_number\] table.
-   Connecting/creating the cloud instance to Host OS, matching on the UUID/Object ID and creating the Runs On:Runs relationship.

​Also, there is a complete model of Storage, Networking, Lamda/Functions in addition to modeling of different regions using the concept of the table Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] with Hosts:HostedOn relationship with Compute, Storage, and such.

## Identification rule

The base system contains pre-defined identification rules for cloud schema classes. A cloud object requires the following identification items:​

-   Object ID: Which is synonymous with the IDs that cloud vendors use for each type of cloud resource, such as Azure Compute, EC2, and Amazon Simple Storage Service \(S3\).
-   Object ID is unique per region and therefore has dependent relationship requiring information from the Logical Datacenter \[cmdb\_ci\_logical\_data\_center\] table, about the region where the cloud resource is being hosted. For example, AWS Datacenter \[cmdb\_ci\_aws\_datacenter\], Azure Datacenter \[cmdb\_ci\_azure\_datacenter\], Google Datacenter \[cmdb\_ci\_google\_datacenter\] that are extended from Logical Datacenter.

    Logical Datacenter itself, has two identifier entries:​

    -   Object ID: Unique ID of the logical datacenter where applicable​
    -   Region: The region of the cloud resource
-   Logical Datacenter has a dependency on cloud service accounts​, which has two identifier entries:

    -   Object ID: Unique ID of the account where applicable.
    -   Account ID: The unique Account ID that encompasses the different cloud resources. Account ID is generally more applicable than Object ID.

For more information, see [CMDB Identification and Reconciliation \(IRE\)](c_CMDBIdentifyandReconcile.md).

