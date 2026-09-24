---
title: AWS Host pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Dedicated Hosts in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-host-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 2
keywords: [Amazon AWS Host, AWS Dedicated Host discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Host pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Dedicated Hosts in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Host \(LP\) pattern.

<table id="table_mkf_2hc_dgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the host.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier, allocated by Amazon for this resource.

</td></tr><tr><td>

CPU Core Count \[cpu\_core\_count\]

</td><td>

The number of host cores.

</td></tr><tr><td>

State \[state\]

</td><td>

The current state of the host.

</td></tr><tr><td>

Host Type \[host\_type\]

</td><td>

Host type \(instance family\). For example: m5, c5.

</td></tr><tr><td>

Cloud Vendor \[cloud\_vendor\]

</td><td>

The cloud vendor: AWS.

</td></tr><tr><td>

Is Virtual \[virtual\]

</td><td>

Indicates whether this is a virtual host. The value is set to **false**.

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS - Host \(LP\) pattern creates the following relationships and references to support AWS Host discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Host \[cmdb\_ci\_cloud\_host\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Runs on::Runs|Cloud Host \[cmdb\_ci\_cloud\_host\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Host \[cmdb\_ci\_cloud\_host\]|

## AWS Tag discovery

The Amazon AWS - Host \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Host \[cmdb\_ci\_cloud\_host\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

