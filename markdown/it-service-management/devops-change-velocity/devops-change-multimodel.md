---
title: DevOps change models
description: DevOps Change Velocity enables you to use fit-for-purpose change models that allow better flexibility in defining change models or processes to reflect modern development practices.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 17
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# DevOps change models

DevOps Change Velocity enables you to use fit-for-purpose change models that allow better flexibility in defining change models or processes to reflect modern development practices.

## DevOps Change model overview

**Important:** For DevOps change requests, use the Change Management - Change Models feature, which provides greater flexibility to enable the change process flow in a way that is optimized for specific use cases. For more information, see [Change models](../../change-management/concept/change-models.md). The legacy Change Management - State Model is also supported. For more information, see [State model and transitions](../../change-management/concept/c_ChangeStateModel.md).

**Important:** The DevOps and DevOps Simplified change models are not supported for Argo CD and Split tool change requests.

Use fit-for-purpose change models with a suite of succinct flows and flow actions built in Flow Designer for specific use cases. Instead of using the legacy ITIL-based change processes that are predefined in change workflows \(Normal, Standard, and Emergency\), you can selectively transition to a wide range of models that are optimized for specific use cases. Change models can be created with states and rules that determine the transitions between the states. For information on change models, see [Change models](../../change-management/concept/change-models.md).

![Change models](../image/change-model-01.png)

You can use any of the base system change models including the DevOps or DevOps Simplified change models. To create a change request based on models, you can either configure the **Model** field in the Step form in ServiceNow, or pass the model sys\_id or name in the change step from your orchestration pipeline.

## Base system DevOps change models

Two change models, called DevOps and DevOps Simplified are included in the base system and are active by default for you to create a model based change request.

-   **Type compatibility flag**

    The type compatibility **com.snc.change\_management.change\_model.type\_compatibility** property is used to determine what kind of change requests \(type- or model-based\) will be created. Navigate to **System Properties &gt; All Properties** to set the value for this property. The default value of this property is False. This property enables change type compatibility for change models. When set to true, the change request can be created either as a type-based workflow or change models. When set to false, change request will be created only using change model.

    The change request will be created based on the configuration combination as defined in the following tables when the property is set to true or false.

<table id="table_vys_fhp_byb"><thead><tr><th>

Change attribute configured in the pipeline step in ServiceNow

</th><th>

Change attribute passed in the pipeline

</th><th>

Change attribute considered in change request creation

</th></tr></thead><tbody><tr><td>

Change model: &lt;any selected change model&gt;

</td><td>

Neither model nor change type is passed.

</td><td>

Model-based change request will be created

</td></tr><tr><td>

Change model: &lt;any selected change model&gt;

</td><td>

Type is passed. For example, Normal```
{
    "attributes": {
      "type": "normal"
    }
  }
```

</td><td>

Type-based change request will be created

</td></tr><tr><td>

Change model: &lt;any selected change model&gt; for example, Model 1.

</td><td>

Different model is passed. For example, Model 2.

```
{
    "attributes": {
      "chg_model": {
         "name": "Model 2"
        }
      }
  }
```

</td><td>

Change will be created based on Model 2

</td></tr><tr><td>

Change model: Not specified

 Change type: &lt;any selected change type&gt;

</td><td>

Neither model nor change type is passed

</td><td>

Type-based change request will be created

</td></tr><tr><td>

Change type: &lt;any selected change type&gt;

</td><td>

Model is passed. ```
{
    "attributes": {
      "chg_model": {
         "name": "DevOps"
      }
    }
  }
```

</td><td>

Model-based change request will be created

</td></tr><tr><td>

Change type: &lt;any selected change type&gt;. For example, Normal

</td><td>

Different type is passed. For example, Emergency.

```
{
    "attributes": {
      "type": "emergency"
    }
  }
```

</td><td>

Change request will be created based on Emergency type.

</td></tr></tbody>
</table><table id="table_d4k_b3s_cyb"><thead><tr><th>

