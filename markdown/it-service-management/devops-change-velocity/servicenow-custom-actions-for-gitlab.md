---
title: Implement custom actions for pipelines using a generic Docker container image
description: Use the ServiceNow custom actions to collect data related to change request creation, Sonar scan, artifact registration, and package registration in your pipeline with the help of the generic Docker Container Image.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 18
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Implement custom actions for pipelines using a generic Docker container image

Use the ServiceNow custom actions to collect data related to change request creation, Sonar scan, artifact registration, and package registration in your pipeline with the help of the generic Docker Container Image.

Docker Image is a software package that can be used to run an application. This image informs how a container should instantiate, and which software components must be run. Docker Container is a virtual environment that combines application code and all the dependencies required to run the application. For more information on Docker, see [Docker documentation](https://docs.docker.com/get-started/overview/).

## Environmental variables for GitLab

To configure Docker Images, the following environmental variables must be available in your GitLab instance for your project.

-   SNOW\_TOKEN: ServiceNow token number. It’s a masked variable and wont be displayed in the jobs.
-   SNOW\_TOOLID: ServiceNow tool ID.
-   SNOW\_URL: ServiceNow instance URL.

When you configure a GitLab project, the environmental variables are created for the project and the latest configured variable values are considered. If you’re an upgrading customer, you must reconfigure your existing GitLab projects or manually add the environmental variables in your GitLab instance. For information on adding variables, see [GitLab documentation](https://docs.gitlab.com/ee/ci/variables/).

When adding the SNOW\_TOKEN variable, you can acquire the token by selecting the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table.

The environmental variables must be updated with the values available in the Configure webhooks manually pop-up in the tool record page. For details on how to view the connection details, see [Configure webhooks from the tool record](../task/configure-webhooks-from-the-tool-record.md) and [Configure webhooks in GitLab manually](../task/configure-webhooks-in-gitlab.md).

![Connection details for GitLab](../image/gitlab-custom-actions-01.png)

## Environmental variables for GitHub Actions

To configure Docker Images, certain environmental variables must be available in your GitHub Actions instance.

The following environmental variables must be configured in your GitHub Actions instance.

**Note:** The variables must be updated with the values available in the Configure webhooks manually pop-up in the tool record page.

-   SNOW\_TOKEN: ServiceNow token number. It’s a masked variable and wont be displayed in the jobs.
-   SNOW\_TOOLID: ServiceNow tool ID.
-   SNOW\_URL: ServiceNow instance URL.

**Note:** For information on adding variables in GitHub Actions, see [GitHub documentation](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/store-information-in-variables).

The following environment variables must be passed in your GitHub Actions pipeline:

**Note:** The values for these variables are dynamically retrieved from GitHub, and you don’t have to configure them separately.

-   PIPELINE\_ID: Workflow run ID of a repository. Usage - PIPELINE\_ID: $\{\{github.run\_id \}\}
-   API\_V4\_URL: URL of the GitHub server. Usage - API\_V4\_URL: $\{\{ github.server\_url \}\}
-   JOB\_ID: Workflow run ID of a repository. Usage - PIPELINE\_ID: $\{\{ github.run\_id \}\}
-   PROJECT\_PATH: Name of the workflow. Usage - PROJECT\_PATH: $\{\{ github.repository \}\}/$\{\{github.workflow\}\}
-   REPOSITORY\_NAME: Name of the repository. Usage - REPOSITORY\_NAME: $\{\{ github.repository \}\}
-   RUN\_ATTEMPT: Number of workflow attempts. Usage - RUN\_ATTEMPT: $\{\{ github.run\_attempt \}\}
-   PROJECT\_TITLE: Name of the workflow. Usage - PROJECT\_TITLE: $\{\{ github.repository \}\}/$\{\{github.workflow\}\}
-   COMMIT\_BRANCH: Name of the branch on which the workflow is running. Usage - COMMIT\_BRANCH: $\{\{ github.ref\_name \}\}
-   WORKFLOW\_NAME: Name of the workflow. Usage - WORKFLOW\_NAME: $\{\{ github.workflow \}\}

When you configure a repository, the environmental variables are created for the repository and the latest configured variable values are considered. If you’re an upgrading customer, you must reconfigure your existing repositories or manually add the environmental variables in your instance.

![Connection details for GitHub Actions](../image/github-actions-connection-details.png)

## Environmental variables for Harness

To configure Docker Images, certain environmental variables must be available in your Harness instance.

The following environmental variables must be configured in your Harness instance.

**Note:** The variables must be updated with the values available in the Configure webhooks manually pop-up in the tool record page.

-   SNOW\_TOKEN: ServiceNow token number. It’s a masked variable and wont be displayed in the jobs.
-   SNOW\_TOOLID: ServiceNow tool ID.
-   SNOW\_URL: ServiceNow instance URL.

The following environment variables must be passed in your Harness pipeline:

-   HARNESS\_STAGE\_NAME: "&lt;+stage.identifier&gt;"

-   HARNESS\_PIPELINE\_NAME: "&lt;+org.identifier&gt;/&lt;+project.identifier&gt;/&lt;+pipeline.name&gt;"


When you configure a repository, the environmental variables are created for the repository and the latest configured variable values are considered. If you’re an upgrading customer, you must reconfigure your existing repositories or manually add the environmental variables in your instance.

![Configure webhooks manually screen](../image/harness-workspace-3.png)

## ServiceNow Docker Image

You must pass the ServiceNow Docker Image \(servicenowdocker/sndevops:6.2.0\) in your pipeline before adding custom actions in your pipeline. You can clone the app-devops-gitlab public repository located at [https://github.com/ServiceNow/app-devops-gitlab](https://github.com/ServiceNow/app-devops-gitlab), and create the Docker Image by running the following commands:

```
docker build -t servicenowdocker/sndevops:6.2.0
```

```
docker push servicenowdocker/sndevops:6.2.0
```

You can add the Docker Image at the starting of the .yml file. You don’t have to add it for each job separately.

**Note:** If you want to use multiple images, then add them at the job levels.

You can also customize the **app-devops-gitlab** public repository and create your own Docker Image to pass in the pipeline.

## Proxy configuration

If your GitLab instance runs behind a proxy server or you want to route requests through a proxy, you must configure proxy settings using environment variables in your Docker deployment.

Configure the following environment variables for proxy support:

-   PROXY\_ENDPOINT: \# for example, http://localhost:7080 or https://proxy.example.com:8080
-   PROXY\_USERNAME: \# Optional: for proxy authentication
-   PROXY\_PASSWORD: \# Optional: for proxy authentication
-   PROXY\_AUTH: \# Optional: alternative authentication using API key

PROXY\_ENDPOINT can be either HTTP or HTTPS. For backward compatibility, HTTP\_PROXY and HTTPS\_PROXY are also supported. If you’re using self-signed certificates with HTTPS proxy, set NODE\_TLS\_REJECT\_UNAUTHORIZED=0 \(for testing only\). Authentication can be provided through the following ways:

-   Username/Password: Use PROXY\_USERNAME and PROXY\_PASSWORD
-   API Key: Use PROXY\_AUTH
-   No authentication: Leave authentication variables unset

For example:

```
stages:
  - package

package:
  stage: package
  image: servicenowdocker/sndevops:6.2.0
  variables:
    PROXY_ENDPOINT: "https://proxy.example.com:8080"
    PROXY_USERNAME: "proxy_user"
    PROXY_PASSWORD: "proxy_pass"
  script: 
    - sndevopscli create package -n "package-name" -a '[{"name":"artifact-name","repositoryName":"artifact-repo-name","version":"1.3.0"}]'
```

## ServiceNow DevOps Change Step

Add the ServiceNow DevOps Change custom step at the job level to create a change in your ServiceNow instance. For example:

```

stages:
  - DevOpsChangeApproval

ServiceNow DevOps Change:
  stage: DevOpsChangeApproval
  image: servicenowdocker/sndevops:6.2.0
  script: 
    - sndevopscli create change -p "{\"changeStepDetails\":{\"timeout\":3600,\"interval\":100},\"attributes\":{\"short_description\":\"Software Deployment\",\"description\":\"Software Deployment.\",\"assignment_group\":\"xxxxxxxxx\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\"}}"


```

**Note:** If you’re using both the Docker change step and the when: manual instruction change step, confirm that you add them at different job levels.

You must enter the input values for this custom action as a JSON-formatted string.

-   **changeStepDetails**: \[optional\] It holds the timeout and interval details.
-   **interval**: \[optional\] The time in seconds to wait between trying the API. The default value is 100 seconds.
-   **timeout**: \[optional\] The maximum time in seconds to wait until the action should fails. The default value is 3600 seconds.

    **Note:** When the timeout value is available here as well in your tool, the timeout value that is earlier is considered.

-   **attributes**: \[optional\] The change request attribute details are to be used while creating a change in a ServiceNow instance. The change request is a JSON object surrounded by curly braces \{\} containing key-value pairs separated by a comma\(,\). A key-value pair consists of a key and a value separated by a colon\(:\). The keys supported in key-value pair are short\_description, description, assignment\_group, implementation\_plan, backout\_plan, test\_plan, and so on.
-   **-ctx**: \[optional\] Additional context parameters in JSON format. Environmental variable details from GitHub that will be used to build the request for the DevOps Change API. For example,

    ```
    sndevopscli create change -ctx "{\"projectId\": \"123456\", \"attemptNumber\": \"${{ github.run_attempt }}\"}" -p "{\"changeStepDetails\": {\"timeout\":3600,\"interval\":100},\"autoCloseChange\":true,\"attributes\":{\"short_description\":\"G Venkata Automated Software Deployment\",\"description\":\"Automated Software Deployment.\",\"assignment_group\":\"a715cd759f2002002920bde8132e7018\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\"}}"
    ```

-   **-w**: \[optional\] Specify whether the pipeline should wait for change creation and approval. By default, the pipeline will be waiting until the change creation and it's approval.

**Note:** The name of the change step must contain the **ServiceNow DevOps Change** keyword, which is the job name.

-   **Deployment gate**

    This attribute enables the passing of data during change request creation using the `sndevopscli`, and at the same time uses the manual job functionality provided by tools like GitLab. For example:

    ```
    stages:
      - DevOpsChangeApproval
      - deploy
    
    ServiceNow DevOps Change:
      stage: DevOpsChangeApproval
      image: servicenowdocker/sndevops:6.2.0
      script: 
        - sndevopscli create change -p '{"changeStepDetails":{"timeout":3600,"interval":100},"deploymentGateDetails":{"jobName":"sn-change-job"},"attributes":{"short_description":"Automated Software Deployment","description":"Automated Software Deployment.","implementation_plan":"Software update is tested and results can be found in Test Summaries Tab.","backout_plan":"When software fails in production, the previous software release will be re-deployed.","test_plan":"Testing if the software was successfully deployed or not"}}'
    
    sn-change-job:
      stage: deploy
      needs:
        job: ServiceNow DevOps Change
      when: manual
      allow_failure: false
      script: |
        echo sn-change-job
    ```

    The optional deploymentGateDetails attribute must contain a jobName attribute, which holds the name of the downstream manual job in the pipeline.


## ServiceNow DevOps SonarScan Results

Add the ServiceNow DevOps SonarScan Results custom step at the job level to create a Sonar summary in your ServiceNow instance. For example:

```

stages:
  - DevOpsSonarStage

ServiceNow DevOps SonarScan Results:
  stage: DevOpsSonarStage
  image: servicenowdocker/sndevops:6.2.0
  script: 
    - sndevopscli create sonar -url 'https://sonarcloud.io' -projectKey 'devsystem2019_TestImportTest'


```

-   **url**: \[Required\] This specifies the Sonar URL.
-   **projectKey**: \[Required\] This specifies the Sonar project key.

**Note:** The name of the Sonar step must be same as the job name, which is **ServiceNow DevOps SonarScan Results**.

-   **Limitation**

    While creating software quality summary results, the MERGE\_REQUEST\_SOURCE\_BRANCH\_NAME environment variable will be used for merge pipelines, and DEFAULT\_BRANCH will be used for tag pipelines because the COMMIT\_BRANCH variable isn’t available for merge or tag pipelines. For more information, see [GitLab documentation](https://docs.gitlab.com/ee/ci/variables/predefined_variables.html).


## Register Artifact

Add the artifact custom step at the job level to register an artifact in your ServiceNow instance. For example:

```

stages:
  - artifact

artifact:
  stage: artifact
  image: servicenowdocker/sndevops:6.2.0
  script: 
    - sndevopscli create artifact -a "[{\"name\":\"Artifact-${JOB_NAME}\",\"repositoryName\":\"Repo\",\"version\":\"1.${JOB_ID}.0\"}]"
 
```

You must enter the input values for this custom action as a JSON-formatted string.

**-a**: \[Required\] This value specifies the artifact details.

## Register Package

Add the package custom step at the job level to register a package in your ServiceNow instance. For example:

```

stages:
  - package

package:
  stage: package
  image: servicenowdocker/sndevops:6.2.0
  script: 
    - sndevopscli create package -n "Package2" -a "[{\"name\":\"Artifact-${JOB_NAME}\",\"repositoryName\":\"Repo\" ,\"version\":\"1.${JOB_ID}.0\"}]"
```

You must enter the input values for this custom action as a JSON-formatted string.

**-n**: \[Required\] This specifies the package name.

## Get change

Add at job level to get changeRequestNumber from ServiceNow instance with the given changeDetails to identify the change request.

For example:

```


stages:
  - DevOpsGetChange

ServiceNow DevOps Get Change:
  stage: DevOpsGetChange
  image: servicenowdocker/sndevops:6.2.0
  script: 
    - sndevopscli get change -p "{\"buildNumber\":${CHG_JOB_ID},\"stageName\":\"ServiceNow DevOps Change Step\",\"pipelineName\":\"GitlabDockerGetAndUpdateChange\"}"

-p: It stands for changeDetails. The change details to be used for identifying change request in ServiceNow instance. The change details is a JSON object surrounded by curly braces {} containing key-value pair separated by a comma ,. A key-value pair consists of a key and a value separated by a colon :. The keys supported in key-value pair are buildNumber, pipelineName, stageName

buildNumber: [mandatory]
This specifies ID of the Job where we have created change request.

stageName: [mandatory]
This specifies the Job name where we have created change request..

pipelineName: [mandatory]
This specifies the pipeline name.

Outputs:
  sndevopschg.json file created with content: {
    "status": "SUCCESS",
    "changeRequestNumber": "CHGXXXXX"
  }
  
  changeRequestNumber: Change Request Number found for the given change details
  status: To know the status of the Change Request GET.

```

## Update change

Add at job level to update change in ServiceNow instance for the changeRequestNumber provided as input along with changeRequestDetails.

For example:

```

stages:
  - DevOpsUpdateChangeStage

ServiceNow DevOps Update Change:
  stage: DevOpsUpdateChangeStage
  image: servicenowdocker/sndevops:6.2.0
  script: 
    - sndevopscli update change -n 'CHGXXXXXX' -p "{\"short_description\":\"G Venkata12345 Automated Software Deployment\",\"description\":\"Automated Software Deployment.\",\"assignment_group\":\"XXXXX\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\"}"

-n [Not mandatory if we have sndevopschg.json in our pipeline yml]: It stands for changeRequestNumber. The change request number to identify a unique change request. 
   Precedence of choosing changeRequestNumber: 
     - changeRequestNumber mentioned in the pipeline yml
     - changeRequestNumber stored in sndevopschg.json.

-p : It stands for changeDetails. The change details to be used for Updating the change request information identified by the specified change request number with the key-value pairs. The change details is a JSON object surrounded by curly braces {} containing key-value pair separated by a comma ,. A key-value pair consists of a key and a value separated by a colon :. The keys supported in key-value pair are short_description, state, description, work_notes ..so on

OR
  - sndevopscli update change -p "{\"short_description\":\"Updated Automated Software Deployment\",\"description\":\"Automated Software Deployment.\",\"assignment_group\":\"XXXXXXXXXX\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\"}"

NOTE: State should be specified at last in case if you are update the state of change request.
- sndevopscli update change -p "{\"short_description\":\"Updated Automated Software Deployment\",\"description\":\"Automated Software Deployment.\",\"assignment_group\":\"XXXXXXXXXX\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\","state":"3"}'

```

## Auto close change

Incorporate auto close change in ServiceNow instance. For detailed information about auto close, see [Configuring DevOps change request details within the pipeline](dev-ops-config-change-details.md).

For example:

```

stages:
  - changeapproval

ServiceNow DevOps Change Step:
  stage: changeapproval
  image: servicenowdocker/sndevops:6.2.0
  script: 
     - sndevopscli create change -p "{\"changeStepDetails\":{\"timeout\":3600,\"interval\":100},\"autoCloseChange\":true,\"attributes\":{\"short_description\":\"G Venkata Automated Software Deployment\",\"description\":\"Automated Software Deployment.\",\"assignment_group\":\"xxxxxxxx\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\"}}"
  
autoCloseChange: [optional] : Boolean value

```

## Security scan results

Add the ServiceNow DevOps Security Scan Results custom step at the job level to retrieve security scan results. For example:

```
stages:
  - DevOpsSecurityScanStageServiceNow 

ServiceNow DevOps Security Scan Results:
  stage: DevOpsSecurityScanStageimage 
  image: servicenowdocker/sndevops:6.2.0
  script: 
      - sndevopscli create securityScan -p "{\"pipelineInfo\":{\"buildNumber\":\"${PIPELINE_ID}\",\"pipelineExecutionUrl\":\"${PIPELINE_URL}\" },\"securityResultAttributes\":{ \"scanner\":\"Veracode\",\"applicationName\":\"PetStoreAPI-Github\",\"buildVersion\":\"\",\"securityToolId\":\"\"}}"
  -p: [mandatory]It the payload of security result attributes. The payload will have attributes as follows:
    buildNumber: PIPELINE_ID (mandatory)pipelineExecutionUrl: PIPELINE_URL (mandatory)scanner: Scanning tool and is required e.g. Checkmarx One.projectName/projectId: Name/Id of your Checkmarx One project and is required. This attribute is applicable only for Checkmarx One.applicationName: Name of your Veracode application and is required. This attribute is applicable only for Veracode.buildVersion": Veracode Scan name / build version and is optional. This attribute is applicable only for Veracode.scanId: Checkmarx One scan id and is optional. This attribute is applicable only for Checkmarx One.securityToolId: Security tool onboarded in ServiceNow (sys_id of the onboarded security tool) and is optional.
 
```

## Sample pipelines

## Sample GitLab pipeline

```

image: servicenowdocker/sndevops:6.2.0
stages:
  - pre-build
  - build
  - sonar
  - securityscan
  - changeapproval
  - getchange
  - updatechange
  - deploy


Pre-Build:
  stage: pre-build
  script:
    - echo $JOB_NAME
    
Artifact and Package:
  stage: build
  script:
    - sndevopscli create artifact -a "[{\"name\":\"Artifact-${JOB_NAME}\",\"repositoryName\":\"TestRepo\",\"version\":\"1.${RUNNER_ID}.0\"}]"
    - sndevopscli create package -n "Test_Package" -a "[{\"name\":\"Artifact-${JOB_NAME}\",\"repositoryName\":\"TestRepo\",\"version\":\"1.${RUNNER_ID}.0\"}]"


ServiceNow DevOps SonarScan Results:
  stage: sonar
  script:
    - sndevopscli create sonar -url 'https://sonarcloud.io' -projectKey 'xxxxxxx'


ServiceNow DevOps Security Scan Results:
  stage: securityscan
  script:
    - sndevopscli create securityScan -p "{\"pipelineInfo\":{\"buildNumber\":\"${JOB_ID}\", \"stageName\":\"ServiceNow DevOps Security Scan Results\",\"taskExecutionUrl\":\"${JOB_URL}\" },\"securityResultAttributes\":{ \"scanner\":\"Veracode\",\"applicationName\":\"PetStoreAPI-Github\",\"buildVersion\":\"\",\"securityToolId\":\"\"}}"

ServiceNow DevOps Change Step:
  stage: changeapproval
  variables:
    CHG_JOB_ID: $JOB_ID
  script: 
     - echo "CHG_JOB_ID=$CHG_JOB_ID" >> generated_job_id.env
     - sndevopscli create change -p "{\"changeStepDetails\":{\"timeout\":3600,\"interval\":100},\"autoCloseChange\":true,\"attributes\":{\"short_description\":\"G Venkata Automated Software Deployment\",\"description\":\"Automated Software Deployment.\",\"assignment_group\":\"a715cd759f2002002920bde8132e7018\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\"}}"
     - sndevopscli get change #If we are placing get change cli command in the same job where we are creating change then no need to mention the changeDetails.
  artifacts:
    paths:
      - generated_job_id.env

DevOps Get Change:
  stage: getchange
  script:
    - source generated_job_id.env
    - sndevopscli get change -p "{\"buildNumber\":${CHG_JOB_ID},\"stageName\":\"ServiceNow DevOps Change Step\",\"pipelineName\":\"SmrutiTestDemoProject\"}"
  artifacts:
    paths:
      - sndevopschg.json  
  dependencies:
    - ServiceNow DevOps Change Step

DevOps Update Change:
  stage: updatechange
  script:
    #- sndevopscli update change -n 'CHGXXXX' -p "{\"short_description\":\"Automated Software Deployment\",\"description\":\"Automated Software Deployment.\",\"assignment_group\":\"xxxxxxx\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\"}"
    - sndevopscli update change -p "{\"short_description\":\"Updated Automated Software Deployment\",\"description\":\"Automated Software Deployment.\",\"assignment_group\":\"xxxxxxx\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\"}"
  dependencies:
    - DevOps Get Change

Deploy Job:
  stage: deploy
  script:
    - echo $JOB_NAME
```

## Sample GitHub Actions pipeline

```
name: GithubAction

on:
  push:
    branches: ["main"]
  pull_request:
    branches: ["main"]

permissions:
  contents: read
env:
  SNOW_URL: ${{ secrets.SNOW_URL }}
  SNOW_TOKEN: ${{ secrets.SNOW_TOKEN }}
  SNOW_TOOLID: ${{ secrets.SNOW_TOOLID }}
  # These are the optional env variables
  #PIPELINE_ID: ${{ github.run_id }}
  #API_V4_URL: ${{ github.server_url }}
  #JOB_ID: ${{ github.run_id }}
  #PROJECT_PATH: ${{ github.job }}
  #REPOSITORY_NAME: ${{ github.repository }}
  #RUN_ATTEMPT: ${{ github.run_attempt }}
  #PROJECT_TITLE: ${{ github.repository }}/${{github.workflow}}
  #COMMIT_BRANCH: ${{ github.ref_name }}
  #WORKFLOW_NAME: ${{ github.workflow }}

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Set up JDK 17
        run: |
          echo 'hello'

  ServiceNowDevOpsChange:
     runs-on: ubuntu-latest
     needs: build
     container:
       image: servicenowdocker/sndevops:6.2.0
     env:
       JOB_NAME: "ServiceNowDevOpsChange"

     steps:
       - name: create change
         run: |
           sndevopscli create change -p "{\"changeStepDetails\":{\"timeout\":3600,\"interval\":10},\"autoCloseChange\":true,\"attributes\":{\"short_description\":\"G Venkata Automated Software Deployment\",\"description\":\"Automated Software Deployment.\",\"assignment_group\":\"a715cd759f2002002920bde8132e7018\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\"}}"

  ServiceNowUpdateDevOpsChange:
       runs-on: ubuntu-latest
       needs: ServiceNowDevOpsChange
       container:
         image: servicenowdocker/sndevops:6.2.0
       env:
         JOB_NAME: "ServiceNowDevOpsChange"
  
       steps:
         - name: update change
           run: |
             sndevopscli update change -p "{\"short_description\":\"Updated Automated Software Deployment\",\"description\":\"Automated Software Deployment.\",\"assignment_group\":\"a715cd759f2002002920bde8132e7018\",\"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",\"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",\"test_plan\":\"Testing if the software was successfully deployed or not\"}"

  ArtifactAndPackage:
      runs-on: ubuntu-latest
      needs: build
      container:
        image: servicenowdocker/sndevops:6.2.0
      env:
        JOB_NAME: "ArtifactAndPackage"
      steps:
        - name: create artifact
          run: |
             sndevopscli create artifact -a "[{\"name\": \"com:customactiondemo\",\"version\": \"1.${{ github.run_number }}\",\"semanticVersion\": \"1.${{ github.run_number }}.0\",\"repositoryName\": \"${{ github.repository }}\"}]"
             sndevopscli create package -n "Test_Package" -a "[{\"name\": \"com:customactiondemo\",\"version\": \"1.${{ github.run_number }}\",\"semanticVersion\": \"1.${{ github.run_number }}.0\",\"repositoryName\": \"${{ github.repository }}\"}]"

  ServiceNowDevOpsSonarScanResults:
      name: ServiceNowDevOpsSonarScanResults
      needs: ArtifactAndPackage
      runs-on: ubuntu-latest
      container:
        image: servicenowdocker/sndevops:6.2.0
      env:
        JOB_NAME: "ServiceNowDevOpsSonarScanResults"
      steps:
        - name: devops soanr results
          run: |
            sndevopscli create sonar -url 'https://sonarcloud.io' -projectKey 'xxxxxxx'

  ServiceNowDevOpsSecurityScan:
      name: ServiceNowDevOpsSecurityScan
      runs-on: ubuntu-latest
      needs: build
      container:
        image: servicenowdocker/sndevops:6.2.0
      steps:
        - name: security scan
          run: |
           sndevopscli create securityScan -p "{ \"pipelineInfo\": {  \"runId\": \"${{ github.run_id }}\",   \"runNumber\": \"${{ github.run_number }}\", \"runAttempt\": \"${{ github.run_attempt }}\",   \"job\": \"ServiceNowDevOpsSecurityScan\",  \"workflow\": \"${{ github.workflow }}\",  \"repository\": \"${{github.repository}}\" }, \"securityResultAttributes\": { \"scanner\": \"Veracode\",    \"applicationName\": \"PetStoreAPI-Github\",\"buildVersion\": \"\",   \"securityToolId\": \"\"}}"

```

## Sample Harness pipeline

```
# This is an example pipeline, and your pipeline and container configurations may vary from the setup shown here.
# Refer to the pipeline stages for Security, Software, and Change configurations. 
# Using this YAML file directly will not work as it contains several Harness-specific configurations; check the Command section present for container steps.
pipeline:
  name: Example pipeline
  identifier: Example_pipeline 
  projectIdentifier: Example_project
  orgIdentifier: ExampleOrg
  tags: {}
  stages:
    - stage:
        name: Build
        identifier: Build
        description: ""
        type: Custom
        spec:
          execution:
            steps:
              - step:
                  type: ShellScript
                  name: ShellScript_1
                  identifier: ShellScript_1
                  spec:
                    shell: Bash
                    executionTarget: {}
                    source:
                      type: Inline
                      spec:
                        script: echo "Building.."
                    environmentVariables: []
                    outputVariables: []
                  timeout: 10m
        tags: {}
    - stage:
        name: ServiceNow DevOps Sonar Scan Results
        identifier: ServiceNow_DevOps_Sonar_Scan_Results
        description: ""
        type: Custom
        spec:
          execution:
            steps:
              - step:
                  type: Container
                  name: Sonar container
                  identifier: Sonar_container
                  spec:
                    connectorRef: docker_connector # harness docker connector
                    image: servicenowdocker/sndevops:6.2.0
                    command: |-
                      export SNOW_URL="<+variable.SNOW_URL>"
                      export SNOW_TOOLID="<+variable.SNOW_TOOLID>"
                      export SNOW_TOKEN="<+variable.SNOW_TOKEN>"
                      export HARNESS_STAGE_NAME="<+stage.identifier>"
                      export HARNESS_PIPELINE_NAME="<+org.identifier>/<+project.identifier>/<+pipeline.name>"
                      export COMMIT_BRANCH="main"
                      sndevopscli create sonar -url 'https://sonarcloud.io' -projectKey 'SONAR_PROJECT_KEY' -branch "main"
                    shell: Sh
                    infrastructure:
                      type: KubernetesDirect
                      spec:
                        connectorRef: KUBE_CONNECTOR # harness kubernates connector
                        namespace: harness-delegate-ng
                        resources:
                          limits:
                            cpu: "0.5"
                            memory: 500Mi
                        annotations: {}
                        labels: {}
                        containerSecurityContext:
                          capabilities:
                            drop: []
                            add: []
                        nodeSelector: {}
                    reports:
                      type: JUnit
                      spec:
                        paths: []
                    outputVariables: []
                    envVariables: {}
                  timeout: 1h
        tags: {}
    - stage:
        name: ServiceNow DevOps Security Scan Results
        identifier: ServiceNow_DevOps_Security_Scan_Results
        description: ""
        type: Custom
        spec:
          execution:
            steps:
              - step:
                  type: Container
                  name: security
                  identifier: security
                  spec:
                    connectorRef: docker_connector # harness docker connector
                    image: servicenowdocker/sndevops:6.2.0
                    command: |-
                      export SNOW_URL="<+variable.SNOW_URL>"
                      export SNOW_TOOLID="<+variable.SNOW_TOOLID>"
                      export SNOW_TOKEN="<+variable.SNOW_TOKEN>"
                      sndevopscli create securityScan -p \
                      "{\"pipelineInfo\":{
                          \"buildNumber\":\"<+stage.nodeExecutionId>\",
                          \"taskExecutionUrl\":\"<+pipeline.executionUrl>?stage=<+stage.nodeExecutionId>\", 
                          \"orchestrationPipeline\":\"<+org.identifier>/<+project.identifier>/<+pipeline.name>\" 
                        },
                        \"securityResultAttributes\":{
                           \"scanner\":\"Veracode\",
                           \"applicationName\":\"VeraDemo-10\"
                        }
                      }"
                    shell: Sh
                    infrastructure:
                      type: KubernetesDirect
                      spec:
                        connectorRef: KUBE_CONNECTOR # harness kubernates connector
                        namespace: harness-delegate-ng
                        resources:
                          limits:
                            cpu: "0.5"
                            memory: 500Mi
                        annotations: {}
                        labels: {}
                        containerSecurityContext:
                          capabilities:
                            drop: []
                            add: []
                        nodeSelector: {}
                    reports:
                      type: JUnit
                      spec:
                        paths: []
                    outputVariables: []
                    envVariables: {}
                  timeout: 1h
        tags: {}
    - stage:
        name: Deploy
        identifier: Deploy
        description: ""
        type: Deployment
        spec:
          deploymentType: Kubernetes
          service:
            serviceRef: service
          environment:
            environmentRef: Dev
            deployToAll: false
            infrastructureDefinitions:
              - identifier: Infra
          execution:
            steps:
              - step:
                  type: Container
                  name: ServiceNow change
                  identifier: ServiceNow_change
                  spec:
                    connectorRef: docker_connector # harness docker connector
                    image: servicenowdocker/sndevops:6.2.0
                    command: |-
                      # set mandetory variables. These can be set from Environment variable section of Optional configuration as well.
                      export HARNESS_STAGE_NAME="<+stage.identifier>"
                      export SNOW_URL="<+variable.SNOW_URL>"
                      export SNOW_TOOLID="<+variable.SNOW_TOOLID>"
                      export SNOW_TOKEN="<+variable.SNOW_TOKEN>"
                      # "sndevopscli create change" command notifies ServiceNow DevOps to create a change. 
                      # Ensure to update "upstreamStage" accordingly. Example, if you have 3 stages Test, Change and Deploy in your pipeline, then you must update as "upstreamStage": "<+pipeline.stages.Test.nodeExecutionId>". Note that if your change stage is the first stage, you can remove this line.
                      sndevopscli create change -ctx \
                      "{
                          \"pipelineExecutionUrl\":\"<+pipeline.executionUrl>\",
                          \"stageIdentifier\": \"<+stage.identifier>\",
                          \"stageNodeExecutionId\": \"<+stage.nodeExecutionId>\",
                          \"pipelineName\": \"<+pipeline.name>\",
                          \"upstreamStage\": \"<+pipeline.stages.ServiceNow_DevOps_Security_Scan_Results.nodeExecutionId>\"
                      }" -p \
                      "{
                          \"changeStepDetails\":
                          {
                                  \"timeout\":3600,
                                  \"interval\":100
                          },
                          \"autoCloseChange\":true,
                          \"attributes\":{
                              \"chg_model\":\"adffaa9e4370211072b7f6be5bb8f2ed\",
                              \"short_description\":\"Software Deployment\",
                              \"description\":\"Automated Software Deployment.\",
                              \"implementation_plan\":\"Software update is tested and results can be found in Test Summaries Tab.\",
                              \"backout_plan\":\"When software fails in production, the previous software release will be re-deployed.\",
                              \"test_plan\":\"Testing if the software was successfully deployed or not\"
                          }
                      }"
                    shell: Sh
                    infrastructure:
                      type: KubernetesDirect
                      spec:
                        connectorRef: KUBE_CONNECTOR # harness kubernates connector
                        namespace: harness-delegate-ng
                        resources:
                          limits:
                            cpu: "0.5"
                            memory: 500Mi
                        annotations: {}
                        labels: {}
                        containerSecurityContext:
                          capabilities:
                            drop: []
                            add: []
                        nodeSelector: {}
                    reports:
                      type: JUnit
                      spec:
                        paths: []
                    outputVariables: []
                    envVariables: {}
                  timeout: 1h
              - step:
                  type: ShellScript
                  name: ShellScript_1
                  identifier: ShellScript_1
                  spec:
                    shell: Bash
                    executionTarget: {}
                    source:
                      type: Inline
                      spec:
                        script: echo "Deploying.."
                    environmentVariables: []
                    outputVariables: []
                  timeout: 10m
            rollbackSteps: []
        tags: {}
        failureStrategies:
          - onFailure:
              errors:
                - AllErrors
              action:
                type: StageRollback
  properties:
    ci:
      codebase:
        connectorRef: CONNECTOR
        repoName: REPO_NAME
        build: <+input>
        sparseCheckout: []
  notificationRules:
    - name: devopsbugbashwp5
      identifier: devopsbugbashwp5
      pipelineEvents:
        - type: AllEvents
      notificationMethod:
        type: Webhook
        spec:
          webhookUrl: https://{instance_url}/api/sn_devops/v2/devops/tool/orchestration?toolId={tool sys id}&projectId={project sys id}&ni.nolog.token={token}
      enabled: true
```

**Note:** If you want to add the Sonar Scan Results and Security Scan Results on the same stage, you can use different step names for both the custom actions by updating their default value in the **sonar\_step\_names** and **security\_step\_names** fields in the sn\_devops\_tool\_integration\_configuration table.

