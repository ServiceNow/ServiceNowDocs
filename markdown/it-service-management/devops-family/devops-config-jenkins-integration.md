---
title: Jenkins pipeline actions
description: Use these actions in your Jenkins pipeline to interact with the DevOps Config data model.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [Integrate, DevOps Config, IT Service Management]
---

# Jenkins pipeline actions

Use these actions in your Jenkins pipeline to interact with the DevOps Config data model.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Jenkins scripted and declarative piplines are supported.

These actions are provided to create a specific pipeline definition to achieve your goal. Add a command to your Jenkins file to perform these actions.

-   snDevOpsConfig

    Combined action to upload, validate, and publish config data.

-   snDevOpsConfigUpload

    Upload config data to DevOps Config via Agent Job.

-   snDevOpsConfigGetSnapshots

    Retrieve snapshots for a specific deployable, or all impacted deployables.

-   snDevOpsConfigPublish

    Publish a snapshot for the given application and deployable.

-   snDevOpsConfigExport

    Export a snapshot for a given application and deployable.

-   snDevOpsConfigRegisterPipeline

    Tie a changeset and/or snapshot to a pipeline execution.

-   snDevOpsConfigValidate

    Validate config data against your organization policies.

-   snDevOpsChange

    Create a change request with associated snapshot attached.


## snDevOpsConfig

Upload, validate, and publish config data changes in one step.

This action combines snDevOpsConfigUpload, snDevOpsConfigGetSnapshots, and snDevOpsConfigRegisterPipeline actions into one action, rather than having to execute each action separately.

-   **Input variables**

<table id="table_mqp_lxp_cyb"><tbody><tr><td>

configFile

</td><td>

Specifies the configuration data file to upload to the component or deployable path in the data model.

</td></tr><tr><td>

applicationName

</td><td>

Specifies the application to where config data will be uploaded.

</td></tr><tr><td>

target

</td><td>

Specifies the data model target to where config data will be uploaded \(for example, `component`, `collection`, `deployable`\).

</td></tr><tr><td>

collectionName

</td><td>

\(Optional\) Name of the collection to upload to \(required if target is collection\).

</td></tr><tr><td>

deployableName

</td><td>

\(Optional\) Name of the deployable to upload to \(required if target is deployable\).

</td></tr><tr><td>

namePath

</td><td>

Specifies the name path in the data model to where config data will be uploaded.

 **Note:** When uploading to a vars folder, you must start the name path with "vars/" to specifiy the variable folder path.

</td></tr><tr><td>

dataFormat

</td><td>

Specifies the data format of the config file \(for example, `JSON`, `YAML`, `XML`, etc.\)

</td></tr><tr><td>

autoCommit

</td><td>

Specifies whether to commit configuration data after upload \(true/false\). Default is true.

</td></tr><tr><td>

autoValidate

</td><td>

Specifies whether to validate configuration data during commit \(true/false\). Default is true.

</td></tr><tr><td>

autoPublish

</td><td>

Specifies whether to publish the configuration data after validation \(true/false\). Default is true.

</td></tr><tr><td>

changesetNumber

</td><td>

\(Optional\) Specifies the \(open\) changeset to which this upload activity is associated. If not provided, a new changeset is created.

 **Note:** Only used for multiple upload scenarios.

</td></tr><tr><td>

markFailed

</td><td>

\(Optional\) Fail the pipeline in the event that the validation attempt failed \(due to a backend issue\).

</td></tr><tr><td>

showResults

</td><td>

\(Optional\) Show validation results in the Jenkins job console log.

</td></tr><tr><td>

continueWithLatest

</td><td>

\(Optional\) Specifies whether to return the latest snapshot per the `applicatioName`-`deployableName`-`changesetNumber` combination if no snapshots are generated \(true/false\). Default is false.

</td></tr></tbody>
</table>-   **Output**
    -   If successful, a snapshot or set of snapshots.
    -   If failure, an API/backend failure message is shown.