Change attribute configured in the pipeline step in ServiceNow

</th><th>

Change attribute passed in the pipeline

</th><th>

Change attribute considered in change request creation

</th></tr></thead><tbody><tr><td>

Change model: &lt;any selected change model&gt;

</td><td>

Neither model nor change type is passed

</td><td>

Model-based change request will be created

</td></tr><tr><td>

Change model: &lt;any selected change model&gt;

</td><td>

Type is passed. For example, Normal```
{
    "attributes": {
      "type": "normal"
    }
  }
```

</td><td>

ErrorChange request can’t be created because the type compatibility flag is disabled. Enable the type compatibility flag in system properties or configure the change model in the step record in ServiceNow or enter the appropriate change model sys id or name in the pipeline.

For information on resolving this error, see [Common errors in DevOps Change Velocity](../reference/devops-reference-error-messages.md).

</td></tr><tr><td>

Change model: &lt;any selected change model&gt; for example, Model 1.

</td><td>

Different model is passed. For example, Model 2.

```
{
    "attributes": {
      "chg_model": {
         "name": "Model 2"
      }
    }
  }
```

</td><td>

Change will be created based on Model 2

</td></tr><tr><td>

Change model: Not specified

 Change type: &lt;any selected change type&gt;

</td><td>

Neither model nor change type is passed.

</td><td>

ErrorChange request can’t be created because either the change type or change model isn’t configured for the pipeline.

For information on resolving this error, see [Common errors in DevOps Change Velocity](../reference/devops-reference-error-messages.md).

</td></tr><tr><td>

Change type: &lt;any selected change type&gt;

</td><td>

Model is passed.```
{
    "attributes": {
      "chg_model": {
         "name": "DevOps"
      }
    }
  }
```

</td><td>

Model-based change request will be created

</td></tr><tr><td>

Change type: &lt;any selected change type&gt;. For example, Normal

</td><td>

Different type is passed. For example, Emergency.

```
{
    "attributes": {
      "type": "emergency"
    }
  }
```

</td><td>

ErrorChange request cannot be created because the type compatibility flag is disabled. Enable the type compatibility flag in system properties or configure the change model in the step record in ServiceNow or enter the appropriate change model sys id or name in the pipeline.

For information on resolving this error, see [Common errors in DevOps Change Velocity](../reference/devops-reference-error-messages.md).

</td></tr></tbody>
</table>
-   **Configuration of DevOps models**

    The base system change models have the **Implementation states** field value as Implement, and the **Record preset** field is selected as **Type=Normal** by default. The model states available for the DevOps change model are New, Assess, Authorize, Scheduled, Implement, Review, Closed, and Canceled. And the model states available for the DevOps Simplified change model are New, Authorize, Scheduled, Implement, Review, Closed, and Canceled. Depending on your requirements, you can modify the change models and configure the states and transitions for your specific use case.

    ![DevOps change model](../image/change-model-devops-02.png "DevOps Change Model")

    ![DevOps Simplified Change Model](../image/devops-simplified-model.png "DevOps Simplified Change Model")

    If you want to create your own model instead of using the base system DevOps models, see the instructions in the [Create a Change model](../../change-management/task/create-a-change-model.md) section.

    You can use record presets to configure change details for your change model. Whenever a change is created, these values will be automatically set on the change. You can set a record preset for any change field that exists in the change request.

    The following logic is considered for pre-filing the change details when creating a change request.

    -   If you have configured change details in the record preset, then you can’t override this value by passing change details from the pipeline.
    -   If change details aren’t configured in the record preset, then the values passed from the pipeline is considered for pre-filing the details in the change request.
    -   If change details are neither configured in the record preset nor passed from the pipeline, then the values configured in the Step form in ServiceNow are considered.
    |Change details configured in record preset in ServiceNow|Change details configured in Step form in ServiceNow|Change details passed in the pipeline|Change details pre-filled when change is created|
    |--------------------------------------------------------|----------------------------------------------------|-------------------------------------|------------------------------------------------|
    |Assignment group: DevOps Report|Assignment group: Not specified|Assignment group: Not specified|Assignment group will be pre-filled from the record preset in the change request|
    |Assignment group: Not configured|Assignment group: Not specified|Assignment group: DevOps Report|Assignment group will be pre-filled from the pipeline in the change request|
    |Assignment group: Not configured|Assignment group: DevOps Report|Assignment group: Not specified|Assignment group will be pre-filled from the Step form in the change request|


