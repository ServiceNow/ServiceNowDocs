---
title: Add support for minor or patch versions of the Terraform
description: Add minor or patch versions of the Terraform \(Terraform Open Source, Terraform Enterprise, or Terraform Cloud\) to the workload provider type record.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Cloud Provisioning and Governance: Terraform Connector, Cloud Provisioning and Governance: Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Add support for minor or patch versions of the Terraform

Add minor or patch versions of the Terraform \(Terraform Open Source, Terraform Enterprise, or Terraform Cloud\) to the workload provider type record.

## Before you begin

Role required: admin

## About this task

The base system Cloud Provisioning and Governance: Terraform Connector supports the following Terraform versions:

-   Terraform Open Source versions 1.1.0 through 1.1.9 and 1.2.0.
-   Terraform Enterprise versions 1.1.9 and 1.2.0.
-   Terraform Cloud versions 1.1.9 and 1.2.0

To use templates that are supported by a minor or patch version, for example version 0.12.29, add the version number to the Workload provider type record. Then, use the minor or patch versions to create configuration providers in Cloud Provisioning and Governance.

## Procedure

1.  Navigate to `https://<instance-name>/sn_cmp_workload_provider_type_list.do`

2.  Select the Terraform type whose minor or patch version that you want to use.

3.  Change the application scope to **Cloud Provisioning and Governance: Terraform Connector**.

4.  In the **Version** field of the Workload Config Provider Type form, enter the minor or patch versions as comma-separated values.

5.  Select **Submit**.


