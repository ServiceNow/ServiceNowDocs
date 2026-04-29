---
title: Azure DevOps pipeline tasks
description: Use these tasks in your Azure DevOps pipeline to interact with the DevOps Config data model.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Integrating your pipeline in DevOps Config, DevOps Config, IT Service Management]
---

# Azure DevOps pipeline tasks

Use these tasks in your Azure DevOps pipeline to interact with the DevOps Config data model.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

These tasks are provided to create a specific pipeline definition to achieve your goal.

-   ServiceNow-DevOps-Config-Agent-Upload-Config

    Upload config data to a deployable in the data model via Agent Job.

-   ServiceNow-DevOps-Config-Agent-Get-Snapshot

    Get the snapshots for an application.

-   ServiceNow-DevOps-Config-Agent-Get-Snapshot-Name

    Extract the name of a snapshot.

-   ServiceNow-DevOps-Config-Agent-Publish-Snapshot

    Publish a snapshot of your configuration data.

-   ServiceNow-DevOps-Config-Agent-Export-Snapshot

    Export a subset of your configuration data.

-   ServiceNow-DevOps-Config-Agent-Register-Pipeline

    Register a changeset and/or snapshot to a pipeline execution.

-   ServiceNow-DevOps-Config-Agent-Validate-Snapshot

    Validate configuration data against organization policies.

-   ServiceNow-DevOps-Server-Change-Acceleration

    Create a change request as part of the pipeline.


## ServiceNow-DevOps-Config-Agent-Upload-Config

Task to upload a configuration file to a given location within an application data model.

This task is meant to be used in an iterative nature for all config files the user chooses to upload to their application data model during the pipeline run.

**Note:** Pre-uploaded files must be in a compatible format.

-   **Input variables**

<table id="table_hpv_5x2_psb"><tbody><tr><td>

connectedServiceName

</td><td>

Specifies the DevOps pipeline endpoint connection.

</td></tr><tr><td>

applicationName

</td><td>

Specifies the application to where config data is uploaded.

</td></tr><tr><td>

deployableName

</td><td>

Specifies the deployable for the application \(required if target is deployable\).

</td></tr><tr><td>

uploadTarget

</td><td>

Specifies the data model target to where config data is uploaded \(for example, `component`, `collection`, `deployable`\).

</td></tr><tr><td>

collectionName

</td><td>

\(Optional\) Specifies the collection to where config data will be uploaded \(required if target is collection\).

</td></tr><tr><td>

namePath

</td><td>

Specifies the data model path to where config data is uploaded.

 **Note:** When uploading to a vars folder, you must start the name path with "vars/" to specifiy the variable folder path.

</td></tr><tr><td>

configFilePath

</td><td>

Specifies the source folder from which config data is uploaded to the component or deployable path in the data model.

 Empty is the root of the repo. Use variables if files are not in the repo \(for example, `$(agent.builddirectory)`\).

</td></tr><tr><td>

convertPath

</td><td>

\(Optional\) Specifies whether to preserve the directory structure of the configuration files \(with respect to the workspace\), and convert the directory to paths within the data model. Default is false.

</td></tr><tr><td>

dataFormat

</td><td>

Specifies the data format of the config\_file \(for example, `JSON`, `YAML`, `XML`, etc.\).

</td></tr><tr><td>

changesetNumber

</td><td>

\(Optional\) Specifies the \(open\) changeset to which this upload activity is associated. If not provided, a new changeset is created.

 **Note:** Only used for multiple upload scenarios.

</td></tr><tr><td>

autocommit

</td><td>

Specifies whether to commit configuration data after upload \(true/false\). Default is false.

</td></tr><tr><td>

autoValidate

</td><td>

Specifies whether to validate configuration data during commit \(true/false\). Default is true.

</td></tr></tbody>
</table>-   **Output variable**

<table id="table_qjq_rbb_w5b"><tbody><tr><td>

changesetNumber

</td><td>