-   **Example**
    -   Input:

        ```
        
        snapshotObj = snDevOpsConfig(
             applicationName: "PaymentDemo",
             configFile: "config/application/Collection/Collection2/*.json",
             target: "collection",
             collectionName: "release-1.0",
             namePath: "settings/infrastructure/database",
             dataFormat: "json",
             autoCommit: 'true',
             autoValidate: 'true',
             autoPublish: 'true',
             continueWithLatest: 'true',
             markFailed: 'true',
             showResults: 'false'
        )
        
        echo"*************************\n ${snapshotObj}"
        ```

    -   Output![Jenkins snDevOpsConfig response output](../image/devops-config-jenkins-response.png)
-   **Example - collection**

    **Note:** When uploading to a collection, the `collectionName` argument is required.

    ```
    
    snDevOpsConfig(
         applicationName: 'PaymentDemo',
         target: 'collection',
         collectionName: 'release-1.0',
         namePath: 'web-api-v1.0',
         configFile: 'k8s/helm/*.yml',
         dataFormat: 'yaml',
         autoCommit: 'true',
         autoValidate: 'true',
         autoPublish: 'true'
    )
    ```

-   **Example - deployable**

    **Note:** When uploading to a deployable, the `deployableName` argument is required.

    ```
    
    snDevOpsConfig(
         applicationName: 'PaymentDemo',
         target: 'deployable',
         deployableName: 'Production',
         namePath: 'web-api-v1.0',
         configFile: 'k8s/helm/*.yml',
         dataFormat: 'yaml',
         autoCommit: 'true',
         autoValidate: 'true',
         autoPublish: 'true'
    )
    ```

-   **Multiple uploads in one commit**

    To upload configuration data from different locations, or to upload a set of data to multiple targets \(for example, one component, one deployable\) tracked as a single commit to your data model, you can call the `snDevOpsConfigUpload` action as many times as necessary for the first set of uploads, then call the `snDevOpsConfig` action for the final upload.​

    Here's an example.

    -   In the first upload, create a variable \(for example, $changeset\), and assign the return value of the step to it so it can be reused in subsequent uploads​.

        Upload 1 - XML file to component:

        ```
        
        $changeset = snDevOpsConfigUpload(
             applicationName: 'PaymentDemo',
             target: 'component',
             namePath: 'paymentService-v1.0',
             configFile: 'infra/v1/config.xml',
             dataFormat: 'xml',
             autoCommit: 'false',
             autoValidate: 'false',
             autoPublish: 'false'
        )
        ```

    -   In subsequent uploads \(and final upload\), use the variable as an input​.

        Upload 2 - JSON file to vars folder of deployable:

        ```
        
        snDevOpsConfig(
             applicationName: 'PaymentDemo',
             target: 'deployable',
             deployableName: 'Production',
             namePath: 'vars/dbSettings',
             configFile: 'infra/prod/dbConfig.json',
             dataFormat: 'json',
             changesetNumber: ”${changeset}”,
             autoCommit: 'false',
             autoValidate: 'false',
             autoPublish: 'false',
             continueWithLatest: 'true'
        )
        ```

-   **Upload multiple data formats**

    To upload configuration data in different file formats, you can call the `snDevOpsConfig` action with these specifications.

    -   Ensure the `configFile` argument is using a wildcard in the path.
    -   Do not specify the `dataFormat` argument.
    Here's an example.

    -   Let's say we have these config files.

        ![DevOps Config Jenkins upload files](../image/devops-config-jenkins-files.png)

    -   This is how to upload the config files using `snDevOpsConfig`.

        ```
        
        snDevOpsConfig(
             applicationName: 'PaymentDemo',
             target: 'component',
             namePath: 'paymentService-v1.0',
             configFile: 'infra/v1/*',
             autoCommit: 'true',
             autoValidate: 'true',
             autoPublish: 'true'
        )
        ```


## snDevOpsConfigUpload

This action uploads a configuration file to a given location within an application data model.

It is meant to be used in an iterative nature for all config files to upload to the application data model during the pipeline run.

