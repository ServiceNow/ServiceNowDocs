---
title: Configuring DevOps change request details within the pipeline
description: Configure how the closure information, change state, and change request fields are updated from within a pipeline in the change step of the pipeline.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Configuring DevOps change request details within the pipeline

Configure how the closure information, change state, and change request fields are updated from within a pipeline in the change step of the pipeline.

**Note:** Configuring change request details from within a GitLab pipeline isn’t supported.

The system variable, by default, points to the Default subflow to auto close a change in the base system. The **DevOps auto close change on pipeline completion subflow** \(**sn\_devops.auto\_close\_change**\) determines how the closure information, change state, and change request fields are updated when a pipeline is completed. If you want to specify a custom subflow that must be activated when a pipeline is completed, you can clone this subflow and customize it according to your requirements.

Closure information and change request attributes are contained with the **changeRequestDetails** object.

## Auto close change

Set the **autoCloseChange** parameter to `true/false` in the changeRequestDetails object when creating a change from a pipeline to update the **Close code** and **Close notes** fields and close the change request when a pipeline is completed. The **Actual start date** and **Actual end date** field values are also updated when the pipeline is completed. The date values are based on the pipeline's start time or the pipeline's first stage's start time, and the pipeline's end time or the pipeline's last stage's end time.

**Note:** If you want the change request start and end time to be considered instead of the pipeline’s, you can set the **sn\_devops.change\_request.auto\_close\_allow\_override\_start\_time** and **sn\_devops.change\_request.auto\_close\_allow\_override\_end\_time** property to false by navigating to **All &gt; System Properties &gt; All Properties**.

The close notes will be suffixed with text specifying that the closure information has been updated based on the Auto close change feature.

If set to true, the **Close code** and **Close notes** fields will be updated and the system will try to close the change request when the pipeline is completed.

If set to false, the **Close code** and **Close notes** fields will be updated when a pipeline is completed but the change request won’t be closed.

You can also set the **Auto close change** field value for a pipeline in the ServiceNow application. If you select **Update Change Only**, the **Close code** and **Close notes** fields will be updated when a pipeline is completed, and if you select **Update and Close Change**, the change request will also be closed along with updating the closure information.

Based on whether the auto close change is specified in the pipeline or column, the final state considered will be as follows:

|autoCloseChange flag in change request attributes|Auto Close Change column value \(sn\_devops\_pipeline\)|Final state|
|-------------------------------------------------|-------------------------------------------------------|-----------|
|True|Update Change Only|Updates change and moves state to close|
|False|Update and Close Change|Only updates the change|
|-|Update Change Only|Only updates the change|
|-|Update and Close Change|Updates change and moves state to close|

**Note:** The value specified for the autoCloseChange attribute in the pipeline takes precedence over the value specified in the Auto Close Change column in ServiceNow.

**Note:**

-   The auto close change feature is only applicable for basic pipelines with a single change created on it. If there are multiple changes, the latest change will be considered for auto close.
-   The auto close change feature isn’t supported for Jenkins freestyle pipelines and change requests where the change receipt feature is enabled.
-   For an Azure release pipeline, the pipeline completion state is derived by consolidating the state of each stage in the pipeline. If even one stage fails, the pipeline will be considered unsuccessful. If even one stage is partially successful, the pipeline will be considered successful with issues.

## Upgrade information

If you’re upgrading, you must re-configure your orchestration tool before setting the autoCloseChange parameter for GitHub and Azure build pipelines.

## Set Close Code

Set the **setCloseCode:** parameter to `true/false` based on the desired behavior. Default is true.

