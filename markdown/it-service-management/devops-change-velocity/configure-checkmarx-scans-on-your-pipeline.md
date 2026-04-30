---
title: Configure Checkmarx scans on your pipeline
description: Configure Checkmarx scans on your Azure DevOps, Jenkins, GitHub, GitLab, or Harness pipelines.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Checkmarx, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure Checkmarx scans on your pipeline

Configure Checkmarx scans on your Azure DevOps, Jenkins, GitHub, GitLab, or Harness pipelines.

You can configure Checkmarx scans on any stage of the pipeline and the scan details are retrieved from the corresponding stage to DevOps Change Velocity. If you’re using Azure DevOps or GitHub Actions orchestration tools, then you must add the custom action code in your pipeline always. If you’re using Jenkins, and your pipeline already has a Checkmarx One security scan \(checkmarxASTScanner\) step, you don’t have to add the custom action code in your pipeline. For Checkmarx SAST, the custom action code must be added in your pipeline even if it has the security scan step \(checkmarxASTScanner\).

If you want to configure Checkmarx for the GitLab tool, you can either use the generic Docker container image to add the Checkmarx security step or perform the steps specified in the [Integrate security tools with GitLab](../task/configure-security-tool-for-gitlab.md) topic.

For Harness pipelines, you can configure Checkmarx scans only through the generic Docker Container Image. For more information, see [Implement custom actions for pipelines using a generic Docker container image](servicenow-custom-actions-for-gitlab.md).

1.  Navigate to the step in your pipeline and add the custom action.

<table id="choicetable_mt3_1xl_1yb"><tbody><tr><td>

Azure DevOps

</td><td>

1.  Navigate to your pipeline .yml file.
2.  In the **Tasks** section on the right side, search for the **ServiceNow DevOps Security Results** extension task.
3.  Enter the ServiceNow endpoint.
4.  Enter the Security results attributes as the following.
    -   Checkmarx SAST

        ```
- task: ServiceNow-DevOps-Build-Security-Results@1
    inputs:
      connectedServiceName: "" # ServiceNow DevOps Change Velocity Service Connection
      securityResultAttributes: |
        {"scanner": "Checkmarx SAST",  "projectId": "", "securityToolId": ""}
      # scanner: Scanning tool and is required e.g. Checkmarx SAST.
      # projectId: Id of your Checkmarx SAST project and is required. This attribute is applicable only for Checkmarx SAST.
      # securityToolId: Security tool onboarded in ServiceNow (sys_id of the onboarded security tool) and is optional.
        ```

    -   Checkmarx One

        ```
- task: ServiceNow-DevOps-Build-Security-Results@1
    inputs:
      connectedServiceName: "" # ServiceNow DevOps Change Velocity Service Connection
      securityResultAttributes: |
        {"scanner": "Checkmarx One", "projectName": "", "projectId": "", "scanId": "", "securityToolId": ""}
      # scanner: Scanning tool and is required e.g. Checkmarx One.
      # projectName: Name of your Checkmarx One project and is required. This attribute is applicable only for Checkmarx One.
      # projectId: Id of your Checkmarx One project and can be used instead of projectName field. This attribute is applicable only for Checkmarx One.
      # scanId: Checkmarx One scan id and is optional. This attribute is applicable only for Checkmarx One.
      # securityToolId: Security tool onboarded in ServiceNow (sys_id of the onboarded security tool) and is optional.
        ```

5.  Select **Add** to add the custom action code to your pipeline.


</td></tr><tr><td>

Jenkins

</td><td>

1.  Navigate to the Pipeline Syntax from a configured pipeline.
2.  Select the **snDevOpsSecurityResult** step from the **Sample Step** list, and update the values for the security scan attributes in the step.
3.  Select **Generate Pipeline Script** to create a snippet. You can copy and paste the snippet into the pipeline.
    -   Checkmarx SAST

        ```
snDevOpsSecurityResult securityResultAttributes: '{"scanner": "Checkmarx SAST", "projectId": "", "securityToolId": ""}'
// scanner: Scanning tool and is required e.g. Checkmarx SAST.
// projectId: Id of your Checkmarx SAST project and is required. This attribute is applicable only for Checkmarx SAST.
// securityToolId: Security tool onboarded in ServiceNow (sys_id of the onboarded security tool) and is optional.
        ```

    -   Checkmarx One

        ```
snDevOpsSecurityResult securityResultAttributes: '{"scanner": "Checkmarx One", "projectName": "", "projectId": "", "scanId": "", "securityToolId": ""}'
// scanner: Scanning tool and is required e.g. Checkmarx One.
// projectName/projectId: Name/Id of your Checkmarx One project and is required. This attribute is applicable only for Checkmarx One.
// scanId: Checkmarx One scan id and is optional. This attribute is applicable only for Checkmarx One.
// securityToolId: Security tool onboarded in ServiceNow (sys_id of the onboarded security tool) and is optional.
        ```

</td></tr><tr><td>

GitHub Actions

</td><td>

