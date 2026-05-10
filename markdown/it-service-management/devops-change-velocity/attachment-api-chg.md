---
title: Add attachments to change requests using attachment API
description: Add test report xmls as attachments to DevOps change requests using the attachment API.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [DevOps test tool integration, User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# Add attachments to change requests using attachment API

Add test report xmls as attachments to DevOps change requests using the attachment API.

For more information about the API, see [Attachment - POST /now/attachment/file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/c_AttachmentAPI.md).

The attachment API URL is:

`https://<your_instance>.service-now.com/api/now/attachment/file?table_name=change_request&table_sys_id=$(getServerChange.sys_id)&file_name=<attached_filename.xml>`, where

-   table\_name = 'change\_request'
-   table\_sys\_id = &lt;chg record sys\_id&gt;
-   file\_name = Any name for the attachment

## Azure DevOps

**Prerequisites**

-   Create an active user with the option **Web service access only** selected. For information on how to create a user, see [Create a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_CreateAUser.md).
-   Assign the role **sn\_change\_write** to the user. For information on how to assign the role, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignARoleToAUser.md).

    ![Create user.](../image/attachment-api-01.png)

-   The system property **sn\_devops.enable\_ado\_generic\_connection** must be enabled.
-   While configuring your Azure DevOps project, to upload to chg. table, the generic connection used should have a user having the role **sn\_change\_write**.

For Azure DevOps pipelines, use the format given here to add attachments to change requests.

Sample pipeline:

```
stage: PostDeploy
    jobs:
      - job: 'pd1'
        pool: server
        steps:
           - task: ServiceNow-DevOps-Server-Get-Change@1
             inputs:
               connectedServiceName: 'v01-Software Quality Scans-ServiceNow DevOps Service Connection'
               projectName: '$(system.teamProject)'
               pipelineName: '$(build.definitionName)'
               stageName: 'Deploy'
               jobName: 'd1'
               buildNumber: '$(build.buildId)'
               branchName: '$(Build.SourceBranchName)'
             name: getServerChange  
           - task: InvokeRESTAPI@1
             inputs:
               connectionType: 'connectedServiceName'
               serviceConnection: 'v01 - new'
               method: 'POST'
               body: '<root><name>john2</name><age>34</age></root>'
               urlSuffix: 'api/now/attachment/file?table_name=change_request&table_sys_id=$(getServerChange.changeSysId)&file_name=test3.xml'
               waitForCompletion: 'false'
```

![Azure DevOps pipeline.](../image/attachment-api-02.png)

## GitHub

For GitHub pipelines, use the format given here to add attachments to change requests.

Sample pipeline:

![GitHub pipeline.](../image/attachment-api-03.png)

**Attachment in the Change Request form in Now instance**:

![Attachments in change record.](../image/attachment-api-04.png)

## Jenkins

For Jenkins pipelines, use the format given here to add attachments to change requests.

Sample pipeline:

```
pipeline {
    agent any
    
    stages {
        stage('POST API Call') {
            steps {
                script {
                    def apiUrl = 'https://<your_instance>.service-now.com/api/sn_devops/v1/devops/tool/test?toolId=<devops_ToolId>&testType=Smoke'
                    def requestBody = [
                        name: "Smoke tests",
                        duration: 0.0,
                        passedTests: 1,
                        failedTests: 1,
                        skippedTests: 1,
                        blockedTests: 1,
                        totalTests: 4,
                        startTime: "2023-12-14T23:31:31z",
	                    finishTime: "2023-12-15T23:31:31z",
                        buildNumber: env.BUILD_NUMBER,
                        stageName: "POST API Call",
                        pipelineName: "TestPipelineKL"
                    ]
                    
                    def auth = "<password>" // devops.integration.user:<password> in base64 encoded.
                    def authHeader = "Basic " + auth
                    
                    def response = httpRequest(
                        contentType: 'APPLICATION_JSON',
                        httpMode: 'POST',
                        requestBody: groovy.json.JsonOutput.toJson(requestBody),
                        url: apiUrl,
                        customHeaders: [[name: 'Authorization', value: authHeader]]
                    )
                    
                    if (response.status == 200 || response.status == 201) {
                        echo "API call successful!"
                        echo "Response: ${response.content}"
                    } else {
                        error "API call failed with status ${response.status}"
                    }
                }
            }
        }
        stage('UAT deploy') {
                    steps {
                        script {
                            def chg_output = snDevOpsChange()
                            def changeRequestNumber = snDevOpsGetChangeNumber(changeDetails: """{"build_number":"${env.BUILD_NUMBER}", "pipeline_name": "TestPipelineKL", "stage_name": "UAT deploy"}""")
                            echo "${changeRequestNumber}"
                            echo "Output of snDevOpsChange(): ${chg_output}"
                    }
                }
        }
        stage('Example') {
            steps {
                script {
                    def API_URL = 'https://<your_instance>.service-now.com/api/sn_devops/devops/orchestration/changeInfo?pipelineName=TestPipelineKL&toolId=<devops_ToolId>&buildNumber=' + env.BUILD_NUMBER + '&stageName=UAT%20deploy'
                    def AUTH = 'Basic <password>'
                    // Call the API
                    def response = sh(script: "curl -X GET -H 'Authorization: ${AUTH}' -H 'Content-Type: application/json' '${API_URL}'", returnStdout: true).trim()
                    echo "Response: ${response}"
                    
                    // Store the JSON response into a variable
                    def slurper = new groovy.json.JsonSlurper()
                    def jsonResponse = slurper.parseText(response)
                    echo "Stored JSON Response: ${jsonResponse}"
                    
                    // Store the specific field value from JSON response into a variable
                    def changeId = jsonResponse.result.sys_id
                    echo "Change ID: ${changeId}"
                    
                    // Call the second API to post attachment
                    def xmlData = '<root><name>john2</name><age>34</age></root>'
                    def AUTH2 = 'Basic <password>='
                    def postResponse = sh(script: "curl -X POST -H 'Authorization: ${AUTH2}' -H 'Content-Type: application/xml' -d '${xmlData}' 'https://<your_instance>.service-now.com/api/now/attachment/file?table_name=change_request&table_sys_id=${changeId}&file_name=test10111.xml'", returnStdout: true).trim()
                }
            }
        }
    }
}

```

![Jenkins pipeline.](../image/attachment-api-05.png)

## Limitations of the attachment API

-   The attachment xml file’s text size should be acceptable to the orchestration tool.
-   For Azure DevOps, **sn\_change\_write** role is needed for authentication of attachment API, to upload the file to the change record.

**Parent Topic:**[DevOps test tool integration](../concept/dev-ops-test-tool-integration.md)

