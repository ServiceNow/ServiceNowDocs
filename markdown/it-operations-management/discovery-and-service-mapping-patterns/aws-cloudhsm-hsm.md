---
title: AWS CloudHSM hardware security module \(HSM\) pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [AWS, Discovery, ITOM, Pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS CloudHSM hardware security module \(HSM\) pattern-based discovery

Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](../discovery/reference/data-discovered-aws-patterns.md).

-   **Remove resources from the Resource Inclusion List table**

    Verify that the relevant resource isn't listed in the Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table to avoid duplicate discovery. For more information on removing resources from the Resource Inclusion List, see [AWS Resource Inventory discovery with Patterns](../service-mapping/reference/aws-resource-inventory.md).

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern](../service-mapping/task/activate-disabled-pattern.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](../it-operations-management/task/create-aws-service-accounts.md).


Discovery and Service Mapping Patterns application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

Discovery and Service Mapping Patterns application populates data in the non-CMDB table when running the Amazon AWS - CloudHSM HSM - Extended Inventory \(LP\) pattern.

You can review the non-CMDB AWS tables by navigating to **All** &gt; **Configuration** &gt; **AWS**. You can also search the navigation filter for the specific pattern name.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The unique identifier of the HSM within the cluster.

</td></tr><tr><td>

Availability Zone \[availability\_zone\]

</td><td>

The AWS availability zone where the HSM is deployed.

</td></tr><tr><td>

Status \[status\]

</td><td>

The current operational status of the HSM.

</td></tr><tr><td>

Cluster Id \[cluster\_id\]

</td><td>

The unique identifier of the HSM cluster.

</td></tr><tr><td>

Configuration Item \[configuration\_item\]

</td><td>

References the Cloud Resource \[cmdb\_ci\_cmp\_resource\] table.

</td></tr><tr><td>

Hsm Type \[hsm\_type\]

</td><td>

The type or model specification of the HSM device.

</td></tr><tr><td>

Object Id \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\) uniquely identifying the AWS CloudHSM HSM. The ARN consists of the discovered region, account ID, and HSM ID in the following format: **arn:aws:cloudhsm:&lt;region&gt;:&lt;account\_id&gt;:hsm/&lt;hsm\_id&gt;**.

</td></tr></tbody>
</table>## Data stored in CMDB tables

Discovery and Service Mapping Patterns application populates data in the CMDB when running the Amazon AWS - CloudHSM HSM - Extended Inventory \(LP\) pattern.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The unique identifier of the HSM within the cluster.

</td></tr><tr><td>

Resource type \[resource\_type\]

</td><td>

Type of resource. The value is set to **AWS::CloudHSM::HSM**.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The ARN uniquely identifying the AWS CloudHSM HSM. The ARN consists of the discovered region, account ID, and HSM ID in the following format: **arn:aws:cloudhsm:&lt;region&gt;:&lt;account\_id&gt;:hsm/&lt;hsm\_id&gt;**.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS - CloudHSM HSM - Extended Inventory \(LP\) pattern creates these relationships to support AWS CloudHSM HSM discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|AWS CloudHSM HSM \[cmdb\_aws\_cloudhsm\_hsm\]|References|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|

**Parent Topic:**[AWS discovery using patterns](../discovery/reference/data-discovered-aws-patterns.md)