If set to true, the **Close code** and **Close notes** fields are updated as specified in the change step attributes and the change request is moved to post-implement when a stage is completed. You can override this behavior by enabling the **Auto close code** feature. The setCloseCode feature will get disabled when autoCloseChange is enabled and set to true or false. For more information, see [Auto Close Change](dev-ops-config-change-details.md#section_ts2_c1b_5yb). Use the autoCloseChange feature for more accurate change request details.

If set to false, when the job or pipeline has completed, the change request isn’t updated and remains in the Implement state.

-   Closure Information in the change request isn’t set \(**Close code** and **Close notes** fields are left empty\).
-   A link to the step execution is added to the **Work notes**.

## Change request fields

Set change request field values within the pipeline for the change request template specified.

-   Use the **attributes:** parameter to set field values.
-   Use the [DevOps - POST /devops/orchestration/changeControl](https://www.servicenow.com/docs/access?context=devops-api&version=australia&pubname=australia-api-reference&ft:locale=en-US) endpoint of the DevOps API.

**Note:**

-   If a specified field has a dependent field that is required, you must set that attribute as well.
-   If the attribute for the dependent required field isn’t set, change request and related step execution are canceled, and work notes are updated.

Field values within the **attributes:** parameter are key-value pairs. Meaning, the key is the field name within the template and the value is the information to populate in the field.

You can use the changeControl API to specify fields such as **type**, **cmdb\_ci**, **template**, **assignment\_group** **business\_service**, **standard\_change\_template**, **chg\_model** and create a change request.

When attributes are passed for change, the order of priority is as follows:

1.  Change request fields or changeControl API.
2.  Values in the Step record.
3.  Values provided in the Change Request template.

**Note:** When configuring change requests from within the pipeline, change type and template fields are always taken from one source. You can’t use a combination of attributes from the API request and the change request form.

All fields in the Change Request \[change\_request\] table are supported except where specified.

<table id="table_jtr_dbr_54b"><tbody><tr><td>

Unsupported fields

</td><td>

-   risk
-   impact
-   number
-   sys\_id
-   risk\_impact\_analysis

</td></tr><tr><td>

Supported fields

</td><td>

All remaining fields in the Change Request \[change\_request\] table.

</td></tr></tbody>
</table>**Note:** The attribute name must match the change request field name, and the value specified must be valid.

## Sample JSON payload

```
{
   "callbackURL":"http://192.168.0.4:3000/jenkins/sn-devops/pipeline_839b7605-b98d-4831-bc87-96829de7da37",
   "orchestrationTaskURL":"http://192.168.0.4:3000/jenkins/job/java_sample_tests#deploy/",
   "isMultiBranch":"false",
   "orchestrationTaskName":"java_sample_tests#deploy",
   "orchestrationTaskDetails":{
      "triggerType":"upstream",
      "upstreamTaskExecutionURL":"http://192.168.0.4:3000/jenkins/job/java_sample_tests/129/execution/node/35/wfapi/describe",
      "taskExecutionURL":"http://192.168.0.4:3000/jenkins/job/java_sample_tests/129/execution/node/50/wfapi/describe"
   },
   "changeRequestDetails":{
      "setCloseCode":false,
      "attributes":{
         "sys_created_by":"1832fbe1d701120035ae23c7ce610369",
         "sys_updated_by":"56826bf03710200044e0bfc8bcbe5dca",
         "requested_by":{
            "name":"Abel Tuter"
         },
         "watch_list":[
            {
               "name":"Abel Tuter"
            },
            {
               "name":"Aileen Mottern"
            },
            {
               "name":"Alejandra Prenatt"
            },
            "56826bf03710200044e0bfc8bcbe5dca"
         ],
         "work_notes_list":[
            "56826bf03710200044e0bfc8bcbe5dca",
            "46c6f9efa9fe198101ddf5eed9adf6e7",
            "d8f57f140b20220050192f15d6673a98"
         ],
         "assigned_to":"1832fbe1d701120035ae23c7ce610369",
         "category":"Service",
         "sys_created_on":"2021-02-09 18:58:41",
         "priority":"2",
      }
   }
}
```

## Pipeline examples

![DevOps Azure change details.](../image/dev-ops-azure-change-details.png "Change request details - Azure pipeline")

![JenkinsJobSettings.](../image/dev-ops-job-settings.png "Job-level settings — Jenkins")

![DevOps Jenkins change details.](../image/dev-ops-jenkins-change-details.png "Change request details - Jenkins")

![DevOps GitHub change details.](../image/auto-close-github.png "Change request details - GitHub")

**Parent Topic:**[Accelerating your DevOps change process](dev-ops-change-acceleration.md)

