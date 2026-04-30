---
title: Day 2 operations using Workflow Studio subflow
description: Take advantage of the flow designer to automate your Day 2 operations. Quickly write a subflow that communicates with a Cloud API or a particular resource.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Day 2 operations using Workflow Studio subflow

Take advantage of the flow designer to automate your Day 2 operations. Quickly write a subflow that communicates with a Cloud API or a particular resource.

Day 1 operations provision resources in a cloud as part of ordering from the ServiceNow catalog or the cloud catalog. These operations result in a stack that contains a list of provisioned resources. Day 2 operations can be carried out on the resources that are part of the stack or the resources discovered by the system.

Previously, to execute Day 2 operations in Cloud Provisioning and Governance, you had to interact directly with the Cloud API \(CAPI\), which frequently meant that you had to write new APIs to support a new operation. You can now use subflows to map Day 2 operations and create REST endpoints that call cloud providers and trigger platform-specific actions.

## Learn more

To learn about flows, subflows, and actions in general, see:

-   [Exploring flows](https://www.servicenow.com/docs/access?context=exploring-flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
-   [Exploring subflows](https://www.servicenow.com/docs/access?context=exploring-subflows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
-   [Exploring actions](https://www.servicenow.com/docs/access?context=exploring-actions&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

