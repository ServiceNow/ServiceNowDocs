---
title: Execute blueprint operations in parallel
description: You can execute your blueprint resource operations to run in a linear or in a parallel way.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-configuration-governance/execute-blueprint-operations-parallel.html
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Build a Cloud Provisioning blueprint, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Execute blueprint operations in parallel

You can execute your blueprint resource operations to run in a linear or in a parallel way.

## Before you begin

Role required: sn.cmp.cloud\_service\_designer.

## About this task

By default, the blueprint resource operations are listed serially and follow an order. You can run operations in parallel by arranging them in branches. Identify the operations specified in a blueprint that have no dependencies and can run in parallel. Arrange such operations in a single branch. The Blueprint Designer runs these operations together. If an error occurs in a branch, the operations in the affected branch cease to execute. However, the operations in the other branches, that are unaffected by the error, continue to execute. The parallel way of executing operations hence cuts down time in provisioning stacks.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Blueprints**.

2.  Click a blueprint, click the **Deployment Model** tab and then click **Operations**.

    All the operations for the blueprint are listed.

3.  Click an operation to view a graph.

    You can rearrange the graph by deleting and adding operations.

4.  Click **Optimize Plan** for the Cloud Provisioning and Governance application to suggest an optimized plan for you.

    The Cloud Provisioning and Governance application looks at the blueprint that you created and based on the attributes, the mappings, and the dependencies of each resource, the application suggests an optimized plan to execute.


**Parent Topic:**[Build a Cloud Provisioning blueprint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/create-blueprint-cmp.md)

**Related topics**  


[Add a resource operation to the execution plan]()

[Blueprint attributes]()

[Configure a blueprint rule]()