Supports:

-   Upload to:
    -   A component, collection, or deployable.
    -   The variable \(vars\) folder of a component, collection, or deployable.
-   Regex pattern for config file input.
-   Ability to be called multiple times in the same pipeline.

-   **Input variables**

<table id="table_ct3_qqf_psb"><tbody><tr><td>

configFile

</td><td>

Specifies the configuration data file to upload to the component or deployable path in the data model.

</td></tr><tr><td>

applicationName

</td><td>

Specifies the application to where config data will be uploaded.

</td></tr><tr><td>

target

</td><td>

Specifies the data model target to where config data will be uploaded \(for example, `component`, `collection`, `deployable`\).

</td></tr><tr><td>

collectionName

</td><td>

\(Optional\) Name of the collection to upload to \(required if target is collection\).

</td></tr><tr><td>

deployableName

</td><td>

Name of the deployable to upload to \(required if target is deployable\).

</td></tr><tr><td>

namePath

</td><td>

Specifies the name path in the data model to where config data will be uploaded.

 **Note:** When uploading to a vars folder, you must start the name path with "vars/" to specifiy the variable folder path.

</td></tr><tr><td>

dataFormat

</td><td>

Specifies the data format of the config file \(for example, `JSON`, `YAML`, `XML`, etc.\)

</td></tr><tr><td>

convertPath

</td><td>

\(Optional\) Specifies whether to preserve the directory structure of configuration files \(with respect to the workspace\) and convert the directory to paths within the data model.

</td></tr><tr><td>

changesetNumber

</td><td>

\(Optional\) Specifies the \(open\) changeset to which this upload activity is associated. If not provided, a new changeset is created.

 **Note:** Only used for multiple upload scenarios.

</td></tr><tr><td>

autoCommit

</td><td>

Specifies whether to commit configuration data after upload \(true/false\). Default is false.

</td></tr><tr><td>

autoValidate

</td><td>

Specifies whether to validate configuration data during commit \(true/false\). Default is false.

</td></tr></tbody>
</table>-   **Output variable**

<table id="table_iz5_2ng_hvb"><tbody><tr><td>

changesetNumber

</td><td>

\(Optional\) Specifies the \(open\) changeset to which this upload activity is associated.

 If a changeset number is not provided, a new changeset is created.

</td></tr></tbody>
</table>-   **Example**
    -   Input:

        Here is an example of the `snDevOpsConfigUpload` action. For the sake of illustration, we’ll assign the response to a variable, `changeSetId`, which could be echoed out to our console log for debugging scenarios.

        ```
        
        changeSetId = snDevOpsConfigUpload(
             applicationName: "PaymentDemo",
             target: 'component',
             namePath: "web-api-v1.0",
             configFile: "k8s/helm/values.yml",
             dataFormat: "json",
             autoCommit: 'true',
             autoValidate: 'true'
        )
        
        echo "Changeset: $changeSetId created"
        ```

    -   Output:

        In addition to the data being uploaded to our data model in DevOps Config, the output would look something like this \(using the Blue Ocean plugin to visualize the console output\).

        ![DevOps Config Configuration Upload output](../image/devops-config-jenkins-up-output.png)

-   **Example - Multiple uploads \(component\)**

    You can call the upload action more than once to upload configuration data in different file formats from different locations, while still keeping the uploads part of one changeset.

    -   In the first upload, name the action so the changesetNumber output variable can be reused in subsequent uploads.

        YAML file upload:

        ```
        
        $changeset = snDevOpsConfigUpload(
             applicationName: 'PaymentDemo',
             target: 'component',
             namePath: 'wep-api-v1.0',
             configFile: 'k8s/helm/values.yml',
             dataFormat: 'yaml',
             autoCommit: 'false',
             autoValidate: 'false'
        )
        ```

    -   In subsequent uploads, reference the changesetNumber output variable from the first upload as an input variable.

        3 JSON files upload:

        ```
        
        snDevOpsConfigUpload(
             applicationName: 'PaymentDemo',
             target: 'component',
             namePath: 'wep-api-v1.0',
             configFile: 'infra/*.json',
             dataFormat: 'json',
             autoCommit: 'false',
             autoValidate: 'false',
             changesetNumber: ”${changeset}”
        )
        ```

    -   In the final call, in addition to referencing the changesetNumber output variable from the first upload as an input variable, set autoCommit and autoValidate to `true`.

        INI file upload:

        ```
        
        snDevOpsConfigUpload(
             applicationName: 'PaymentDemo',
             target: 'component',
             namePath: 'wep-api-v1.0',
             configFile: 'featureToggles/set1.ini',
             dataFormat: 'ini',
             autoCommit: 'true',
             autoValidate: 'true',
             changesetNumber: ”${changeset}”
        )
        ```