## DevOps Change model

The DevOps change model contains flows in the base system for state transition and change approvals. Each state in the DevOps model has its own flows and each flow will get triggered when the required conditions are met. Change approval \(auto or manual\) is based on the DevOps Model Change Policy. By default, the base system DevOps Model Change Policy only has the manual approval decision activated. When you are ready for more approval automation, you can modify the policy. The following flows explain the state transition and change approval behavior.

-   Change - DevOps - New: When the change request is created in the New state, this flow gets triggered. If it has an Assignment Group, then this flow updates the change state to Assess.
-   Change - DevOps - Assess: When the change request is in the Assess state, this flow gets triggered. There are two key actions in this flow - DevOps Gather Change Policy Data and Apply Change Approval Policy, which are used to retrieve the DevOps data associated with the change request and check whether the change request must be auto approved, auto rejected, or sent for manual approval. The change approval \(auto or manual\) happens as part of this flow in the Apply Change Approval Policy action based on the DevOps Model Change Policy. If the change is approved \(auto or manual\), it moves to the Authorize state. If the change is rejected, an email notification is sent to the user who requested the change and the change is moved back to the New state. ![Change - DevOps - Assess flow](../image/change-devops-assess.png)
-   Change - DevOps - Authorize: When the change request is in the Authorize state, this flow gets triggered. In the base system, you will notice that there are two key actions - DevOps Gather Change Policy Data and Apply Change Approval Policy, which are used to retrieve the DevOps data associated with the change request and check whether the change request must be auto approved, auto rejected, or sent for manual approval. The conditions in the DevOps Model Change Policy in the Apply Change Approval Policy action won't be met. So the change approval \(auto or manual\) in this flow will be skipped. This flow will only move the change request state to Scheduled that triggers the Change - DevOps - Schedule flow.

    **Note:** If your change process requires another approval, you can refer to this flow and customize the DevOps Model Change Policy according to your requirements.

-   Change - DevOps - Schedule: When the change request is in the Scheduled state, this flow gets triggered. When the planned start date is reached, the change is moved to the Implement state.
-   Change - DevOps - Implement: When the change request is in the Implement state, this flow gets triggered.

The DevOps Model Change Policy contains the following policy inputs:

-   is\_change\_with\_partial\_data
-   regression\_tests\_failed
-   code\_security
-   code\_coverage
-   total\_num\_of\_commits
-   tests\_passing\_percent
-   load\_tests\_failed
-   num\_of\_open\_incidents
-   num\_of\_outages\_in\_last\_7\_days
-   num\_of\_current\_outages
-   integration\_tests\_failed
-   commits\_without\_work\_item
-   change\_request
-   risk

The three outcomes for the DevOps Model Change Policy \(depending on the conditions that you specify\) are:

-   Auto approval: If the conditions specified in the policy are met, the change request is automatically approved.
-   Auto reject: If one or more of the conditions specified in the policy are not met, the change request is automatically rejected.
-   Manual approval: If one or more conditions need manual approval by a user or group, that is specified in the policy. Notifications are sent by the policy to the relevant users or groups to expedite the manual approval and progress the change request.

    **Note:** By default, the base system DevOps Model Change Policy only has the manual approval decision activated.


**Important:** When you use the base system DevOps model as is, the change approval is automated by default. If you do not want automated change approval, you can modify the DevOps Model Change Policy in a way it suits your current change process.

## DevOps Simplified model