Changeset record created/committed during the upload.

 Provide a name to the task so it can be used later in the pipeline \(per example, `componentUpload`\).

</td></tr></tbody>
</table>-   **Example - Upload config**

    ```
    
    -task: ServiceNow-DevOps-Config-Agent-Upload-Config
     name: componentUpload​
     inputs:​
       connectedServiceName: 'MyServiceNowInstance'​
       applicationName: 'PaymentDemo'​
       uploadTarget: 'component'​
       namePath: 'wep-api-v1.0'
       configFilePath: 'k8s/helm/values.yml'​
       dataFormat: 'yaml'
       autoCommit: true​
       autoValidate: true​
     
    ```

-   **Example - Multiple uploads \(component\)**

    You can call the upload task more than once to upload configuration data in different file formats from different locations, while still keeping the uploads part of one changeset.

    -   In the first upload, name the task so the changesetNumber output variable can be reused in subsequent uploads.

        YAML file upload:

        ```
        
        -task: ServiceNow-DevOps-Config-Agent-Upload-Config​
           name: componentUpload​
           inputs:​ 
             connectedServiceName: 'MyServiceNowInstance'​
             applicationName: 'PaymentDemo'​
             uploadTarget: 'component'​
             namePath: 'wep-api-v1.0'
             configFilePath: 'k8s/helm/values.yml'​
             dataFormat: 'yaml'
             autoCommit: false​
             autoValidate: false​
        ```

    -   In subsequent uploads, reference the changesetNumber output variable from the first upload as an input variable.

        JSON file upload:

        ```
        
        -task: ServiceNow-DevOps-Config-Agent-Upload-Config
           inputs:​
             connectedServiceName: 'MyServiceNowInstance'
             applicationName: 'PaymentDemo'
             uploadTarget: 'component'
             namePath: 'wep-api-v1.0'
             configFilePath: 'featureToggles/set1.json'
             dataFormat: 'json'
             autoCommit: true​
             autoValidate: true​
             changesetNumber: '$(componentUpload.changesetNumber)'
        ```

-   **Example - Multiple uploads \(collection and vars\)**

    You can call the upload task more than once to upload configuration data in different file formats from different locations, while still keeping the uploads part of one changeset.

    -   In the first upload, make sure to name the task so the changesetNumber output variable can be reused in subsequent uploads.

        XML file upload:

        ```
        
        -task: ServiceNow-DevOps-Config-Agent-Upload-Config​
           name: componentUpload​
           inputs:​ 
             connectedServiceName: 'MyServiceNowInstance'​
             applicationName: 'PaymentDemo'​
             uploadTarget: 'collection'​
             collectionName: 'release-1.0'​
             namePath: 'v1-common-configs'
             configFilePath: 'infra/v1/config.xml'​
             dataFormat: 'xml'
             autoCommit: false​
             autoValidate: false​
        ```

    -   In subsequent uploads, reference the changesetNumber output variable from the first upload as an input.

        JSON file upload:

        ```
        
        -task: ServiceNow-DevOps-Config-Agent-Upload-Config
           inputs:​
             connectedServiceName: 'MyServiceNowInstance'
             applicationName: 'PaymentDemo'
             uploadTarget: 'deployable'
             deployableName: 'Production-EMEA'
             namePath: 'vars/dbSettings'
             configFilePath: 'infra/prodc/dbSettings.json'
             dataFormat: 'json'
             autoCommit: true​
             autoValidate: true​
             changesetNumber: '$(componentUpload.changesetNumber)'
        ```

    **Note:** To upload to a variable folder, uploadTarget must be set to `deployable`, and the correct values must be set for deployableName and changesetNumber.


## ServiceNow-DevOps-Config-Agent-Get-Snapshot

This task is intended to be used in different scenarios:

-   Retrieve a specific snapshot.

    Following the CD flow, a specific snapshot is retrieved so it can be published and then exported to be consumed downstream \(for example, to provision out infrastructure or application\).

-   Retrieve latest validated snapshot.

    The latest validated snapshot is retrieved for the given application-deployable combination.

