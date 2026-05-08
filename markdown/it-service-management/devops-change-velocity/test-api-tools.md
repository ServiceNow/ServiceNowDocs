---
title: Add test results to change requests using test API
description: Add test results to DevOps change requests using the test capability of the DevOps - POST /devops/tool/\{capability\} API. The API is available for all test types for various tools connected to DevOps Change Velocity.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [DevOps test tool integration, User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# Add test results to change requests using test API

Add test results to DevOps change requests using the test capability of the DevOps - POST /devops/tool/\{capability\} API. The API is available for all test types for various tools connected to DevOps Change Velocity.

For more information about the API, see DevOps - POST /devops/tool/\{capability\}. To use the API in Azure DevOps, GitHub, and Jenkins, you must use the format mentioned in the respective sections below.

**Prerequisites**

Role required: sn\_devops.admin

You must make sure that the test type you want to use in the API is available as a test type in DevOps Change Velocity and that it is mapped with the respective orchestration tool.

1.  Navigate to **DevOps Change Workspace** &gt; **Administration** &gt; **Integrations** &gt; **Test types**.

    You can also use the classic UI navigation **DevOps** &gt; **Integrations** &gt; **Test Types**.

2.  Verify if the test type is available in the Test types table.

    ![Test types table.](../image/test-api-12.png)

3.  For custom test types, select **New** and add the test type to the list.
    1.  In the **Test type** field, enter a name for your test type.
    2.  From the **Test category** list, select the category of your test type.
    3.  Select **Save**.
4.  Navigate to **DevOps Change Workspace** &gt; **Administration** &gt; **Integrations** &gt; **Test type mappings**.

    You can also use the classic UI navigation **DevOps** &gt; **Integrations** &gt; **Test Type Mappings**.

5.  Verify if the test type is mapped to your orchestration tool.

    ![Test type mappings table.](../image/test-api-13.png)

6.  If the mapping is not available, then select **New** and create the mapping.
    1.  From the **Test type** list, select the test type that you want to map.
    2.  From the **Tool integration** list, select your orchestration tool.
    3.  Select **Save**.

## Azure DevOps

For Azure DevOps pipelines, use the format given here to add test results to change requests for various test types.

Format for URL suffix and parameters:

```
/api/sn_devops/v1/devops/tool/test?toolId=<devops_ToolID>&testType=<test_type>
```

-   The parameter **toolId** must be a valid Tool Id from a connected and configured tool in DevOps Change Velocity.
-   The parameter **testType** should have a test type mapping in DevOps Change Velocity.

Within the **Body**, you must pass the parameters based on the test type.

**Note:** For the generic connection, use the following:

-   username: devops.integration.user
-   password: &lt;devops.integration.user password&gt;

**Pipeline configuration for performance tests**

Sample parameters for the body:

```
{
  "name": "Perf. tests DEMO5",
  "duration": 0,
  "maximumVirtualUsers": 10,
  "throughput": "5/min",
  "maximumTime": 10000,
  "minimumTime": 5000,
  "averageTime": 7000,
  "ninetyPercent": 8000,
  "standardDeviation": 2,
"startTime": "2023-12-14T23:31:31z",
  "finishTime": "2023-12-14T23:40:32z",
  "buildNumber": $(Build.BuildNumber),
  "stageName": "Test API Job",
  "pipelineName": "TEST-CI-PIPELINE"
}
```

![Sample Azure DevOps pipeline configuration for performance tests.](../image/test-api-05.png)

**Performance test summary in your Now instance**:

![Performance test summary.](../image/test-api-06.png)

**Test summary attached to your DevOps change request**:

![Change request test summary.](../image/test-api-07.png)

**Pipeline configuration for other functional and unit tests**

Sample parameters for the body:

```
{
  "name":" Smoke Test summary",
   "duration":0.0,
   "passedTests":1,
   "failedTests":1,
   "skippedTests":1,
   "blockedTests":1,
   "totalTests":4,
  "startTime": "2023-12-14T23:31:31z",
  "finishTime": "2023-12-15T23:31:31z",
  "buildNumber": $(Build. BuildNumber),
 "stageName": "Test API Job",
  "pipelineName": "TEST-CI-PIPELINE"
}
```

![Sample Azure DevOps pipeline configuration for other functional tests.](../image/test-api-03.png)

**Test summary attached to your DevOps change request**:

![Change request test summary.](../image/test-api-04.png)

## Azure DevOps YAML pipeline

Sample pipeline:

```
stages:
  - stage: BashScript
    jobs:
      - job: 'bash'
        steps:
        - script: echo Hello, world!
          displayName: 'BashScript'

        
  - stage: TestAPI
    dependsOn: BashScript
    jobs:
      - job: 'RESTTestAPI'
        # dependsOn: BashScript
        pool: server
        steps:
        - task: InvokeRESTAPI@1
          displayName: 'Invoke REST API: POST'
          inputs:
            connectionType: 'connectedServiceName'
            serviceConnection: 'v01 - generic connection'
            method: 'POST'
            body: |
              {
                            "name": "Performance test summary kl2",
                            "duration": 0,
                            "maximumVirtualUsers": 10,
                            "throughput": "5/min",
                            "maximumTime": 10000,
                            "minimumTime": 5000,
                            "averageTime": 7000,
                            "ninetyPercent": 8000,
                            "standardDeviation": 2,
                            "startTime": "2023-12-14T23:31:31z",
                            "finishTime": "2023-12-14T23:40:32z",
                            "buildNumber": $(Build.BuildId),
                            "stageName": "TestAPI/RestTestAPI",
                            "pipelineName": "TESTYMLPipeline"
                          }
            urlSuffix: '/api/sn_devops/v1/devops/tool/test?toolId=<devops_ToolID>&testType=<test_type>'
            waitForCompletion: 'false'

          
```

![Azure DevOps yml pipeline.](../image/test-api-08.png)

**Release pipeline**

![Azure DevOps release pipeline yml.](../image/test-api-09.png)

## GitHub

For GitHub pipelines, use the format given here to add test results to change requests for various test types.

**Pipeline configuration for performance tests**

Sample pipeline:

```
name: Test API Call Perf

on: 
  workflow_dispatch:

jobs:
  post_api_call_perf:
    runs-on: ubuntu-latest
    
    steps:
    - name: Checkout Repository
      uses: actions/checkout@v2

    - name: post_api_call_perf
      run: |
        apiUrl="https://<your_instance>.service-now.com/api/sn_devops/v1/devops/tool/test?toolId=<devops_ToolId>&testType=<performance_test_type>"
        requestBody='{"toolId": "<devops_ToolId>", "buildNumber": '${{ github.run_number }}' , "workflow": "Test API Call Perf", "repository": "<your_GitHub_repository>", "stageName":"post_api_call_perf","pipelineName":"Test API Call Perf", "testType": "Load", "buildNumber": '${{ github.run_number }}', "buildId": '${{ github.run_id }}' , "attemptNumber" : '${{ github.run_attempt }}', "name": "GitHub Test Summary - Performance 1.0","duration": 0.0,"maximumVirtualUsers": 10,"throughput": "5/min","maximumTime": 1000,"minimumTime": 5000,"averageTime": 7000,"startTime": "2023-12-14T23:31:31z","finishTime": "2023-12-14T23:31:31z","ninetyPercent": 8000, "standardDeviation": 2.0 }'
        auth="devops.integration.user:<password> in base64 encoded"
        authHeader="Basic $auth"
        response=$(curl -X POST -H "Content-Type: application/json" -H "Authorization: $authHeader" -d "$requestBody" $apiUrl)
        exitCode=$?
        
        if [ $exitCode -eq 0 ]; then
          echo "API call successful!"
          echo "Response: $response"
        else
          echo "API call failed!"
          echo "Response: $response"
          exit 1
        fi

```

![Sample GitHub pipeline configuration for performance tests.](../image/test-api-11.png)

**Pipeline configuration for other functional and unit tests**

Sample pipeline:

```
name: Test API Call

on: 
  workflow_dispatch:

jobs:
  post_api_call:
    runs-on: ubuntu-latest
    
    steps:
    - name: Checkout Repository
      uses: actions/checkout@v2

    - name: post_api_call
      run: |
        apiUrl="https://<your_instance>.service-now.com/api/sn_devops/v1/devops/tool/test?toolId=<devops_ToolID>&testType=<test_type>"
        requestBody='{"toolId": "<devops_ToolID>", "buildNumber": '${{ github.run_number }}' , "workflow": "Test API Call", "repository": "<your_GitHub_repository>", "stageName":"post_api_call","pipelineName":"TestAPICall", "testType": "Smoke", "buildNumber": '${{ github.run_number }}', "buildId": '${{ github.run_id }}' , "attemptNumber" : '${{ github.run_attempt }}', "testSummaries": [{"name": "GitHub Test Summary - smoke","passedTests": 1,"failedTests": 1,"skippedTests": 1,"ignoredTests": 0,"blockedTests": 1,"totalTests": 4,"startTime": "2023-12-14T23:31:31z","endTime": "2023-12-14T23:31:31z","duration": 0.0,"testType": "Smoke", "suites": []}] }'
        auth="devops.integration.user:<password> in base64 encoded"
        
        authHeader="Basic $auth"
        response=$(curl -X POST -H "Content-Type: application/json" -H "Authorization: $authHeader" -d "$requestBody" $apiUrl)
        exitCode=$?
        
        if [ $exitCode -eq 0 ]; then
          echo "API call successful!"
          echo "Response: $response"
        else
          echo "API call failed!"
          echo "Response: $response"
          exit 1
        fi

```

![Sample GitHub pipeline configuration for other functional tests.](../image/test-api-10.png)

## Jenkins

For Jenkins pipelines, use the format given here to add test results to change requests for various test types.

**Pipeline configuration for performance tests**

Sample pipeline:

```
pipeline {
    agent any
    stages {
        stage('POST API Call') {
            steps {
                script {
                    def apiUrl = 'https://<your_instance>.service-now.com/api/sn_devops/v1/devops/tool/test?toolId=<devops_ToolID>&testType=<performance_test_type>'
                    def requestBody = [
                        name: "Performance Load tests jenkins",
                        duration: 0.0,
                        maximumVirtualUsers: 10,
                        throughput: "6/min",
                        maximumTime: 1000,
                        minimumTime: 300,
                        averageTime: 700,
                        ninetyPercent: 600,
                        standardDeviation: 2.0,
                        startTime: "2023-12-14T23:31:31z",
                        finishTime: "2023-12-14T23:40:32z",
                        buildNumber: env.BUILD_NUMBER,
                        stageName: "POST API Call",
                        pipelineName: "KLPerformanceTestPipeline"
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
    }
}
```

![Sample Jenkins pipeline configuration for performance tests.](../image/test-api-01.png)

**Pipeline configuration for other functional and unit tests**

Sample pipeline:

```
pipeline {
    agent any
    
    stages {
        stage('POST API Call') {
            steps {
                script {
                    def apiUrl = 'https://<your_instance>.service-now.com/api/sn_devops/v1/devops/tool/test?toolId=<devops_ToolID>&testType=<test_type>'
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
    }
}
```

![Sample Jenkins pipeline configuration for other functional tests.](../image/test-api-02.png)

## Limitations of the test API

-   Waiting logic will not be taken care of.
-   Re-run scenarios cannot be handled.

**Parent Topic:**[DevOps test tool integration](../concept/dev-ops-test-tool-integration.md)

