---
title: Amazon MQ Broker pattern-based discovery
description: Discovery and Service Mapping Patterns finds Amazon MQ Brokers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-mq-broker.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-05-13"
reading_time_minutes: 3
keywords: [Amazon MQ Broker, AWS MQ discovery, AWS patterns, Amazon MQ Extended Inventory]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon MQ Broker pattern-based discovery

Discovery and Service Mapping Patterns finds Amazon MQ Brokers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns]().

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [AWS Resource Inventory discovery with Patterns]().

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts]().


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - MQ Broker - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

<table id="table_non_cmdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the broker.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\) of the broker.

</td></tr><tr><td>

Broker Id \[broker\_id\]

</td><td>

The unique ID of the broker.

</td></tr><tr><td>

Broker State \[broker\_state\]

</td><td>

The current state of the broker. For example: RUNNING, CREATION\_IN\_PROGRESS, DELETION\_IN\_PROGRESS, or REBOOT\_IN\_PROGRESS.

</td></tr><tr><td>

Engine Type \[engine\_type\]

</td><td>

The type of broker engine. For example: ACTIVEMQ or RABBITMQ.

</td></tr><tr><td>

Engine Version \[engine\_version\]

</td><td>

The version of the broker engine.

</td></tr><tr><td>

Host Instance Type \[host\_instance\_type\]

</td><td>

The broker's instance type, which determines the computing resources assigned to the broker.

</td></tr><tr><td>

Configuration Item \[configuration\_item\]

</td><td>

References the Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\] table.

</td></tr></tbody>
</table>## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - MQ Broker - Extended Inventory \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the broker.|
|Object ID \[object\_id\]|The ARN of the broker.|
|Type \[type\]|Type of resource. The value is set to **AWS::MQ::Broker**.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

## CI relationships

The Amazon AWS - MQ Broker - Extended Inventory \(LP\) pattern creates the following relationships and references to support Amazon MQ Broker discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|AWS MQ Broker \[cmdb\_aws\_mq\_broker\]|Configuration Item \[configuration\_item\]|Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\]|

## AWS Tag discovery

The Amazon AWS - MQ Broker - Extended Inventory \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Messaging Service \[cmdb\_ci\_cloud\_messaging\_service\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