-   Retrieve all snapshots for any impacted deployables.

    When config files are uploaded to an application data model, the system will create snapshots for any deployables determined to be impacted by the upload. Following along the CI flow, assuming the last Upload call had validation enabled, the next step would be to iterate through the list of snapshots and ensure they all passed validation.

-   Retrieve the latest snapshots for a deployable of an application in the event an upload does not generate any snapshots.

    A set of config data is available to deploy to an environment for an application-deployable-changeset combination when no configuration changes are made.

-   Show policy validation results in a pipeline execution.

    View policy validation results as test results on the ADO build tests results page, including compliant with exception, when getting a snapshot.


-   **Input variables**

<table id="table_dmc_nz2_psb"><tbody><tr><td>

connectedServiceName

</td><td>

Specifies the DevOps pipeline endpoint connection \(defined in the service connection settings of the project\).

</td></tr><tr><td>

applicationName

</td><td>

Specifies the application to upload config data to, or export data from.

</td></tr><tr><td>

deployableName

</td><td>

\(Optional\) Specifies the deployable \(per the specified application\) on which to get the latest snapshot data.

</td></tr><tr><td>

changesetNumber

</td><td>

\(Optional\) Specifies the changeset ID for the applicable set of config changes.

</td></tr><tr><td>

isValidated

</td><td>

\(Optional\) Specifies whether to return only snapshots that are passed, or passed with exception \(true/false\). Default is true.

</td></tr><tr><td>

continueWithLatest

</td><td>

\(Optional\) Specifies whether to return the latest snapshot per the `applicationName`-`deployableName`-`changesetNumber` combination if no snapshots are generated \(true/false\). Default is false.

</td></tr></tbody>
</table>-   **Output variable**

<table id="table_gb4_yfb_w5b"><tbody><tr><td>

snapshotObject

</td><td>

A JSON object containing the requested snapshots.

 Provide a name to the task so it can be used later in the pipeline \(per example, `getSnapshot`\).

</td></tr></tbody>
</table>-   **Example - Specific snapshot**

    ```
    
    -task: ServiceNow-DevOps-Config-Agent-Get-Snapshot
     name: getSnapshot
     inputs:
       connectedServiceName: 'MyServiceNowInstance'
       applicationName: 'PaymentDemo'
       deployableName: 'Production'
       changesetNumber: 'Chset-16'
       isValidated: true
       continueWithLatest: true
    
    ```

-   **Example - Latest validated snapshots \(for a given application-deployable combination\)**

    ```
    
    -task: ServiceNow-DevOps-Config-Agent-Get-Snapshot
     name: getSnapshot
     inputs:
       connectedServiceName: 'MyServiceNowInstance'
       applicationName: 'PaymentDemo'
       deployableName: 'Production'
       isValidated: true
    
    ```

-   **Example - All changeset snapshots**

    ```
    
    -task: ServiceNow-DevOps-Config-Agent-Get-Snapshot
     name: getSnapshot
     inputs:
       connectedServiceName: 'MyServiceNowInstance'
       applicationName: 'PaymentDemo'
       changesetNumber: 'Chset-16'
    
    ```

-   **Example - Show policy validation results**

    Assign a variable to the path of the file that contains the snapshot validation results generated during the `ServiceNow-DevOps-Config-Agent-Get-Snapshot` task.

    To load the snapshot validation results in your pipeline execution, you need to leverage the ADO native [Publish Test Results v2 task](https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/publish-test-results-v2?view=azure-pipelines&tabs=trx%2Ctrxattachments%2Cyaml), using the variable as an input.

    ```
    
    stages:
    - stage: Two
      jobs:
        - job: A
    	variables:
          - name: validationResultsPath
            value: 1/TEST_DATA_$(Build.DefinitionName)_$(Build.BuildNumber)_*.xml
          steps:
            - task: PublishTestResults@2
              inputs:
                 testResultsFormat: 'JUnit'
                 testResultsFiles: '$(validationResultsPath)'
                 searchFolder: '$(System.WorkFolder)'
    
    ```


