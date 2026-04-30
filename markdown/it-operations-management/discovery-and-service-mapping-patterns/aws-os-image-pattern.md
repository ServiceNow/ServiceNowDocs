---
title: AWS OS image pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS OS images \(both owned and executable\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-30"
reading_time_minutes: 3
keywords: [Amazon AWS - Executable Template, Amazon AWS - Owned Template, Amazon AWS - Executable Cloud OS Image, Amazon AWS - Owned Cloud OS Image, AWS OS image, AWS AMI, AWS discovery, AWS patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS OS image pattern-based discovery

Discovery and Service Mapping Patterns finds AWS OS images \(both owned and executable\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses the Amazon AWS - Owned Template \(LP\) and Amazon AWS - Executable Template \(LP\) patterns to discover AWS OS images from your AWS account. Owned images are custom images created by your AWS account, while executable images include public and shared images your account has permission to use.

When using the Image \[cmdb\_ci\_os\_template\] table to store Cloud OS Images, you may notice an unusually large number of records. To avoid this issue, you can store the discovered OS images in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. When enabled, Discovery launches the Amazon AWS - Owned Cloud OS Image \(LP\) and Amazon AWS - Executable Cloud OS Image \(LP\) patterns, which populate the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table. For more information, see [Enable Cloud OS Image discovery](../../discovery/task/enable-cloud-os-image-discovery-pattern.md).

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [Amazon AWS Cloud components discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the AWS OS image patterns.

<table id="table_os_image_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the image. For example: **CentOS 7.0-64 Minimal for VSI**.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier, allocated by Amazon AWS Cloud for this resource.

</td></tr><tr><td>

Image Type \[image\_type\]

</td><td>

Type of the OS image.

</td></tr><tr><td>

Root Device Type \[root\_device\_type\]

</td><td>

The device name of the root device volume. For example: **/dev/sda1**.

</td></tr><tr><td>

Image Source \[image\_source\]

</td><td>

Source of the OS image.

</td></tr><tr><td>

Guest OS \[guest\_os\]

</td><td>

Operating system that is secondary to the OS.

</td></tr><tr><td>

Provider \[provider\]

</td><td>

The cloud provider, which is **AWS**. This field is only populated in the Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.

</td></tr></tbody>
</table>## CI relationships

The AWS OS image patterns create these relationships to support AWS OS image discovery.

|CI|Relationship|CI|
|---|------------|---|
|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Key value \[cmdb\_key\_value\]|References|Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\]|

## AWS Tag discovery

The pattern extension section discovers tags and populates them in the Key value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.|

## AWS BYOL discovery

The pattern extension section discovers the following license types for Windows and Red Hat Enterprise Linux \(RHEL\) VMs:

-   Bring Your Own License \(BYOL\)
-   License included

The pattern stores the license type and model in the Key Value \[cmdb\_key\_value\] table.

<table id="table_jwc_kvk_k3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key \[key\]

</td><td>

The license type key, which is one of the following:-   Windows\_OS\_License\_Type\_automatic
-   RHEL\_OS\_License\_Type\_automatic

</td></tr><tr><td>

Value \[value\]

</td><td>

The license model, which is one of the following:-   BYOL
-   License Included

</td></tr><tr><td>

Configuration item \[configuration\_item\]

</td><td>

References the Image \[cmdb\_ci\_os\_template\] or Cloud Image \[cmdb\_ci\_cloud\_os\_image\] table.

</td></tr></tbody>
</table>**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

