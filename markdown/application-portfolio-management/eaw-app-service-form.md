---
title: Application service form
description: An application service is a configuration item \(CI\) that represents the operational view of a deployed application or your technology landscape. It logically models all technical components such as servers, databases, middleware, and configurations, that work together to deliver a specific business capability. Application services are linked to business applications in the CMDB.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Application service form

An application service is a configuration item \(CI\) that represents the operational view of a deployed application or your technology landscape. It logically models all technical components such as servers, databases, middleware, and configurations, that work together to deliver a specific business capability. Application services are linked to business applications in the CMDB.

## Application service form fields

|Field|Description|
|-----|-----------|
|Name|A unique, descriptive name that identifies the application service and distinguishes it from other services supporting the same business application.|
|Location|Specifies where the application service is hosted or primarily operated, such as a data center or geographic location.|
|Short Description|Briefly describes what this application service delivers or supports, such as the capability or function it enables.|
|Created|Date and time when the application service record was created. These fields are system‑generated and read‑only.|
|Created by|This is field is non-editable field.|
|Updated|Date and time when the application service record was last updated. These fields are system‑generated and read‑only.|
|Updated by|Name of the user who updated the application service.|
|Support group|The group responsible for supporting this application service during normal operations.|
|Supported by|Name of the user who supports the application service.|
|Managed by|Name of the user who manages the application service.|
|Managed by group|Name of the user group who manages the application service.|
|Environment|Indicates the deployment environment of the service, such as Development, Test, or Production.|
|Company|Name of the company.|
|Manufacturer|Name of the manufacturer.|
|Model ID|Model ID associated with the service.|
|Model number|Number of the Model.|
|Category|This field is auto-populated as Business Service.|
|Sub-category|This field is auto-populated as Service.|
|Department|Name of the department.|

|Field|Description|
|-----|-----------|
|Discovery source|Identifies the source that populated or last updated this application service record, such as ServiceNow Discovery or Service Mapping.|
|First discovered|Date when the application service was first identified by discovery processes. These values are typically system‑managed.|
|Most recent discovery|Date when the application service was most recently identified by discovery processes. These values are typically system‑managed.|
|Correlation ID|Enter the co-relation ID.|
|Skip sync|Option to select to skip the sync. This is a read-only field.|

|Field|Description|
|-----|-----------|
|Life Cycle Stage|Select the life cycle stage of the application service.|
|Life Cycle Stage Status|Select the status of the lifecycle stage.|
|Attested by|Name of the user who attested.|
|Attested Date|Date when the attestation is done.|
|Attestation Status|Select the attestation status as Attested or Rejected.|
|Install Status|Indicates whether the application service is currently deployed and available for use, such as Installed, In Maintenance, or Retired.|
|Operational status|Select the operational state of the application service.|
|Fault count|Number of faults or operational issues currently associated with this application service.|
|Maintenance schedule|Name of the maintenance schedule.|
|Schedule|Select the schedule for maintenance.|
|Requires verification|Option to select to request verification. This is a read-only field.|

|Field|Description|
|-----|-----------|
|Fully qualified domain name|Fully qualified domain name of the application service.|
|IP Address, MAC Address, and DNS Domain|Network attributes associated with the application service. These fields are usually populated automatically from the CMDB and are not manually maintained in Enterprise Architecture.|
|Serial number|Enter the serial number.|
|Attributes|Enter attributes names.|
|Comments|Add comments.|
|Monitor|Option to select monitor.|
|Can Print|Option to print the details.|

**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Add or edit an application service in the Enterprise Architecture Workspace](../../task/eaw-task/eaw-add-appl-service.md)