## ServiceNow-DevOps-Config-Agent-Get-Snapshot-Name

This task is used as a follow-up from the `ServiceNow-DevOps-Config-Agent-Get-Snapshot-Name` task to get the snapshot name from a particular snapshot. From here, the snapshot name can be used as an input to a downstream task, like publishing the snapshot.

-   **Input variables**

<table id="table_ctq_f1f_psb"><tbody><tr><td>

deployableName

</td><td>

Specifies the deployable to get the snapshot object that was returned from the `ServiceNow-DevOps-Config-Agent-Get-Snapshot` task.

</td></tr><tr><td>

script

</td><td>

Specifies the script to extract the snapshot name from the snapshot object.

</td></tr></tbody>
</table>-   **Output variable**

<table id="table_u4n_hgb_w5b"><tbody><tr><td>

snapshotName

</td><td>

The snapshot name for the deployable.

 Provide a name to the task so it can be used later in the pipeline \(per example, `getSnapshotName`\).

</td></tr></tbody>
</table>-   **Example - Get snapshot name**

    Use this script to extract the snapshot name retrieved from the `ServiceNow-DevOps-Config-Agent-Get-Snapshot` task.

    ```
    
    -task: ServiceNow-DevOps-Config-Agent-Get-Snapshot-Name
     inputs:
       deployableName: 'PRD'
       script: |
    	function run() {
            let name;
            let deployableName = process.argv[2];
            let jsonObj = $(getSnapshot.snapshotObjects);
            let size = jsonObj.result.length;
            for(let i=0; i<size; i++) {
             obj = jsonObj.result[i];
             if(obj[“deployable_id.name”].toLowerCase() == deployableName) {
               name = obj.name;
               console.log(name);
              }
             }
            }
            run();
    
    ```

-   **Example - Get snapshot name used with get snapshot**

    Call the `ServiceNow-DevOps-Config-Agent-Get-Snapshot-Name` task right after the `ServiceNow-DevOps-Config-Agent-Get-Snapshot` task to return the snapshot name.

    Get snapshots \(returns a JSON object containing impacted snapshots\):

    ```
    
    -stage: Two​
     jobs:​
        -job: B​
         steps:​
            -task: ServiceNow-DevOps-Config-Agent-Get-Snapshot
             name: getSnapshot​
             inputs:​
                connectedServiceName: 'MyServiceNowInstance'​​
                applicationName: 'PaymentDemo'​
                deployableName: 'Production-2'
                changesetNumber: 'Chset-16'​
    ```

    Get snapshot name \(returns snapshot name for a specific deployable\):

    ```
    
    -stage: Two​
     jobs:​
        - job: B​
          steps:​
            - task: ServiceNow-DevOps-Config-Agent-Get-Snapshot
              name: getSnapshotName​
              inputs:​
                  deployableName: 'Production-2'
                  script:|​
                  function run() {​
                   let name;​
                   let deployableName = process.argv[2]; ​
                   let jsonObj = $(getSnapshot.snapshotObjects);​
                   let size = jsonObj.result.length;​
                   for(let i=0; i<size ;i++) {​
                    obj = jsonObj.result[i];​
                    if(obj["deployable_id.name"].toLowerCase() == deployableName) {​
                     name = obj.name;​
                     console.log(name); // This standard output of inline script is given as the task output​
                    }​
                   }​
                  }​
                  run();
    
    ```

    Use returned snapshot name in the pipeline \(for example, publish\):

    ```
    
    -stage: Three​
     jobs:​
        -job: C​
         variables:​
           varSnapshotName: $[stageDependencies.Two.B.outputs['getSnapshotName.snapshotName']]​
         steps:​
            -task: ServiceNow-DevOps-Config-Agent-Publish-Snapshot
             inputs:​
               connectedServiceName: 'MyServiceNowInstance'
               applicationName: 'PaymentDemo'
               deployableName: 'Production-2'
               snapshotName: '$(varSnapshotName)'​
    ```


