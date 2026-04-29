---
title: Configure JFrog in Jenkins
description: Configure JFrog plugin for Jenkins to publish, deploy, or download artifacts.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure JFrog in Jenkins

Configure JFrog plugin for Jenkins to publish, deploy, or download artifacts.

## Before you begin

Role required: admin role in Jenkins

## Procedure

1.  Install the [Artifactory](https://plugins.jenkins.io/artifactory/) plugin, to integrate Jenkins with JFrog, to publish, deploy, or download artifacts.

2.  After the installation, configure the JFrog server details from **Manage Jenkins** &gt; **Configure System**.

    **Note:**

    To be able to integrate JFrog with Jenkins, the build info must be published for JFrog along with the artifacts.

    ![Enter JFrog instance details.](../image/jenkins-jfrog-config.png)

3.  Use the following scripts to download or upload artifacts to Jenkins.

    Scripted pipeline to upload:

    ```
          def server = Artifactory.server 'JFROG1'
                    def uploadSpec = """{
                       "files": [{
                         "pattern": "${env.WORKSPACE}/target/artifact-1.3.jar",
                          "target": "default-docker-virtual/"
                       }]
                    }"""
    
                 def buildInfo = server.upload(uploadSpec) 
                 server.publishBuildInfo buildInfo
    ```

    Scripted pipeline to download:

    ```
    
              def server = Artifactory.server 'JFROG1'
                    def downSpec= """{
                       "files": [{
                          "pattern": "default-docker-local/artifact-1.3.jar",
                         "target":"/var/jfrog_artifacts/"
                       }]
                    }"""
    
                 def buildInfo = server.download(downSpec) 
                 server.publishBuildInfo buildInfo 
    
    ```


**Parent Topic:**[Jenkins integration with DevOps Change Velocity](../concept/jenkins-integration-dev-ops.md)

