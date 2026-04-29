---
title: CI lookup rules for Microsoft Defender for Cloud Integration for Security Operations and Palo Alto Prisma Cloud
description: You can use the configuration item \(CI\) lookup rules for the Microsoft Defender for Cloud Integration and Palo Alto Prisma Cloud integrations to find a correct match to commonly used resource types in the Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# CI lookup rules for Microsoft Defender for Cloud Integration for Security Operations and Palo Alto Prisma Cloud

You can use the configuration item \(CI\) lookup rules for the Microsoft Defender for Cloud Integration and Palo Alto Prisma Cloud integrations to find a correct match to commonly used resource types in the Configuration Management Database \(CMDB\).

## Overview

The CI Lookup rules module contains the rules that help you to define the fields that have the matching data in the Configuration Management Database \(CMDB\). You can use these rules to identify the applications and application releases. All Microsoft Defender for Cloud Integration and Palo Alto Prisma Cloud assets are uniquely identified by the combination of their object ID, cloud account, and logical datacenter in the ServiceNow platform. ServiceNow discovery populates the resource ID in the `Object_id` column of the CMDB in different formats for the different resource types. The following table shows the object ID formats of commonly used resource types that the discovery service uses to populate in the `Object_id` column of the CI. Any scanner that wants to look up an asset of a particular resource type must search by using the right object ID format. You can get the right object ID format by looking into the object ID column of corresponding CMDB CI class and then try to construct the object ID using the values that are received from scanner.

|Resource Type|Format|
|-------------|------|
|AWS::EC2::Instance|Object ID|
|AWS::ElasticLoadBalancing::LoadBalancer|Load balancer name|
|AWS::S3::Bucket|arn:aws:s3:::&lt;Bucket Name&gt;|

The CI match for a test result may not be found accurately in the Configuration Management Database \(CMDB\) unless the same format of the `object_id` is used in the lookup rule. Most of the times, the OOB CI lookup rules find a match for the most commonly used resource types for Microsoft Defender for Cloud Integration and Palo Alto Prisma Cloud. If the following CI lookup rules aren’t finding the CIs in the CMDB for your test results, you can create a CI lookup rule for a resource type. For more information on how to create a CI lookup rule, see [Create a CI lookup rule](../../security-operations-common/task/create-ci-identifier-rules.md).

## CI lookup rules

The following CI lookup rules are specific to the Microsoft Defender for Cloud Integration and Palo Alto Prisma Cloud.

-   **__S3 Bucket__**

    This lookup rule attempts to find the CI in the CMDB by the value that was obtained by concatenating the `arn:aws:s3:::` and resource name. The obtained value is looked up in the `object_id` column of the `cmdb_ci_cloud_object_storage` table. This lookup rule applies only when the resource type is `AWS::S3::Bucket`.​

-   **__Name__**

    This lookup rule attempts to find the CI in the CMDB by name. The name, which is looked up in the `Object_id` column of the CI class, corresponds to a resource type in the `sn_capi_resource_type` table.

    **Note:** For the Palo Alto Prisma Cloud application, this CI lookup rule runs only for the `AWS::RDS::DBInstance`, `AWS::ElasticLoadBalancing::LoadBalancer`, and `AWS::CloudTrail::Trail` resource types​. You can add the resource types that you want to execute this CI lookup rule for.

-   **__Resource Id__**

    This lookup rule attempts to find the CI in the CMDB by the resource ID. The resource ID, which is looked up in the `Object_id` column of the CI class, corresponds to a resource type in the `sn_capi_resource_type` table.


**Note:** You can set the priority for a CI lookup rule in the **Order** field. The CI lookup rule with the least order value is executed first.