## ServiceNow-DevOps-Config-Agent-Publish-Snapshot

This task publishes a snapshot for the given application and deployable. From here, the snapshot can be consumed through the Export process.

-   **Input variables**

<table id="table_vd4_41f_psb"><tbody><tr><td>

connectedServiceName

</td><td>

Specifies the ServiceNow endpoint connection.

</td></tr><tr><td>

applicationName

</td><td>

Specifies the application to publish.

</td></tr><tr><td>

deployableName

</td><td>

Specifies the deployable for the application to publish config data.

</td></tr><tr><td>

snapshotName

</td><td>

Specifies the name of the snapshot to publish.

</td></tr></tbody>
</table>-   **Output variable**

    Not applicable \(returns true if successful, otherwise false\).

-   **Example**

    ```
    
    -task: ServiceNow-DevOps-Config-Agent-Publish-Snapshot
     inputs:
       connectedServiceName: 'MyServiceNowInstance'
       applicationName: 'PaymentDemo'
       deployableName: 'Production-2'
       snapshotName: 'Production-v23.dpl'
    
    ```


## ServiceNow-DevOps-Config-Agent-Export-Snapshot

This task exports a snapshot for the given application and deployable. Specify the exporter, relevant exporter arguments, the export format \(for example, YAML, JSON, etc.\), and output location for the exported config data. From here, the config data can be used directly as an input for a deployment or provisioning tool downstream in the pipeline.

-   **Input variables**

<table id="table_mtx_bbf_psb"><tbody><tr><td>

connectedServiceName

</td><td>

Specifies the ServiceNow endpoint connection.

</td></tr><tr><td>

applicationName

</td><td>

Specifies the application from which to publish.

</td></tr><tr><td>

deployableName

</td><td>

Specifies the deployable for the application from which to export config data.

</td></tr><tr><td>

snapshotName

</td><td>

Specifies the name of the snapshot from which to export config data.

</td></tr><tr><td>

exporterName

</td><td>

Specifies the exporter to apply to the snapshot \(for example, `UniqueCDIs`\).

</td></tr><tr><td>

args

</td><td>

\(Optional\) Specifies arguments to be used along with the exporter.

</td></tr><tr><td>

exportFormat

</td><td>

Specifies the format to export the snapshot data \(for example, `INI`, `YAML`, `PROPS`\).

</td></tr><tr><td>

saveFile

</td><td>

Checks if file is to be saved to an Azure repository \(true/false\). Default is false.

 **Note:** Appropriate permission/OAuth token access to script is required.

 Otherwise the export file is created in the pipeline workspace directory.

</td></tr></tbody>
</table>-   **Output variable**

    Not applicable \(returns true if successful, otherwise false\).

-   **Example**

    ```
    
    -task: ServiceNow-DevOps-Config-Agent-Export-Snapshot
     inputs:
       connectedServiceName: 'MyServiceNowInstance'
       applicationName: 'PaymentDemo'
       deployableName: 'Production-2'
       exporterName: 'returnAllData-nowPreview'
       dataFormat: 'yaml'
       args: ''
       snapshotName: 'Production-v23.dpl'
       saveFile: true​
       fileName: 'ExporterOutput/ExportData_$(build.definitionName)_$(build.buildNumber).yaml'
       
    ```


## ServiceNow-DevOps-Config-Agent-Register-Pipeline

This task ties a changeset and a snapshot to the pipeline so that it can be tracked during the pipeline execution. In DevOps Change Velocity, this is shown in the Pipeline UI.

-   **Input variables**

<table id="table_nym_4cf_psb"><tbody><tr><td>

connectedServiceName

</td><td>

Specifies the DevOps pipeline endpoint connection.

</td></tr><tr><td>

applicationName

</td><td>

Specifies the application name.

</td></tr><tr><td>

changesetNumber

</td><td>

\(Optional\) Specifies the ID of the changeset to associate to the pipeline execution.