-   **Example - Multiple uploads \(collection and vars\)**

    You can call the upload action more than once to upload configuration data in different file formats from different locations, while still keeping the uploads part of one changeset.

    -   In the first upload, create a variable \(for example, $changeset\), and assign the return value of the step to it so it can be reused in subsequent uploads.

        XML file upload:

        ```
        
        $changeset = snDevOpsConfigUpload(
             applicationName: 'PaymentDemo',
             target: 'collection',
             collectionName: 'release-v1.0',
             namePath: 'v1-common-configs',
             configFile: 'infra/v1/config.xml',
             dataFormat: 'xml',
             autoCommit: 'false',
             autoValidate: 'false'
        )
        ```

    -   In subsequent uploads, use the variable as an input.

        JSON file upload:

        ```
        
        snDevOpsConfigUpload(
             applicationName: 'PaymentDemo',
             target: 'deployable',
             deployableName: 'Production',
             namePath: 'vars/dbSettings',
             configFile: 'infra/prod/dbConfig.json',
             dataFormat: 'json',
             autoCommit: 'true',
             autoValidate: 'true',
             changesetNumber: ”${changeset}”
        )
        ```

    **Note:** To upload to a variable folder, uploadTarget must be set to `deployable`, and the correct values must be set for deployableName and changesetNumber.


## snDevOpsConfigGetSnapshots

This action is intended to be used in different scenarios:

-   Retrieve all snapshots for any impacted deployables.

    When config files are uploaded to an application data model, the system will create snapshots for any deployables determined to be impacted by the upload. Following along the CI flow, assuming the last Upload call had validation enabled, the next step would be to iterate through the list of snapshots and ensure they all passed validation.

-   Retrieve a specific snapshot.

    Following the CD flow, a specific snapshot is retrieved so it can be published and then exported to be consumed downstream \(for example, to provision out infrastructure or application\).

-   Retrieve the latest snapshots for a deployable of an application in the event an upload does not generate any snapshots.

    A set of config data is available to deploy to an environment for an application-deployable-changeset combination when no configuration changes are made.

-   Show policy validation results in a pipeline execution.

    View policy validation results as test results on the Jenkins build tests results page, including compliant with exception, when getting a snapshot.


-   **Input definitions**

<table id="table_hmn_3rf_psb"><tbody><tr><td>

applicationName

</td><td>

Specifies the application to upload config data to or export data from.

</td></tr><tr><td>

deployableName

</td><td>

\(Optional\) Specifies the deployable for the application on which to get the latest snapshot data.

</td></tr><tr><td>

changesetNumber

</td><td>

\(Optional\) Specifies the changeset ID for the set of config changes the user is interested in.

</td></tr><tr><td>

isValidated

</td><td>

\(Optional\) Specifies whether to return only snapshots that are passed, or passed with exception \(true/false\). Default is true.

</td></tr><tr><td>

continueWithLatest

</td><td>

\(Optional\) Specifies whether to return the latest snapshot per the `applicatioName`-`deployableName`-`changesetNumber` combination if no snapshots are generated \(true/false\). Default is false.

</td></tr></tbody>
</table>-   **Output**
    -   If successful, a snapshot or set of snapshots.
    -   If failure, an API/backend failure message is shown.