1.  Navigate to your workflow .yml file.
2.  In the **Marketplace** section on the right side, search for the **ServiceNow DevOps Security Results** custom action.
3.  Add the following snippet into your .yml file.
    -   Checkmarx SAST

        ```
ServiceNowSecurityScanResults:
    # jobs that must complete successfully before this job will run
    needs: build
    # type of machine to run the job on
    runs-on: ubuntu-latest
    name: ServiceNow Security Scan Results
    steps:
      - name: ServiceNow DevOps Security Results
        uses: ServiceNow/servicenow-devops-security-result@v3.0.0
        with:
            # Devops Integration User Name
            devops-integration-user-name: ${{ secrets.SN_DEVOPS_USER }}
            # Devops Integration User Password
            devops-integration-user-password: ${{ secrets.SN_DEVOPS_PASSWORD }}
            # ServiceNow Instance URL
            instance-url: ${{ secrets.SN_INSTANCE_URL }}
            # Orchestration Tool Id
            tool-id: ${{ secrets.SN_ORCHESTRATION_TOOL_ID }}
            # GitHub Context
            context-github: ${{ toJSON(github) }}
            # Display Name of the Job
            job-name: 'ServiceNow Security Scan Results'
            security-result-attributes: '{"scanner": "Checkmarx SAST", "projectId": "", "securityToolId": ""}'
            # scanner: Scanning tool and is required e.g. Checkmarx SAST.
            # projectId: Id of your Checkmarx SAST project and is required. This attribute is applicable only for Checkmarx SAST.
            # securityToolId: Security tool onboarded in ServiceNow (sys_id of the onboarded security tool) and is optional.
        ```

    -   Checkmarx One

        ```
ServiceNowSecurityScanResults:
    # jobs that must complete successfully before this job will run
    needs: build
    # type of machine to run the job on
    runs-on: ubuntu-latest
    name: ServiceNow Security Scan Results
    steps:
      - name: ServiceNow DevOps Security Results
        uses: ServiceNow/servicenow-devops-security-result@v3.0.0
        with:
            # Devops Integration User Name
            devops-integration-user-name: ${{ secrets.SN_DEVOPS_USER }}
            # Devops Integration User Password
            devops-integration-user-password: ${{ secrets.SN_DEVOPS_PASSWORD }}
            # ServiceNow Instance URL
            instance-url: ${{ secrets.SN_INSTANCE_URL }}
            # Orchestration Tool Id
            tool-id: ${{ secrets.SN_ORCHESTRATION_TOOL_ID }}
            # GitHub Context
            context-github: ${{ toJSON(github) }}
            # Display Name of the Job
            job-name: 'ServiceNow Security Scan Results'
            security-result-attributes: '{"scanner": "Checkmarx One", "projectName": "", "projectId": "", "scanId": "", "securityToolId": ""}'
            # scanner: Scanning tool and is required e.g. Checkmarx One.
            # projectName/projectId: Name/Id of your Checkmarx One project and is required. This attribute is applicable only for Checkmarx One.
            # scanId: Checkmarx One scan id and is optional. This attribute is applicable only for Checkmarx One.
            # securityToolId: Security tool onboarded in ServiceNow (sys_id of the onboarded security tool) and is optional.
        ```

For more information, see [GitHub marketplace](https://github.com/ServiceNow/servicenow-devops-security-result).

</td></tr><tr><td>

Harness

</td><td>

Run the generic Docker Container Image to use the following script. For more information, see [Implement custom actions for pipelines using a generic Docker container image](servicenow-custom-actions-for-gitlab.md).```
- stage:
    name: ServiceNow DevOps Security Result
    identifier: Security
    description: ""
    type: Custom
    spec:
      execution:
        steps:
          - stepGroup:
              name: Security
              identifier: Security
              steps:
                - step:
                    type: Run
                    name: ServiceNow DevOps Security Result
                    identifier: ServiceNow_DevOps_Security_Result
                    spec:
                      connectorRef: docker_hub_connector_for_harness
                      image: servicenowdocker/sndevops:5.0.0
                      shell: Sh
                      command: |-
                        sndevopscli create securityScan -p  

                        "{"pipelineInfo":{
                            "buildNumber":"<+stage.nodeExecutionId>",
                            "taskExecutionUrl":"<+pipeline.executionUrl>?stage=<+stage.nodeExecutionId>", 
                            "orchestrationPipeline":"<+org.identifier>/<+project.identifier>/<+pipeline.name>" 
                          },
                          "securityResultAttributes":{
				"scanner":"Veracode",
				"applicationName":"",
				"buildVersion":"",
				"securityToolId":""
                          }
                        }"
                      envVariables:
                        SNOW_URL: <+variable.SNOW_URL>
                        SNOW_TOOLID: <+variable.SNOW_TOOLID>
                        SNOW_TOKEN: <+variable.SNOW_TOKEN>
              stepGroupInfra:
                type: KubernetesDirect
                spec:
                  connectorRef: kubernates_connector
                  namespace: harness-delegate-ng
    tags: {}
```

</td></tr></tbody>
</table>2.  Run the pipeline to retrieve the security scan results.

**Parent Topic:**[Checkmarx integration with DevOps Change Velocity](checkmarx-integration-with-devops-change-velocity.md)

