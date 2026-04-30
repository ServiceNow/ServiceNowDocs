---
title: Passing parameters to PaCE policies
description: Parameters can be passed to a PaCE policy to validate updates to an object \(tables and document IDs\). These variables apply to authoring in both low-code or JavaScript. Policy versions include three types of parameter inputs: API Variables, Config Parameters, and Record References.
locale: en-US
release: zurich
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Passing parameters to PaCE policies

Parameters can be passed to a PaCE policy to validate updates to an object \(tables and document IDs\). These variables apply to authoring in both low-code or JavaScript. Policy versions include three types of parameter inputs: API Variables, Config Parameters, and Record References.

## API Variables

Previously known as Caller Inputs, the API Variables is passed to the PaCE API at the time of invocation by a developer. The API Variable is a variable that enables you to pass the value to the policy whenever the policy is invoked. Specify a value for this API Variable when calling the API, otherwise the policy is not executed and no decision is reached. In the code editor, the variable name is `apiVars`.

For each PaCE policy, there is only one pre-defined API Variable called **SnapshotId**. This API Variable is Immutable and cannot be modified or deleted. You cannot define any additional API Variables for a policy.

## Config Parameters

Previously known as Mapped Inputs, the Config Parameters can be passed when mapping policies to an object \(tables and document IDs\). When you define a Config Parameter, you are creating a parameter that enables you to pass values to the policy whenever the policy is mapped. If you define mandatory inputs, you must specify values for these inputs when mapping the policy. If the inputs you define are not mandatory, the policy is not executed \(the status is set to inactive\) and no decision is reached. In the code editor, the variable name is `configParams`.

For example, for a travel expenses policy you can add variables to define the limits of different types of expenses. The limits are specified when mapping the policy, and set the limits on the expense when the policy is invoked on this object. The breakfast expense limit for one group of employees could be $25, and for a different group of employees the limit could be $50. Each time the policy is invoked, the expenses are validated by the policy according to the limits specified in the mapping.

## Record References

Record references define queries to extract data from any ServiceNow® tables and use the data to configure the policy logic. This feature enables you to retrieve additional data that may be required while defining the policy. You can define a query to perform aggregate functions for a record reference. In the code editor, the variable name is `recordRefs`.

## Data Collectors

The data collectors function collects input process data from ServiceNow or an external data source to provide an output. The output can be used in the policy logic to make a decision. You can define and manage data collectors by creating, editing, updating, and activating them to your policy builder.

Data collectors can be accessed by using the `dataCollectors` object in JavaScript.

**Note:** Auto-completion lists all possible outputs and data collectors that are available to use.

While editing a policy in low-code, an output of the configured data collectors is available under the drop-down menu.