</td></tr><tr><td>

snapshotName

</td><td>

\(Optional\) Specifies the name of the snapshot to associate to the pipeline execution.

</td></tr></tbody>
</table>-   **Output variable**

    Not applicable \(returns true if successful, otherwise false\).

-   **Example**

    ```
    
    -task: ServiceNow-DevOps-Config-Agent-Publish-Snapshot
     inputs:
       connectedServiceName: 'MyServiceNowInstance'
       changesetNumber: 'Changeset-143'
    
    ```


## ServiceNow-DevOps-Config-Agent-Validate-Snapshot

Validate config data against your organization policies.

-   **Input variables**

<table id="table_hk2_nkf_psb"><tbody><tr><td>

connectedServiceName

</td><td>

Specifies the ServiceNow endpoint connection.

</td></tr><tr><td>

applicationName

</td><td>

Specifies the application to validate.

</td></tr><tr><td>

deployableName

</td><td>

Specifies the deployable \(per the specified application\) to validate.

</td></tr><tr><td>

snapshotName

</td><td>

\(Optional\) Specifies the name of the snapshot to validate.

</td></tr><tr><td>

showResults

</td><td>

\(Optional\) Specifies to show validation results in the console log.

</td></tr></tbody>
</table>-   **Output variable**

    Not applicable \(returns true if successful, otherwise false\).

-   **Example**

    ```
    
    -task: ServiceNow-DevOps-Config-Agent-Validate-Snapshot
     inputs:
       connectedServiceName: 'MyServiceNowInstance'
       applicationName: 'PaymentDemo'
       deployableName: 'Production-2'
       snapshotName: ''
       showResults: false
    
    ```


## ServiceNow-DevOps-Server-Change-Acceleration

This task is required for agentless \(server\) jobs to automatically create a change request in ServiceNow Change Management as part of the Azure DevOps pipeline.

In DevOps Config, to associate multiple snapshots of the same changeset to a change request, use snapshot name and application name to track specific configuration data for a given application service.

See [Accelerating your DevOps change process](../../enterprise-dev-ops/concept/dev-ops-change-acceleration.md) for more information regarding the DevOps Change Acceleration feature.

-   **Input variables \(related to DevOps Config\)**

<table id="table_tsl_wsf_w5b"><tbody><tr><td>

connectedServiceName

</td><td>

Specifies the DevOps pipeline endpoint connection.

</td></tr><tr><td>

applicationName

</td><td>

Application associated with the snapshot being attached to the change request.

</td></tr><tr><td>

snapshotName

</td><td>

Name of the snapshot to attach to the change request.

</td></tr></tbody>
</table>-   **Example**

    ```
    
    -stage: ChangeRequest
     jobs:
        -job: 'changerequestjob'
         pool: server
         steps:
            -task: ServiceNow-DevOps-Server-Change-Acceleration
             inputs:
                connectedServiceName: 'MyServiceNowInstance'
                applicationName: 'PaymentDemo'
                snapshotName: 'Production-v23.dpl'
    
    ```


## YAML pipeline example

