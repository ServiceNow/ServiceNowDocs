---
title: Day 2 operations using workflows
description: Take advantage of the workflows framework to automate your Day 2 operations. Quickly write a workflow that communicates with a Cloud API or a particular resource. Use SSH, PowerShell, or a similar tool, to access and then extend the workflow capabilities.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Day 2 operations using workflows

Take advantage of the workflows framework to automate your Day 2 operations. Quickly write a workflow that communicates with a Cloud API or a particular resource. Use SSH, PowerShell, or a similar tool, to access and then extend the workflow capabilities.

Day 1 operations provision resources in a cloud as part of ordering from the ServiceNow catalog or the cloud catalog. These operations result in a stack that contains a list of provisioned resources. Day 2 operations can be carried out on the resources that are part of the stack or the resources discovered by the system.

Previously, to execute Day 2 operations in Cloud Provisioning and Governance, you had to interact directly with the Cloud API \(CAPI\), which frequently meant that you had to write new APIs to support a new operation. With the ability to map Day 2 operations to workflows, you can now more easily use base-system workflow capabilities.

Capabilities include:

-   SSH/PowerShell to connect to a VM.
-   Use REST end points to call various Cloud Providers.
-   Invoke platform-specific features.

Rules with workflows

Cloud Provisioning and Governance supports using ServiceNow AI Platform rules with workflows. Rules are collections of conditions and actions. ​If all conditions of a rule evaluate to true, the system performs the actions. If any condition evaluates to false, the system does not perform the actions. Creating rules helps you track activities and more quickly respond to and resolve issues.

Learn more

To learn about workflows in general, see:

-   [Workflow overview](https://www.servicenow.com/docs/access?context=c_WorkflowOverview&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)
-   [Create a workflow from a table](https://www.servicenow.com/docs/access?context=t_CreateAWorkflowFromATable&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

To learn about how to work with variables in workflows, see:

-   [Workflow input variables](https://www.servicenow.com/docs/access?context=c_UsingVariablesInAWorkflow&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)
-   [Using variables in a workflow](https://www.servicenow.com/docs/access?context=c_UsingVariablesInAWorkflow&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

