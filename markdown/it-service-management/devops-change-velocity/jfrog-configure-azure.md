---
title: Configure Azure DevOps for JFrog
description: Configure your Azure DevOps instance to enable upload and download of JFrog artifacts.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [JFrog, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure Azure DevOps for JFrog

Configure your Azure DevOps instance to enable upload and download of JFrog artifacts.

The following settings are required in your Azure DevOps instance:

1.  Install the plugin [JFrog Artifactory](https://marketplace.visualstudio.com/items?itemName=JFrog.jfrog-artifactory-vsts-extension).
2.  Select your project and navigate to **Project settings** &gt; **Pipelines** &gt; **Service connections**.
3.  Select **New service connection**, search and select the installed **JFrog Artifactory** plugin, and select **Next**.
4.  Enter your JFrog instance details and create a service connection for JFrog.

    ![New JFrog Artifactory service connection.](../image/jfrog-config-azure-01.png)

    **Note:** The **Username** and **Password** fields must contain the credentials to your JFrog instance entered in the **Server URL** field.


## Upload artifacts from Azure DevOps to JFrog

To upload artifacts:

1.  Navigate to your project pipeline.
2.  In your stage for uploading, add the task **Artifactory Generic Upload** for uploading artifacts.
3.  For the **Artifactory Generic Upload** task:

    1.  Select the service connection you created for JFrog.
    2.  In the **Spec** field, entire your file spec.
    3.  Select the **Collect build info** check box.
    4.  The **Build number** field should contain the **BuildId** parameter.
    5.  Select **Add**.
    ![Artifactory Generic Upload task.](../image/jfrog-config-azure-02.png)

4.  Add the task **Artifactory Publish Build Info** for publishing build info.
5.  For the **Artifactory Publish Build Info** task:

    1.  Select the service connection you created for JFrog.
    2.  The **Build number** field should contain the **BuildId** parameter.
    3.  Select **Add**.
    ![Artifactory Publish Build Info task.](../image/jfrog-config-azure-03.png)


**Sample pipeline to upload artifacts from Azure DevOps to JFrog**

```

trigger:
- none
pool: 
  vmImage: ubuntu-latest
 

variables:
- group: Variable Group

stages:
  - stage: upload_artifact
    jobs:
      - job: 'upload'
        steps:
        - script: echo Hello, world!
          displayName: 'Run a one-line script'
        - task: ArtifactoryGenericUpload@2
          inputs:
            artifactoryService: 'JFrogCloud'
            specSource: 'taskConfiguration'
            fileSpec: |
              {
                "files": [
                  {
                    "pattern": "servicenow-app-devops.zip",
                    "target": "local-repo"
                  }
                ]
              }
            collectBuildInfo: true
            buildName: '$(Build.DefinitionName)'
            buildNumber: '$(Build.BuildId)'
            failNoOp: true'
        - task: ArtifactoryPublishBuildInfo@1
          inputs:
            artifactoryService: 'JFrogCloud'
            buildName: '$(Build.DefinitionName)'
            buildNumber: '$(Build.BuildId)'
```

## Download artifacts from JFrog to Azure DevOps

To download artifacts:

1.  Navigate to your project pipeline.
2.  In your stage for downloading, add the task **Artifactory Generic Download** for downloading artifacts.
3.  For the **Artifactory Generic Download** task:
    1.  Select the service connection you created for JFrog.
    2.  In the **Spec** field, entire your file spec.
    3.  Select the **Collect build info** check box.
    4.  The **Build number** field should contain the **BuildId** parameter.
    5.  Select **Add**.
4.  Add the task **Artifactory Publish Build Info** for publishing build info.
5.  For the **Artifactory Publish Build Info** task:
    1.  Select the service connection you created for JFrog.
    2.  The **Build number** field should contain the **BuildId** parameter.
    3.  Select **Add**.

**Sample pipeline to download artifacts from Azure DevOps to JFrog**

```

trigger:
- none
pool: 
  vmImage: ubuntu-latest
 

variables:
- group: Variable Group

stages:        
  - stage: download_artifact
    jobs:
      - job: 'download'
        steps:
        - task: ArtifactoryGenericDownload@3
          inputs:
            connection: 'JFrogCloud'
            specSource: 'taskConfiguration'
            fileSpec: |
              {
                "files": [
                  {
                    "pattern": "local-repo/servicenow-app-devops.zip",
                    "target": "/tmp/"
                  }
                ]
              }
            collectBuildInfo: true
            buildName: '$(Build.DefinitionName)'
            buildNumber: '$(Build.BuildId)'
            failNoOp: true
        - task: ArtifactoryPublishBuildInfo@1
          inputs:
            artifactoryService: 'JFrogCloud'
            buildName: '$(Build.DefinitionName)'
            buildNumber: '$(Build.BuildId)'
```

**Parent Topic:**[JFrog integration with DevOps Change Velocity](../concept/devops-jfrog-integration.md)