The DevOps Simplified change model contains flows in the base system for state transition and change approvals. Each state in the DevOps Simplified model has its own flows and each flow will get triggered when the required conditions are met. Change approval \(auto or manual\) is based on the DevOps Simplified Model Change Policy. The following flows explains the state transition and change approval behavior.

-   Change - DevOps Simplified - New: When the change request is created in the New state, this flow gets triggered. If it has an Assignment Group, then this flow updates the change state to Assess.
-   Change - DevOps Simplified - Authorize: When the change request is in the Authorize state, this flow gets triggered. There are two key actions in this flow - DevOps Gather Change Policy Data and Apply Change Approval Policy, which are used to retrieve the DevOps data associated with the change request and check whether the change request must be auto approved, auto rejected, or sent for manual approval. The change approval \(auto or manual\) happens as part of this flow in the Apply Change Approval Policy action based on the DevOps Simplified Model Change Policy. If the change is approved \(auto or manual\), it moves to the Schedule state. If the change is rejected, an email notification is sent to the user who requested the change and the change is moved back to the New state.

    **Note:** If your change process requires another approval, you can refer to this flow and customize the DevOps Simplified Model Change Policy according to your requirements.

    ![Change - DevOps Simplified - Authorize flow](../image/change-devops-simplified-authorize.png)

-   Change - DevOps Simplified- Schedule: When the change request is in the Scheduled state, this flow gets triggered. When the planned start date is reached, the change is moved to the Implement state.
-   Change - DevOps Simplified - Implement: When the change request is in the Implement state, this flow gets triggered.

The DevOps Simplified Model Change Policy contains the following policy inputs:

-   is\_change\_with\_partial\_data
-   regression\_tests\_failed
-   code\_security
-   code\_coverage
-   total\_num\_of\_commits
-   tests\_passing\_percent
-   load\_tests\_failed
-   num\_of\_open\_incidents
-   num\_of\_outages\_in\_last\_7\_days
-   num\_of\_current\_outages
-   integration\_tests\_failed
-   commits\_without\_work\_item
-   change\_request
-   risk

The three outcomes for the DevOps Simplified Model Change Policy \(depending on the conditions that you specify\) are:

-   Auto approval: If the conditions specified in the policy are met, the change request is automatically approved.
-   Auto reject: If one or more of the conditions specified in the policy are not met, the change request is automatically rejected.
-   Manual approval: If one or more conditions need manual approval by a user or group, that is specified in the policy. Notifications are sent by the policy to the relevant users or groups to expedite the manual approval and progress the change request.

    **Note:** By default, the base system DevOps Simplified Model Change Policy only has the manual approval decision activated.


## Callback to resume the pipeline

In DevOps Change Velocity, the following considerations are made to send a callback request.

-   The implementation states is used to send a callback to the third-party orchestration tool. If only one implementation state is present in the change model, then an absolute comparison is made. When the change created by a change model reaches the implementation state that is set, a call back is sent to the third-party orchestration tool.

    **Note:** In change models, the Implementation states field can have one or more states. You can define the implementation states for each change model. For more information, see [State model and transitions](../../change-management/concept/c_ChangeStateModel.md).

-   If multiple implementation states are present in the change model, a call back is sent to the third-party orchestration tool in the state where implementation state is reached first.
-   If there’s no implementation state set on the change model, then the model states are checked for the **Implement** state. If the Implement state is present, then that is considered for call back to the third-party orchestration tool. If there’s no implement state in the model states as well, then the value present in the **sn\_devops.change\_request.implement\_state** property is considered. The value of the system property is -1 by default, which is the implement state.

**Note:** The Change – DevOps – Update execution state flow is used to send a callback to the third-party orchestration tool. This approval flow waits until the change request is in the Implement state. Once the change request reaches Implement state, this flow updates the Step Execution record to the appropriate \(approved, rejected, canceled\) state. The moment the Step Execution record is updated, the Change Control Callback flow is triggered to send the callback to the third-party tool.

## After upgrade

