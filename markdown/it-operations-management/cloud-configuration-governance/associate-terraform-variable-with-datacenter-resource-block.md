---
title: Associate the Terraform environment variable with the datacenter resource block
description: Associate the Terraform environment variable with the Cloud Provisioning and Governance datacenter resource block. After associating the environment variable, you can use it to pass custom inputs parameters during resource deployment through Terraform Enterprise.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Associate the Terraform environment variable with the datacenter resource block

Associate the Terraform environment variable with the Cloud Provisioning and Governance datacenter resource block. After associating the environment variable, you can use it to pass custom inputs parameters during resource deployment through Terraform Enterprise.

## Before you begin

Role required: admin

## About this task

To set the Terraform environment variable conditionally, use a scripted expression. For more information, see [Using expressions in Cloud Provisioning and Governance](../reference/expressions-cloud-mgt.md).

## Procedure

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal**.

    The Cloud Admin Portal opens in a new browser tab.

2.  Select **Design** &gt; **Resource Blocks**.

3.  Select the appropriate logical datacenter card.

4.  Set the logical datacenter resource block to the **Draft** state.

5.  Select the **Operations** tab.

6.  From the Interface drop-down list, select **Terraform Orchestration Interface**.

7.  Select **Steps** &gt; **Flow.Subflow.TFEProvision**.

8.  Set the **terraform\_variables** text box to the environment variable key value pair.

    For example: **\{"USER\_AGENT\_PROVIDER\_NAME":"AgentValue"\}**

9.  Set the logical datacenter resource block to the **Published** state.


**Parent Topic:**[Using Cloud Services Catalog Terraform Connector](../concept/using-ccg-terraform-connector.md)

