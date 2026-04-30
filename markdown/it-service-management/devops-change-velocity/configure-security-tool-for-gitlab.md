---
title: Integrate security tools with GitLab
description: Configure security tool for GitLab which is not supported in the base system.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [DevOps user-created security tool integration, User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# Integrate security tools with GitLab

Configure security tool for GitLab which is not supported in the base system.

## Before you begin

Role required: sn\_devops.admin

## Procedure

1.  Navigate to **DevOps &gt; Integrations &gt; Tool Integrations** and open the GitLab orchestration tool integration record.

2.  Navigate to the Tool Integration Capability Mappings related list.

3.  Select **New**, and enter the following values in the form fields.

    |Field|Value|
    |-----|-----|
    |Tool integration|GitLab|
    |Tool type capability|Security|

    ![Tool Integration Capability Mapping form for GitLab](../image/gitlab-security-01.png)

4.  Select **Submit**.

5.  Navigate to the Integration Capabilities related list, and select **New**.

6.  Enter the following values in the form fields.

<table id="simpletable_lsy_fjf_cyb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Tool integration

</td><td>

GitLab

</td></tr><tr><td>

Capability mapping

</td><td>

Capability mapping record created in step 4.

</td></tr><tr><td>

Action

</td><td>

Notification**Note:** Do not edit tool action records.

</td></tr><tr><td>

Active

</td><td>

Selected

</td></tr><tr><td>

Timeout \(ms\)

</td><td>

Timeout for the corresponding subflow. If execution of the subflow exceeds this value, a timeout exception occurs. Value is in milliseconds \(ms\). Default is 45,000 \(45 seconds\).

</td></tr><tr><td>

Subflow name

</td><td>

sn\_devops\_vul\_ints.devops\_security\_notification

</td></tr><tr><td>

Domain

</td><td>

global

</td></tr></tbody>
</table>    ![Integration capability form for GitLab](../image/gitlab-security-02.png)

    **Note:** Deactivate the **BR Seeded tool integrations not editable** business rule to integrate security tools with GitLab.

7.  Modify the **sn\_devops\_ints.DevOpsGitLabIntegrationHandler**script include by navigating to **System definitions &gt; Script include**, and searching for the **DevOpsGitLabIntegrationHandler** script.

    1.  Modify the handleEvent method to process the security scan results from the GitLab pipeline. Ensure that your security stage name in your GitLab pipeline is same as the name you update in the VERACODE\_STAGE\_NAME, CMARX\_ONE\_STAGE\_NAME, or CMARX\_SAST\_STAGE\_NAME variable in the handleEvent method. Replace the handleEvent method code with the following code snippet.

        ```
         handleEvent: function(eventGr) {
            try {
                var renameHandler = new sn_devops.DevOpsPipelineRenameHandler(this.refTable, this.appContext, this.relatedRecord);
                renameHandler.handlePipelineRename(eventGr);
                var payload = JSON.parse(eventGr.getValue("original_payload"));
                this._logger.debug("typeof payload >>" + typeof payload);
                if (!gs.nil(payload) && typeof payload === 'object') {
                    var status = this.getTaskExecutionStatus(payload);
                    this._logger.debug("Task Execution status -> " + status);
                    if (gs.nil(status))
                        this.updateInboundEvent(eventGr, {
                            processing_details: gs.getMessage('Task execution status [{0}] is not handled', payload.build_status),
                            state: sn_devops.DevOpsCommonConstants.INBOUND_EVENT_STATE_IGNORED
                        });
                    else {
                        // create fake start event for cancelled job
                        if (status == 'cancelled') {
                            this.createFakeEvent(eventGr, payload, 'running');
                        }
                        var normalizedObject = {};
                        normalizedObject.taskExecution = this.getTaskExecutionObject(eventGr, payload, status);
                        normalizedObject.orchestrationTask = this.getOrchestrationTaskObject(normalizedObject.taskExecution, payload);
                        normalizedObject.callback = this.getCallbackObject(normalizedObject.taskExecution, payload);
                        var devopsUtil = new sn_devops.DevOpsUtil(this.refTable, this.appContext, this.relatedRecord);
                        normalizedObject = devopsUtil.schemaValidationForTransformedPayload(normalizedObject);
                        var VERACODE_STAGE_NAME = 'SN_VERACODE';
                        var CMARX_ONE_STAGE_NAME = 'SN_CMARX_ONE_STAGE_NAME';
                        var CMARX_SAST_STAGE_NAME = 'SN_CMARX_SAST_STAGE_NAME';
                        if (!gs.nil(payload.build_stage) && 
                            (   
                                payload.build_stage == VERACODE_STAGE_NAME ||
                                payload.build_stage == CMARX_ONE_STAGE_NAME ||
                                payload.build_stage == CMARX_SAST_STAGE_NAME 
                            )
                            && this.isCompleted(normalizedObject.taskExecution)) {
                            var queryParams = sn_devops.DevOpsQueryParamsHelper.convertToSingular(JSON.parse(eventGr.getValue('query_params')));
                            if (gs.nil(normalizedObject.taskExecution.securityScan)) {
                                normalizedObject.taskExecution.securityScan = {
                                    securityScanSummaryCount: 0
                                };
                            }
                            normalizedObject.taskExecution.securityScan.securityScanSummaryCount += 1;
                        }
                        this._logger.debug("Normalized Object: " + JSON.stringify(normalizedObject));
                        return JSON.stringify(normalizedObject);
                    }
                } else
                    this.updateInboundEvent(eventGr, {
                        processing_details: gs.getMessage('Payload is missing or invalid'),
                        state: sn_devops.DevOpsCommonConstants.INBOUND_EVENT_STATE_ERROR
                    });
            } catch (error) {
                throw sn_devops.DevOpsErrorHelper.createDevOpsScriptIncludeError(error, sn_devops_ints.DevOpsIntegrationsCommonMessages.GITLAB_INBOUND_EVENT_PROCESS_ISSUE, "DevOpsGitLabIntegrationHandler.handleEvent", "handleEvent");
            }
        },
        ```

        In the following examples the GitLab pipeline shows that the security stage name is same as the VERACODE\_STAGE\_NAME, CMARX\_ONE\_STAGE\_NAME, or CMARX\_SAST\_STAGE\_NAME variables respectively in the handleEvent method.

        VERACODE\_STAGE\_NAME is for Veracode.

        ```
        image: maven:latest
        stages:
          - build
          - SN_VERACODE
          - Deploy
        
        build_1:
          stage: build
          tags:
            - local-runner1
          script:
            - echo "build"
            
        security_test:
          stage: SN_VERACODE
          tags:
            - local-runner1
          script:
            - |
              curl "https://<instance>.service-now.com/api/sn_devops/v1/devops/tool/security?toolId=<gitlab_tool_sys_id> " \
                --request POST \
                --header "Accept:application/json" \
                --header "Content-Type:application/json" \
                --data "{
                      \"pipelineInfo\": {
                        \"buildNumber\": \"${CI_JOB_ID}\",
                        \"taskExecutionUrl\": \"${CI_JOB_URL}/\"
                      },
                      \"securityResultAttributes\": {
                        \"scanner\": \"Veracode\",
                        \"applicationName\": \"Application\"
                      }
                    }" \
                --user 'devops.system':’password’
        
        
        ```

        CMARX\_ONE\_STAGE\_NAME is for Checkmarx One.

        ```
        image: maven:latest
        stages:
          - build
          - SN_CMARX_ONE_STAGE_NAME
          - Deploy
        
        build_1:
          stage: build
          tags:
            - local-runner1
          script:
            - echo "build"
            
        security_test:
          stage: SN_CMARX_ONE_STAGE_NAME
          tags:
            - local-runner1
          script:
            - |
              curl "https://<instance>.service-now.com/api/sn_devops/v1/devops/tool/security?toolId=<gitlab_tool_sys_id> " \
                --request POST \
                --header "Accept:application/json" \
                --header "Content-Type:application/json" \
                --data "{
                      \"pipelineInfo\": {
                        \"buildNumber\": \"${CI_JOB_ID}\",
                        \"taskExecutionUrl\": \"${CI_JOB_URL}/\"
                      },
                      \"securityResultAttributes\": {
                        \"scanner\": \"Checkmarx One\",
                        \"projectId\": \"projectId\",
                        \"scanId\": \"scanId\",
                      }
                    }" \
                --user 'devops.system':’password’
        ```

        CMARX\_SAST\_STAGE\_NAME is for Checkmarx SAST.

        ```
        image: maven:latest
        stages:
          - build
          - SN_CMARX_SAST_STAGE_NAME
          - Deploy
        
        build_1:
          stage: build
          tags:
            - local-runner1
          script:
            - echo "build"
            
        security_test:
          stage: SN_CMARX_SAST_STAGE_NAME
          tags:
            - local-runner1
          script:
            - |
              curl "https://<instance>.service-now.com/api/sn_devops/v1/devops/tool/security?toolId=<gitlab_tool_sys_id> " \
                --request POST \
                --header "Accept:application/json" \
                --header "Content-Type:application/json" \
                --data "{
                      \"pipelineInfo\": {
                        \"buildNumber\": \"${CI_JOB_ID}\",
                        \"taskExecutionUrl\": \"${CI_JOB_URL}/\"
                      },
                      \"securityResultAttributes\": {
                        \"scanner\": \"Checkmarx\",
                        \"projectId\": \"projectId\"
                      }
                    }" \
                --user 'devops.system':’password’
        ```

    2.  Add the getPipelineWithSecurityEventPayload method to the DevOpsGitLabIntegrationHandler script.

        ```
        getPipelineWithSecurityEventPayload: function(payload) {
                var gr = new GlideRecordSecure('sn_devops_task_execution');
                gr.addEncodedQuery("execution_url=" + payload.pipelineInfo.taskExecutionUrl);
                gr.query();
                var task = null;
                if (gr.next()) {
                    task = gr;
                }
                if (gs.nil(task) || gs.nil(task.orchestration_task) || gs.nil(task.orchestration_task.step)) {
                    throw "Pipeline Info not found";
                }
                var step = task.orchestration_task.step.getRefRecord();
                var pipelineDAO = new sn_devops.DevOpsPipelineDAO();
                var query = 'sys_id=' + step.pipeline;
                var pipeline = pipelineDAO.getLimitedRecordsByEncodedQuery(query);
                return pipeline;
            },
        
        ```


**Parent Topic:**[DevOps user-created security tool integration](../concept/devops-security-tool-integration.md)

