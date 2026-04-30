---
title: Pattern-based targeted discovery
description: Automatically discover the newly provisioned cloud resources and store their information in the ServiceNow ServiceNow Configuration Management Database \(CMDB\) by using pattern-based targeted discovery.Define a one-to-one association between the resource type and the single-resource-discovery pattern in the Cloud Resource Types \[sn\_capi\_resource\_type\] table. The pattern-based targeted discovery feature uses this information to invoke the appropriate pattern and discover the provisioned resource.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Pattern-based targeted discovery

Automatically discover the newly provisioned cloud resources and store their information in the ServiceNow® ServiceNow® Configuration Management Database \(CMDB\) by using pattern-based targeted discovery.

After the cloud provisions the resources mentioned in the resource template, such as Azure Resource Manager \(ARM\) or CloudFormation Template \(CFT\), it sends a response to the Cloud Provisioning and Governance application. The response contains information about the provisioned resources. Cloud Provisioning and Governance uses this information to launch a discovery—called targeted discovery—to discover only the newly provisioned or modified resources and update their attributes in the appropriate CMDB CI class.

The pattern-based targeted discovery offers an easier alternative to the existing CAPI-based approach. Cloud Provisioning and Governance uses single-resource-discovery patterns to discover only the newly provisioned or modified resources. Contrary to the other patterns, the single-resource-discovery pattern doesn’t scan the entire cloud landscape for changes. It only discovers the newly provisioned or modified resource of a given type.

The Cloud Resource Types \[sn\_capi\_resource\_type\] table stores the one-to-one association between the resource type and the single-resource-discovery pattern used to discover the resource. Cloud Provisioning and Governance uses the sn\_capi\_resource\_type table to identify the appropriate pattern for the given resource type. For more information on patterns, see [Discovery patterns used by ITOM Visibility](../../service-mapping/concept/c_MappingPatternsCustomization.md).

In the base system, Cloud Provisioning and Governance supports pattern-based targeted discovery for a wide variety of resource types. If required, you can use custom patterns that you created to perform targeted discovery. For more information, see [Associate a resource type with a single-resource-discovery pattern](pattern-based-targeted-discovery.md#).

Cloud Provisioning and Governance checks the following conditions to invoke the pattern-based targeted discovery:

-   The CAPI-based targeted discovery isn’t implemented for the resource type.
-   The **sn\_cmp.targeted.disco.patterns** system property is set to **True**.
-   The sn\_capi\_resource\_type table contains a one-to-one association between the resource type and the single-resource-discovery pattern.

For example, If you use CFT to provision an Amazon S3 bucket, Cloud Provisioning and Governance reads the resource type from the cloud response \(AWS::S3::Bucket\), and then identifies the appropriate pattern \( AWS S3\) from the sn\_capi\_resource\_type table. Then, it invokes the pattern to discover the newly provisioned Amazon S3 bucket only, and update its attributes in the appropriate CMDB CI class \(Cloud Object Storage \[cmbd\_ci\_cloud\_object\_storage\] table\).

If both CAPI-based targeted discovery and pattern-based targeted discovery are implemented for the resource type, then the system uses CAPI-based targeted discovery.

If both CAPI-based and pattern-based targeted discovery are not implemented for the resource type, the resource type is classified as a generic cloud resource in the Cloud Resources \[cmdb\_ci\_cmp\_resource\] table. In such cases, you can create a single-resource-discovery pattern and associate it with the resource type. For more information, see [Create or customize patterns](../../service-mapping/task/t_CreatePatternPatDef.md) and [Associate a resource type with a single-resource-discovery pattern](pattern-based-targeted-discovery.md#).

**Related topics**  


[Configure a response processor](../task/configure-response-processor.md)

[Create or extend a CAPI interface](../task/create-interface.md)

## Associate a resource type with a single-resource-discovery pattern

Define a one-to-one association between the resource type and the single-resource-discovery pattern in the Cloud Resource Types \[sn\_capi\_resource\_type\] table. The pattern-based targeted discovery feature uses this information to invoke the appropriate pattern and discover the provisioned resource.

### Before you begin

-   Ensure that the Cloud Provisioning and Governance application is deployed.
-   Ensure that the latest Discovery and Service Mapping is installed.
-   Ensure that the application scope is Cloud API.

Role required: sn\_cmp.cloud\_service\_designer or sn\_cmp.cloud\_admin

### Procedure

1.  Navigate to the sn\_capi\_resource\_type table.

2.  Select the appropriate resource type record.

3.  On the form, fill in the fields.

    The example values provided in this table establish a one-to-one relationship between the AWS::S3::Bucket resource type and its corresponding single-resource-discovery pattern \(Amazon AWS S3\).

<table id="table_cwg_14j_jrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Cloud resource type that you want to discoverExample: AWS::S3::Bucket

</td></tr><tr><td>

Product

</td><td>

\(Optional\) Product categoryExample: AWS Simple Storage Service

</td></tr><tr><td>

CI Class

</td><td>

CMDB CI table name. The system writes the discovered information into this table.Example: Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]

</td></tr><tr><td>

Pattern

</td><td>

A single-resource-discovery pattern to discover the resourceExample: Amazon AWS S3

</td></tr><tr><td>

Dependency sequence

</td><td>

\(Optional\) Order for triggering the pattern.

</td></tr></tbody>
</table>4.  Select **Update**.


