---
title: DevOps change request attributes
description: Add or update DevOps change request attributes using the changeInfo REST API, the Default Change Handler subflow, by passing attributes through the pipeline, Update function, or automated flows.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# DevOps change request attributes

Add or update DevOps change request attributes using the changeInfo REST API, the Default Change Handler subflow, by passing attributes through the pipeline, Update function, or automated flows.

## Specifying attributes

Use one of the following methods to specify change request attributes:

-   [DevOps - PUT /devops/orchestration/changeInfo/\{changeInfo\}](https://www.servicenow.com/docs/access?context=devops-api&version=yokohama&pubname=yokohama-api-reference&section=devops-PUT-orch-changeInfo&ft:locale=en-US) to update fields within a specified change request.

    **Note:**

    -   The changeInfo API won’t function when the pipeline is in the paused state.
    -   An API call can’t be executed while the pipeline is waiting.
    -   The API approach must be considered after thorough testing.
-   Default Change Handler subflow to populate change request fields with default values. For more information, see [Default Change Handler subflow](using-dev-ops-model-change-flow.md).
-   Passing the change attributes through the orchestration pipeline. For more information, see [Configuring DevOps change request details within the pipeline](dev-ops-config-change-details.md).
-   Passing the change attributes through the Update function in the orchestration pipeline function. For more information, see the following:
    -   [Get and update change request details in Azure DevOps pipeline](../task/update-change-request-details-in-an-azure-devops-pipeline.md)
    -   [Update change request details in Jenkins pipeline](../task/update-change-request-details-in-jenkins-pipeline.md)
    -   [ServiceNow DevOps custom actions from GitHub marketplace](servicenow-devops-custom-actions-from-github-marketplace.md#)
    -   [Implement custom actions for pipelines using a generic Docker container image](servicenow-custom-actions-for-gitlab.md)
-   Automated flows: DevOps approval flows to make changes in a change request. For more information, see [Flows](dev-ops-change-acceleration.md).

## Precedence of consideration

When the change attributes are specified through multiple methods, the precedence in which the attribute values are considered will vary. In ServiceNow, attributes can be specified in the pipeline step of DevOps Change Velocity, in the Default Change Handler subflow, or in an approval flow. In the orchestration tool pipeline, attributes can be passed in the pipeline step, or using the REST APIs. If a change model is used, they can also be specified in model presets.

See the following tables and examples to understand the precedence in which the values will be considered.

<table id="table_gzf_mzr_5dc"><thead><tr><th>

Change request

</th><th>

Precedence

</th></tr></thead><tbody><tr><td>

Standard

</td><td>

1.  Change attributes passed through pipeline
2.  Step record fields in ServiceNow
3.  Template passed in change attributes through pipeline
4.  Template in Step fields in ServiceNow

</td></tr><tr><td>

Non-standard

</td><td>

1.  Change attributes passed through pipeline
2.  Default Change Handler subflow &amp; approval flows

**Important:** Setting attribute values in both the Default Change Handler subflow and approval flows can cause conflicts because they might run simultaneously. Set the attribute values in only one source to avoid issues.

3.  Step record fields in ServiceNow
4.  Template passed in change attributes through pipeline
5.  Template in Step fields in ServiceNow

</td></tr></tbody>
</table><table id="table_tyh_31s_5dc"><thead><tr><th>

Change request

</th><th>

Precedence

</th></tr></thead><tbody><tr><td>

Standard

</td><td>

1.  Model Presets
2.  Change attributes passed through pipeline
3.  Step record fields in ServiceNow
4.  Template passed in change attributes through pipeline
5.  Template in Step fields in ServiceNow

</td></tr><tr><td>

Non-standard

</td><td>

1.  Model Presets
2.  Change attributes passed through pipeline
3.  Default Change Handler subflow &amp; approval flows

**Important:** Setting attribute values in both the Default Change Handler subflow and approval flows can cause conflicts because they might run simultaneously. Set the attribute values in only one source to avoid issues.

4.  Step record fields in ServiceNow
5.  Template passed in change attributes through pipeline
6.  Template in Step fields in ServiceNow

</td></tr></tbody>
</table>**Note:** If you have used business rules in your change operations, then you must set the **sn\_devops.change\_request.apply\_attributes\_on\_creation** property to true, so that the change attributes passed in the pipeline are set when the change request is created instead of the attributes being passed after the change request is created. For more information, see [DevOps Change Velocity properties](dev-ops-administration.md).

## Scenario 1

Consider a scenario where the attributes are specified in the Default change handler subflow in ServiceNow and in the Update function in the orchestration pipeline. Assume that the assignment\_group attribute is specified as “change mgmt” in the Default change handler subflow, and as “CAB” in the Update function in the pipeline. In this scenario, when the change is created, the value from the Default change handler subflow will be considered, and “change mgmt” will be the value considered for assignment\_group. Once the change is approved, and the pipeline is resumed, the value specified in the Update function will be considered, i.e. “CAB”.

## Scenario 2

Consider a scenario where the attributes are specified in the Default change handler subflow in ServiceNow and in the change step in the orchestration pipeline. Assume that the assignment\_group attribute is specified as “change mgmt” in the Default change handler subflow, and as “chg mgmt1” in the change step of the pipeline. In this scenario, when the change is created, the value from change step \(chg mgmt1\) will be considered, and then once the Default change handler subflow is triggered, the value considered will be “change mgmt”.

## Scenario 3

Consider a scenario where the attributes are specified through the template passed in change attributes and in the template of the step record. Assume that the assignment\_group attribute is specified as “change mgmt” in the template passed in change attributes, and as “chg mgmt1” in the template of the pipeline step record. In this scenario, when the change is created, the value from the template passed in change attribute \(chg mgmt\) will be considered.

## Scenario 4

Consider a scenario where the attributes are specified in the change attributes and the model preset for a model-based change. Assume that the assignment\_group attribute is specified as “change mgmt” in change attributes and as “chg mgmt1” in the model preset. In this scenario, when the change is created, the value from model preset \(chg mgmt1\) will be considered.

**Parent Topic:**[Accelerating your DevOps change process](dev-ops-change-acceleration.md)