-   The **Change model** field will be displayed in the Step form. This won’t impact your existing type-based change creation process as the type compatibility property \(**com.snc.change\_management.change\_model.type\_compatibility**\) is true.
-   If you want to have a model-based change request, set the type compatibility property to false. The **Change model** field in the Step form will be required. For information on configuration combination based on the property, see the table [When the type compatibility property is set to False](devops-change-multimodel.md#table_d4k_b3s_cyb).

**Note:** If you’re an existing customer and zbooted your instance, or a new customer, you can create model-based change requests by default. However, you can create type-based change requests by setting the type compatibility property to true.

The following table explains how the change model feature works for new and upgrading customers.

<table id="table_ky5_z3j_w1c"><thead><tr><th>

New or upgrade instance

</th><th>

Type compatibility flag

</th><th>

Model or Type

</th><th>

State transition flows

</th><th>

Auto change approval flows

</th><th>

Callback to 3rd party

</th></tr></thead><tbody><tr><td>

zboot \(new or existing zbooted\)

</td><td>

false

</td><td>

DevOps model

</td><td>

-   Change request - DevOps - New
-   Change request - DevOps - Assess
-   Change request - DevOps - Authorize
-   Change request - DevOps - Schedule
-   Change request - DevOps - Implement

</td><td>

In the base system, change approval \(auto or manual\) happens through the Change request - DevOps - Assess flow. If you want another level of approval, you can refer to the Change request - DevOps - Authorize flow and customize the DevOps Model Change Policy accordingly.

</td><td>

See the [Note](devops-change-multimodel.md#note-callback) in the Callback section.

</td></tr><tr><td>

Upgrade

</td><td>

false

</td><td>

DevOps model

</td><td>

-   Change request - DevOps - New
-   Change request - DevOps - Assess
-   Change request - DevOps - Authorize
-   Change request - DevOps - Schedule
-   Change request - DevOps - Implement

</td><td>

In the base system, change approval \(auto or manual\) happens through the Change request - DevOps - Assess flow. If you want another level of approval, you can refer to the Change request - DevOps - Authorize flow and customize the DevOps Model Change Policy accordingly.

</td><td>

See the [Note](devops-change-multimodel.md#note-callback) in the Callback section.

</td></tr><tr><td>

zboot \(new or existing zbooted\)

</td><td>

false

</td><td>

DevOps Simplified model

</td><td>

-   Change request - DevOps - New
-   Change request - DevOps - Authorize
-   Change request - DevOps - Schedule
-   Change request - DevOps - Implement

</td><td>

In the base system, change approval \(auto or manual\) happens through the Change request - DevOps - Authorize flow. If you want another level of approval, you can customize the DevOps Simplified Model Change Policy accordingly.

</td><td>

See the [Note](devops-change-multimodel.md#note-callback) in the Callback section.

</td></tr><tr><td>

Upgrade

</td><td>

false

</td><td>

DevOps Simplified model

</td><td>

-   Change request - DevOps - New
-   Change request - DevOps - Assess
-   Change request - DevOps - Authorize
-   Change request - DevOps - Schedule
-   Change request - DevOps - Implement

</td><td>

In the base system, change approval \(auto or manual\) happens through the Change request - DevOps - Authorize flow. If you want another level of approval, you can customize the DevOps Simplified Model Change Policy accordingly.

</td><td>

See the [Note](devops-change-multimodel.md#note-callback) in the Callback section.

</td></tr><tr><td>

Upgrade

</td><td>

true

</td><td>

Type

</td><td>

Current behavior is continued

</td><td>

DevOps Change Request Manual Approval, or DevOps Change Request Minimal Automation Approval, or DevOps Change Request Advanced Automation Approval flows \(whichever flow is active\)

</td><td>

Change Control Callback flows

</td></tr></tbody>
</table>-   **[Update change model in pipeline](../task/update-change-model-in-pipeline.md)**  
Update the change model in your existing pipeline steps using the DevOps Pipeline Migration to Change Models catalog item.

**Parent Topic:**[Accelerating your DevOps change process](dev-ops-change-acceleration.md)