-   **Example**
    -   Specific snapshot \(specified\):

        ```
        
        $snapshots = snDevOpsConfigGetSnapshots(
             applicationName: 'PaymentDemo',
             deployableName: 'Production',
             changesetNumber: 'Chset-16',
             isValidated: 'true',
             continueWithLatest: 'true'
        )
        ```

    -   Latest validated snapshot \(returns the latest snapshot for application and deployable combination\):

        ```
        
        $snapshots = snDevOpsConfigGetSnapshots(
             applicationName: 'PaymentDemo',
             deployableName: 'Production',
             isValidated: 'true'
        )
        ```

    -   All changeset snapshots \(returns all snapshots for application and deployable combination\):

        ```
        
        $snapshots = snDevOpsConfigGetSnapshots(
             applicationName: 'PaymentDemo',
             changesetNumber: 'Chset-16'
        )
        ```

    -   Show policy validation results in a pipeline execution.

        1.  Assign a variable to the path of the file that contains the snapshot validation results generated during the `snDevOpsConfigGetSnapshots` action.
        2.  Call the [JUnit action](https://plugins.jenkins.io/junit/) to load the snapshot validation results into the pipeline execution test section.
        ```
        
        stage('Validate') {
            steps {
        	script {
                   changeSetResults = snDevOpsConfigGetSnapshots( … )
                   if (!changeSetResults) {
                      echo "No snapshots were created"
                   } else {
        	       def changeSetResultsObject = readJSON text: changeSetResults
        
        	       changeSetResultsObject.each {
                          snapshotName = it.name
                          snapshotObject = it
        	       }
        	       // STEP 1
        		validationResultsPath = "${snapshotName}_${currentBuild.projectName}_${currentBuild.number}.xml"
        	    }
        	}
            }
        }
        
        post {
            always {
                // STEP 2
                junit testResults: "${validationResultsPath}", skipPublishingChecks: true
            }
        }
        
        ```


## snDevOpsConfigPublish

This action publishes a snapshot for the given application and deployable. From here, the snapshot can be consumed through the Export process.

-   **Input definitions**

<table id="table_i4g_xrf_psb"><tbody><tr><td>

applicationName

</td><td>

Specifies the application from which to publish config data.

</td></tr><tr><td>

deployableName

</td><td>

Specifies the deployable for the application from which to publish config data.

</td></tr><tr><td>

snapshotName

</td><td>

Specifies the name of the snapshot to publish.

</td></tr></tbody>
</table>-   **Output**
    -   If successful, true.
    -   Otherwise false.
-   **Example**

    ```
    
    snDevOpsConfigPublish(
         applicationName: 'PaymentDemo',
         deployableName: 'Production',
         snapshotName: 'Production-v23.dpl',
    )
    ```


## snDevOpsConfigExport

This action exports a snapshot for the given application and deployable.

The user should specify the exporter, relevant exporter arguments, the export format \(for example, YAML, JSON, etc.\), and output location for the exported config data.

From here, the config data can be used directly as an input for a deployment or provisioning tool downstream in the pipeline.

-   **Input arguments**

<table id="table_syy_nsf_psb"><tbody><tr><td>

applicationName

</td><td>

Specifies the application from which to export data.

</td></tr><tr><td>

deployableName

</td><td>

Specifies the config deployable for the application from which to export data.

</td></tr><tr><td>

snapshotName

</td><td>

\(Optional\) Specifies snapshot from which to export data.

 If a snapshot is not specified, the latest snapshot for the deployable is used.

</td></tr><tr><td>

exporterName

</td><td>

Specifies the exporter to apply to the snapshot \(for example, `UniqueCDIs`\).

</td></tr><tr><td>

exporterArgs

</td><td>

\(Optional\) Specifies arguments to be used along with the exporter.

</td></tr><tr><td>

exportFormat

</td><td>

Specifies the format to export the snapshot data \(For example, `INI`, `YAML`, `PROPS`\).

</td></tr><tr><td>

fileName

</td><td>

Specifies the file to export data to \(assumed to be in the workspace\).

 If a filename is not specified, a concatenation of application name and deployable name \(plus file extension\) is used by default.

</td></tr></tbody>
</table>-   **Output**
    -   If successful, true.
    -   Otherwise false.
-   **Example**

    ```
    
    snDevOpsConfigExport(
         applicationName: 'PaymentDemo',
         deployableName: 'Production',
         snapshotName: 'Production-v23.dpl',
         exporterFormat: 'yaml',
         exporterName: 'returnAllData-now',
         exporterArgs: '',
         fileName: 'exported_file-Production-20220302.yml'
    )
    ```


## snDevOpsConfigRegisterPipeline

This action ties a changeset and/or snapshot to the pipeline so that it can be tracked during the pipeline execution. In DevOps Change Velocity, this is shown in the Pipeline UI.

See [Accelerating your DevOps change process](../../enterprise-dev-ops/concept/dev-ops-change-acceleration.md) for more information regarding the DevOps Change Acceleration feature.

-   **Input arguments**

<table id="table_uql_ctf_psb"><tbody><tr><td>

applicationName

</td><td>

Specifies the name of the application.

</td></tr><tr><td>

changesetNumber

</td><td>

\(Optional\) Specifies the changeset to associate with the pipeline execution.

 **Note:** Specify either changesetNumber or snapshotName, but not both.

</td></tr><tr><td>

snapshotName

</td><td>

\(Optional\) Specifies the name of the snapshot to associate to the pipeline execution.

 **Note:** Specify either changesetNumber or snapshotName, but not both.

</td></tr></tbody>
</table>-   **Output**
    -   If successful, true.
    -   Otherwise false.
-   **Example**
    -   Input:

        Here is an example of the `snDevOpsConfigRegisterPipeline` action. For the sake of illustration, we’ll assign the response to a variable, `changeSetRegResult`, which could be echoed out to our console log for debugging scenarios.

        ```
        
        changeSetRegResult = snDevOpsConfigRegisterPipeline(
             applicationName: "PaymentDemo",
             changesetNumber: "Chset-122"
        )
        
        echo "Pipeline registration result: ${changeSetRegResult}"
        ```

    -   Output:

        In addition to the data being uploaded to our data model in DevOps Config, the output would look something like this \(using the Blue Ocean plugin to visualize the console output\).

        ![DevOps Configuration Register Pipeline output](../image/devops-config-jenkins-reg-output.png)


## snDevOpsConfigValidate

Validate config data against your organization policies.

-   **Input arguments**

<table id="table_e1d_zdj_psb"><tbody><tr><td>

applicationName

</td><td>

Application to validate.

</td></tr><tr><td>

deployableName

</td><td>

Deployable for the application to validate.

</td></tr><tr><td>

snapshotName

</td><td>

\(Optional\) Name of the snapshot to validate.

</td></tr><tr><td>

markFailed

</td><td>

\(Optional\) Fail the pipeline in the event that the validation attempt failed \(due to a backend issue\).

</td></tr><tr><td>

showResults

</td><td>

\(Optional\) Show validation results in the Jenkins job console log.

</td></tr></tbody>
</table>-   **Output**
    -   If successful, no output.
    -   If failure, an API/backend failure message is shown.
-   **Example**
    -   Specific snapshot \(specified\):

        ```
        
        snDevOpsConfigValidate(
             applicationName: 'PaymentDemo',
             deployableName: 'Production',
             snapshotName: 'Production-v23.dpl',
        )
        ```

    -   Latest snapshot \(retrieves and validates the latest snapshot for application and deployable combination\):

        ```
        
        $changeset = snDevOpsConfigValidate(
             applicationName: 'PaymentDemo',
             deployableName: 'Production'
        )
        ```


## snDevOpsChange

Create a change request and attach a snapshot for reference.

See [Accelerating your DevOps change process](../../enterprise-dev-ops/concept/dev-ops-change-acceleration.md) for more information regarding the DevOps Change Acceleration feature.

-   **Input arguments**

<table id="table_w5k_x5x_mxb"><tbody><tr><td>

applicationName

</td><td>

Specifies the name of the application.

</td></tr><tr><td>

snapshotName

</td><td>

Specifies the name of the snapshot to associate with the change request.

</td></tr></tbody>
</table>-   **Example**

    ```
    
    snDevOpsChange(
         applicationName: 'PaymentDemo',
         snapshotName: 'Production-v23.dpl'
    )
    ```


## Jenkins pipeline example

```

pipeline {
    environment {
        buildArtifactsPath = "build_artifacts/${currentBuild.number}"
        validationResultsPath = ""
    }

    agent any

    stages {
        // Initialize pipeline
        stage('Initialize') {
            steps {
                script {
                    // DevOps Config application related information
                    appName = 'PaymentDemo'
                    deployableName = 'Production'
                    componentName = "web-api-v1.0"
                    collectionName = "release-1.0"
                    // Configuration file information
                    exportFormat = 'yaml'
                    configFilePath = "k8s/helm/values.yml"
                    // Exporter related information
                    exporterName = 'returnAllData-nowPreview' 
                    exporterArgs = ''
                    // Jenkins variables declared to be used in pipeline
                    exportFileName = "${buildArtifactsPath}/export_file-${appName}-${deployableName}-${currentBuild.number}.${exportFormat}"
                    changeSetId = ""
                    snapshotName = ""
                    snapshotObject = ""
                    isSnapshotValidateionRequired = false
                    isSnapshotPublisingRequired = false
                }
            }
        }
            
        // Validate configuration data changes
        stage('Validate') {
            parallel {
                stage('Config') {
                    stages('Config Steps') {
                        // Upload configuration data to DevOps Config
                        stage('Upload, Validate, & Publish') {
                            steps {
                                sh "echo uploading and auto-validating configuration file: ${configFilePath}"
                                script {
                                    changeSetResults = snDevOpsConfig(
                                        applicationName: "${appName}",
                                        target: 'component',
                                        namePath: "${componentName}",
                                        configFile: "${configFilePath}",
                                        dataFormat: "${configFileFormat}",
                                        autoCommit: 'true',
                                        autoValidate: 'true',
                                        autoPublish: 'true',
                                        isValidated: 'true',
                                        continueWithLatest: 'true',
                                        markFailed: 'true'
                                    )

                                    echo "Snapshots generated, validated, and published: ${changeSetResults}"

                                    def changeSetResultsObject = readJSON text: changeSetResults

                                    changeSetResultsObject.each {
                                        snapshotName = it.name
                                        snapshotObject = it
                                    }

                                    validationResultsPath = "${snapshotName}_${currentBuild.projectName}_${currentBuild.number}*.xml"
                                }
                            }
                        }
                        // Export published snapshot to be used by downstream deployment tools
                        stage('Export') {
                            steps {
                                script {
                                    // create build artifacts dir to store export file
                                    sh "mkdir -p ${buildArtifactsPath}"
                                    
                                    exportResponse = snDevOpsConfigExport(
                                        applicationName: "${appName}",
                                        snapshotName: "${snapshotObject.name}",
                                        deployableName: "${deployableName}",
                                        exporterFormat: "${exportFormat}",
                                        fileName: "${exportFileName}",
                                        exporterName: "${exporterName}",
                                        exporterArgs: "${exporterArgs}"
                                    )
                                }
                            }
                        }
                    }
                }
            }
        }
        
        // Create change request and attach snapshot for reference
        stage('Change Management') {
            steps {
                script {
                    // Trigger change request
                    snDevOpsChange(
                        applicationName: "${appName}",
                        snapshotName: "${snapshotName}"
                    )
                }     
            }
        }
    }
    // NOTE: attach snapshot validation results to run (if the snapshot fails validation)
    post {
        always {
            // attach policy validation results
            junit testResults: "${validationResultsPath}", skipPublishingChecks: true
        }
    }
}

```

