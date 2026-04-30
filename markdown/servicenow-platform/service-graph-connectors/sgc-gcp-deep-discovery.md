---
title: Deep discovery for Service Graph Connector for GCP
description: The SG-GCP Execute Patch Job and SG-GCP Get Patch Job scheduled import jobs enable deep discovery by running patch jobs at the GCP project level.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, GCP, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Deep discovery for Service Graph Connector for GCP

The SG-GCP Execute Patch Job and SG-GCP Get Patch Job scheduled import jobs enable deep discovery by running patch jobs at the GCP project level.

Deep discovery involves fetching server data. The deep discovery data populates host name, serial number, CPU data, TCP connections, and running processes data into the CMDB.

The Service Graph Connector for GCP uses OS Config Patch jobs on GCP projects to execute the deep discovery commands on the VMs. These patch jobs run independently on Linux and Windows VMs.

The following scheduled imports execute the OS Config Patch jobs, and then read and delete the output:

-   [SG-GCP Execute Patch Job](sgc-gcp-deep-discovery.md#section_kj4_kc3_cgc)
-   [SG-GCP Get Patch Job](sgc-gcp-deep-discovery.md#section_qh1_sc3_cgc)

## Deep discovery connection properties

|Connection property name|Connection property value|
|------------------------|-------------------------|
|Scripts Bucket Name|Name of the Cloud Storage Bucket where the deep discovery scripts are saved.|
|Outputs Bucket Name|Name of the output Cloud Storage Bucket.|
|Outputs Storage Path|Path of the output Cloud Storage Bucket.|
|Shell Script Object Path|Path of the deep discovery Shell script file.|
|Shell Script Generation Number|Number that is used to identify the versioning of the cloud storage object.|
|PowerShell Script Object Path|Path of the deep discovery PowerShell script file.|
|PowerShell Script Generation Number|Number that is used to identify the versioning of the cloud storage object.|

## SG-GCP Execute Patch Job

The SG-GCP Execute Patch Job scheduled import reads the path of the Shell and PowerShell scripts uploaded to the Cloud Storage Bucket and the generation numbers from the deep discovery connection properties. The scheduled import then runs the commands on Linux and Windows VMs separately.

In the Import Set table for the SG-GCP Execute Patch Job import schedule, each project will have two rows, one for Linux VMs and the other for Windows VMs. The **Import Set** rows remain in `Pending` state because no transformations are required for these rows. The **Import Set** rows include the patch job ID and the list of instances on which the deep discovery script is run. The output is stored in the Cloud Storage Bucket with the Object ID of the VMs on which the deep discovery commands are run.

## SG-GCP Get Patch Job

The SG-GCP Get Patch Job scheduled import reads the output of the commands that are run on the Linux and Windows VMs. The scheduled import reads the output from the output bucket and folder path that are specified in the deep discovery connection properties. The SG-GCP Get Patch Job scheduled import then deletes the output from the Cloud Storage Bucket. The **Import Set** rows are processed using Application Dependency Mapping \(ADM\) to populate the Server records with the data of the VMs on which deep discovery was run. The **Import Set** rows include VM data such as running processes, TCP connections, and CPU information.

## Application Dependency Mapping

Using the deep discovery information, Application Dependency Mapping \(ADM\) creates and classifies the following applications from the imported middleware information:

-   Apache Web Server
-   MongoDB Instance
-   MSFT SQL Instance
-   MySQL Instance
-   Nginx Web Server
-   Oracle Database Listener
-   Oracle Instance
-   PostgreSQL Instance
-   Tomcat

## Additional resource

[Service Graph Connector for GCP - Deep Discovery Setup Instructions \[KB2213095\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2213095) article in the Now Support Knowledge Base

**Parent Topic:**[Service Graph Connector for GCP reference](sgc-cmdb-gcp-reference.md)

**Related topics**  


[Service Graph Connector for GCP properties](../reference/cmdb-sgc-gcp-props.md)