```
trigger:
  branches:
    include:
    - none
stages:
- stage: One
  displayName: Upload Configuration Data
  pool:
    vmImage: ubuntu-latest
  jobs:
  - job: A
    displayName: Upload
    steps:
    - task: ServiceNow-DevOps-Config-Agent-Upload-Config@1
      name: componentUpload
      inputs:
        connectedServiceName: 'MyServiceNowInstance'
        applicationName: 'PaymentDemo'
        uploadTarget: 'component'
        configFile: 'k8s/helm/values.yml'
        namePath: 'processor-api-v1.0'
        dataFormat: 'yaml'
        autoValidate: true
        autoCommit: true
        convertPath: true
- stage: Two
  displayName: Get Latest Snapshot
  pool:
    vmImage: ubuntu-latest
  jobs:
  - job: B
    displayName: Get Snapshot
    variables:
    - name: varChangesetNumber
      value: $[stageDependencies.One.A.outputs['componentUpload.changesetNumber'] ]
    - name: varConfigValidationResults
        value: 1/TEST_DATA_$(Build.DefinitionName)_$(Build.BuildNumber)_*.xml
    steps:
    - task: ServiceNow-DevOps-Config-Agent-Get-Snapshot@1
      name: getSnapshot
      inputs:
        connectedServiceName: 'MyServiceNowInstance'
        applicationName: 'PaymentDemo'
        deployableName: 'Production-EMEA'
        changeSetNumber: '$(varChangesetNumber)'
        continueWithLatest: true
    - task: ServiceNow-DevOps-Config-Agent-Get-Snapshot-Name@1
      name: getSnapshotName
      inputs:
        deployableName: 'Production-EMEA'
        script: "function run() {\n  let name;\n  let deployableName = process.argv[2]; \n  let jsonObj = $(getSnapshot.snapshotObjects);\n  let size = jsonObj.result.length;\n  for(let i=0; i<size ;i++) {\n    obj = jsonObj.result[i];\n    if(obj[\"deployable_id.name\"].toLowerCase() == deployableName) {\n      name = obj.name;\n      console.log(name);   // This standard output of inline script is given as the task output\n    }\n  }\n}\nrun();\n"
    - task: PublishTestResults@2
          inputs:
             testResultsFormat: ‘JUnit’
             testResultsFiles: ‘$(varConfigValidationResults)’
             searchFolder: ‘$(System.WorkFolder)’
    - task: ServiceNow-DevOps-Config-Agent-Register-Pipeline@1
      inputs:
        connectedServiceName: 'MyServiceNowInstance'
        snapshotName: '$(getSnapshotName.snapshotName)'
        applicationName: 'PaymentDemo'
- stage: Three
  displayName: Publish Snapshot
  pool:
    vmImage: ubuntu-latest
  jobs:
  - job: C
    displayName: Publish
    variables:
    - name: varSnapshotName
      value: $[stageDependencies.Two.B.outputs['getSnapshotName.snapshotName']]
    steps:
    - task: ServiceNow-DevOps-Config-Agent-Publish-Snapshot@1
      inputs:
        connectedServiceName: 'MyServiceNowInstance'
        applicationName: 'PaymentDemo'
        deployableName: 'Production-EMEA'
        snapshotName: '$(varSnapshotName)'
- stage: ChangeRequest
  dependsOn:
  - Two
  - Three
  jobs:
  - job: 'changerequestjob'
    timeoutInMinutes: 2
    pool:
      name: server
    variables:
    - name: varSnapshotName
      value: $[stageDependencies.Two.B.outputs['getSnapshotName.snapshotName']]
    steps:
    - task: ServiceNow-DevOps-Server-Change-Acceleration@1
      inputs:
        connectedServiceName: 'MyServiceNowInstance'
        applicationName: 'PaymentDemo'
        snapshotName: '$(varSnapshotName)'
- stage: Four
  displayName: Export Snapshot
  dependsOn:
  - Two
  - Three
  - ChangeRequest
  pool:
    vmImage: ubuntu-latest
  variables:
  - name: varSnapshotName
    value: $[stageDependencies.Two.B.outputs['getSnapshotName.snapshotName']]
  jobs:
  - job: D
    displayName: Export
    steps:
    - task: ServiceNow-DevOps-Config-Agent-Export-Snapshot@1
      inputs:
        connectedServiceName: 'MyServiceNowInstance'
        applicationName: 'PaymentDemo'
        deployableName: 'Production-EMEA'
        exporterName: 'returnAllData-now'
        dataFormat: 'yaml'
        snapshotName: '$(varSnapshotName)'
        saveFile: true
        fileName: 'ExportData_$(build.definitionName)_$(build.buildNumber).yaml'
    - task: CmdLine@2
      inputs:
        script: |
          echo Write your commands here
          echo Hello world
          tree $(Pipeline.Workspace)
```

