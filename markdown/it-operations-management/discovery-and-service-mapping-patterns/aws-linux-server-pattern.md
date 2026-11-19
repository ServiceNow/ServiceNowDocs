---
title: AWS Linux Server pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Linux Server configuration items \(CIs\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/aws-linux-server-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-08-11"
reading_time_minutes: 3
keywords: [AWS Linux Server discovery, AWS Linux Server pattern, AWS SSM server CI, EC2 Linux server]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Linux Server pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Linux Server configuration items \(CIs\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Verify that AWS SSM is enabled**

    Verify that AWS Systems Manager \(AWS SSM\) is enabled on the Amazon Elastic Compute Cloud \(Amazon EC2\) instances.

-   **Enable Linux Server CI creation**

    Set the **sn\_itom\_pattern.aws\_cloud\_discovery\_populate\_server\_ci** system property to **true**. For more information, see [Configure Server CI creation during AWS cloud discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/configure-aws-server-ci-cloud-discovery.md).

-   **Verify SSM Agent execution context**

    The SSM Agent must run as root to retrieve the serial number using `dmidecode`. If your security policy restricts the SSM Agent to a non-root user, the pattern can't create a Server CI for that instance.

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the AWS - Linux Server \(LP\) pattern.

<table id="table_linux_server_main"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

OS-level hostname of the EC2 instance. If the **glide.discovery.hostname.include\_domain** property is set to false, the domain suffix is removed and only the short hostname is stored.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The EC2 instance ID.

</td></tr><tr><td>

Correlation ID \[correlation\_id\]

</td><td>

The EC2 instance ID.

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

BIOS serial number of the EC2 instance.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address of the EC2 instance.

</td></tr><tr><td>

CPU core count \[cpu\_core\_count\]

</td><td>

Number of vCPUs available to the EC2 instance.

</td></tr><tr><td>

CPU count \[cpu\_count\]

</td><td>

CPU count. The value is set to **1**.

</td></tr><tr><td>

RAM \(MB\) \[ram\]

</td><td>

Amount of memory available to the EC2 instance, in megabytes \(MB\).

</td></tr><tr><td>

Operating System \[os\]

</td><td>

Operating system of the server. The value is set to **Linux**.

</td></tr><tr><td>

Is Virtual \[virtual\]

</td><td>

Indicates that the server is a virtual machine. The value is set to **true**.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. The value is set to **Installed**.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. The value is set to **Operational**.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Serial number \[serial\_number\]|BIOS serial number of the EC2 instance.|
|Serial number type \[serial\_number\_type\]|Type of serial number. The value is set to **bios**.|
|Valid \[valid\]|Indicates that the serial number is active and valid. The value is set to **true**.|
|Configuration item \[cmdb\_ci\]|References the Linux Server \[cmdb\_ci\_linux\_server\] table.|

## CI relationships and references

The AWS - Linux Server \(LP\) pattern creates the following relationships and references to support AWS Linux Server discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Linux Server \[cmdb\_ci\_linux\_server\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Serial Number \[cmdb\_serial\_number\]|Configuration item \[cmdb\_ci\]|Linux Server \[cmdb\_ci\_linux\_server\]|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

