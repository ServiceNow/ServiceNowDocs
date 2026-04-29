---
title: Configure Veracode scans on your pipeline
description: Configure Veracode scans on your Azure DevOps, Jenkins, GitHub, GitLab, or Harness pipelines.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Veracode, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure Veracode scans on your pipeline

Configure Veracode scans on your Azure DevOps, Jenkins, GitHub, GitLab, or Harness pipelines.

You can configure Veracode scans on any stage of the pipeline and the scan details are retrieved from the corresponding stage to DevOps Change Velocity. If you are using Azure DevOps or GitHub Actions orchestration tools then you need to add the custom action code in your pipeline always. If you are using Jenkins, and your pipeline already has a Veracode security scan step, you do not have to add the custom action code in your pipeline. Ensure that your Veracode security scan step has waitForScan: true. This is required for the system to retrieve the scan information.

If you want to configure Veracode for the GitLab tool, you can either use the generic Docker container image to add the Veracode security step or perform the steps specified in the [Integrate security tools with GitLab](configure-security-tool-for-gitlab.md) topic.

For Harness pipelines, you can configure Veracode scans only through the generic Docker Container Image. For more information, see [Implement custom actions for pipelines using a generic Docker container image](../concept/servicenow-custom-actions-for-gitlab.md).

1.  Navigate to the step in your pipeline and add the custom action.

<table id="choicetable_mt3_1xl_1yb"><tbody><tr><td>

Azure DevOps

</td><td>

1.  Navigate to your pipeline .yml file.
2.  In the **Tasks** section on the right side, search for the **ServiceNow DevOps Security Results** extension task.
3.  Enter the ServiceNow endpoint.
4.  Enter the Security results attributes as the following.

    ```

    {
        "scanner": "Veracode", "applicationName": "", "buildVersion": "", "securityToolId": "" 
    }
    ```

// scanner: Scanning tool and is required e.g. Veracode.

// applicationName: Name of your Veracode application and is required. This attribute is applicable only for Veracode.

// buildVersion: Veracode Scan name / build version and is optional. This attribute is applicable only for Veracode.

// securityToolId: Security tool onboarded in ServiceNow \(sys\_id of the onboarded security tool\) and is optional.

5.  Select **Add** to add the custom action code to your pipeline.


</td></tr><tr><td>

Jenkins

</td><td>

1.  Navigate to the Pipeline Syntax from a configured pipeline.
2.  Select the **snDevOpsSecurityResult** step from the **Sample Step** list, and update the values for the security scan attributes in the step.
3.  Select **Generate Pipeline Script** to create a snippet. You can copy and paste the snippet into the pipeline.

    ```
snDevOpsSecurityResult { 
securityResultAttributes:{"scanner":"Veracode", "applicationName": "", "buildVersion": "", "securityToolId": ""}}
    ```

// scanner: Scanning tool and is required e.g. Veracode.

// applicationName: Name of your Veracode application and is required. This attribute is applicable only for Veracode.

// buildVersion: Veracode Scan name / build version and is optional. This attribute is applicable only for Veracode.

// securityToolId: Security tool onboarded in ServiceNow \(sys\_id of the onboarded security tool\) and is optional.

</td></tr><tr><td>

GitHub Actions

</td><td>

1.  Navigate to your workflow .yml file.
2.  In the **Marketplace** section on the right side, search for the **ServiceNow DevOps Security Results** custom action.
3.  Add the following snippet into your .yml file.

    ```

    SecurityScanResults:
        needs: build
        runs-on: ubuntu-latest
        name: Servicenow Security Scan Results

    steps:
      - name: ServiceNow DevOps Security Results
        uses: ServiceNow/servicenow-devops-security-result@v1.39.0
        with:
            devops-integration-user-name: ${{ secrets.SN_DEVOPS_USER }}
            devops-integration-user-password: ${{ secrets.SN_DEVOPS_PASSWORD }}
            instance-url: ${{ secrets.SN_INSTANCE_URL }}
            tool-id: ${{ secrets.SN_ORCHESTRATION_TOOL_ID }}
            context-github: ${{ toJSON(github) }}
            job-name: 'Servicenow Security Scan Results'
            security-result-attributes: '{ "scanner": "Veracode", "applicationName": "", "buildVersion": "", "securityToolId": ""}
    ```

// scanner: Scanning tool and is required e.g. Veracode.

// applicationName: Name of your Veracode application and is required. This attribute is applicable only for Veracode.

// buildVersion: Veracode Scan name / build version and is optional. This attribute is applicable only for Veracode.

// securityToolId: Security tool onboarded in ServiceNow \(sys\_id of the onboarded security tool\) and is optional.

For more information, see [GitHub marketplace](https://github.com/ServiceNow/servicenow-devops-security-result).

</td></tr><tr><td>

Harness

</td><td>

Run the generic Docker Container Image to use the following script. For more information, see [Implement custom actions for pipelines using a generic Docker container image](../concept/servicenow-custom-actions-for-gitlab.md).```
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

**Parent Topic:**[Veracode integration with DevOps Change Velocity](../concept/veracode-integration-with-devops-change-velocity.md)

