---
title: The Cloud Orchestration Trail
description: The Cloud Orchestration Trail is an activity log for all cloud resource activity on the instance.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Troubleshooting tools for Cloud Provisioning and Governance, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# The Cloud Orchestration Trail

The Cloud Orchestration Trail is an activity log for all cloud resource activity on the instance.

## Cloud Orchestration Trail contents

![The Cloud Orchestration Trail form](../image/cloud-orch-trail.png "Cloud orchestration trail form")

<table id="table_ewy_tll_3z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

An auto-generated number for the trail entry.

</td></tr><tr><td>

Level

</td><td>

One of the following: -   Debug
-   Info
-   Warn
-   Error

</td></tr><tr><td>

Template

</td><td>

The component, such as a resource block or blueprint, on which a Cloud Provisioning and Governance action was applied.

</td></tr><tr><td>

Template Instance

</td><td>

The datacenter in which the cloud resource is located.

</td></tr><tr><td>

User

</td><td>

The user involved in the transaction.

</td></tr><tr><td>

User group

</td><td>

The user group that the user belongs to.

</td></tr><tr><td>

Created

</td><td>

The date and time that the system created the entry.

</td></tr><tr><td>

Milestone

</td><td>

If this transaction is a milestone. You can configure the form to see this field.

</td></tr><tr><td>

Request Item

</td><td>

The service catalog request generated for the transaction.

</td></tr><tr><td>

Step

</td><td>

The step that identifies additional information about the transaction, including the component and the stage. You can configure the form to see this field.

</td></tr><tr><td>

Catalog Item

</td><td>

The catalog item, if any, that was involved in the execution.

</td></tr><tr><td>

Message

</td><td>

The error message or successful completion message. This could include items like the ID of the corresponding message in the Cloud API Trail record or the Cloud API that was invoked.

</td></tr><tr><td>

Message details

</td><td>

Details about the error, such as an HTTP error.

</td></tr></tbody>
</table>An example of an error message detail is as follows:

```
Failed to list loadbalancer Failed : HTTP error code : 403
```

This indicate that the credentials were incorrect, and Discovery could not access the cloud resource. The load balancer interface throws the first error because the load balancer device is the first device that allows access to the cloud resource.

A corresponding error on the MID- Server is captured in the Cloud API Trail.

## Steps, stages, and components

Each Cloud Orchestration entry has identifying attributes that explain what the triggering transaction was about. Steps group these attributes together and identify the component in the system that was involved in the transaction and the stage at which the transaction took place.

You can configure the Cloud Orchestration Trail form to show the **Step** field if it is not already visible.

|Step|Component|Stage|
|----|---------|-----|
|Apply API Parameter|CAPI Probe|Cloud API Orchestration|
|Apply Config Parameter|CAPI Probe|Cloud API Orchestration|
|Apply Endpoint Binding|CAPI Probe|Cloud API Orchestration|
|Apply Policy|Policy Engine|Workflow and Policy Execution|
|Apply Policy Rule Action|Policy Engine|Workflow and Policy Execution|
|Call Cloud API|BP DSL Executor|Cloud Orchestration|
|Call Cloud API Connector|CAPI Probe|Cloud API Orchestration|
|Check Cloud Match|BP DSL Validator|Cloud Orchestration|
|Check Datacenter Capacity|BP DSL Validator|Cloud Orchestration|
|Check Resource Block Policies|BP DSL Executor|Cloud Orchestration|
|Check User Permissions|BP DSL Validator|Cloud Orchestration|
|Check User Quota|BP DSL Validator|Cloud Orchestration|
|Complete Cloud Orchestration|BP DSL Executor|Cloud Orchestration|
|Execute Cat Item Policy|Dynamic Forms|Catalog Item Request|
|Execute Form Rules|Dynamic Forms|Catalog Item Request|
|Execute Resource Block Operation|BP DSL Executor|Cloud Orchestration|
|Execute Resource Instance Script|BP DSL Executor|Cloud Orchestration|
|Get Quota Details|Dynamic Forms|Catalog Item Request|
|Get Response|CAPI Orchestrator|Cloud API Orchestration|
|Handle Cloud API Response|BP DSL Executor|Cloud Orchestration|
|Handle Policy Execution Response|BP DSL Executor|Cloud Orchestration|
|Handle Response and Chunking|CAPI Probe|Cloud API Orchestration|
|Invoke Cloud Orchestration|Workflow Engine|Workflow and Policy Execution|
|Invoke Policy Engine|Workflow Engine|Workflow and Policy Execution|
|Invoke Pre-Process Workflow|Workflow Engine|Workflow and Policy Execution|
|Launch Cat Item|Catalog Item|Catalog Item Request|
|Notify Caller|CAPI Orchestrator|Cloud API Orchestration|
|Prepare BP Execution Plan|BP DSL Executor|Cloud Orchestration|
|Prepare Runnable API|CAPI Orchestrator|Cloud API Orchestration|
|Publish API Route Request|CAPI Orchestrator|Cloud API Orchestration|
|Send Cloud API Response|CAPI Probe|Cloud API Orchestration|
|Show Form with Filters|Dynamic Forms|Catalog Item Request|
|Submit Form|Catalog Item|Catalog Item Request|
|Validate Inputs|BP DSL Validator|Cloud Orchestration|

See [Use Cloud Root Cause Analysis reports](../task/use-cloud-root-call-analysis.md) for instructions on how to access reports related to the Cloud Orchestration Trail.

**Related topics**  


[The Cloud API Trail](cloud-api-trail.md#)

