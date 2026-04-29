---
title: Artifacts and packages
description: Artifacts and packages enable DevOps Change Velocity to track development and testing activities across a wide range of deployment and release models. This feature ensures that pipeline activity stored in the DevOps data model can be retrieved and applied when artifacts are created and released at different times or in different pipelines.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Artifacts and packages

Artifacts and packages enable DevOps Change Velocity to track development and testing activities across a wide range of deployment and release models. This feature ensures that pipeline activity stored in the DevOps data model can be retrieved and applied when artifacts are created and released at different times or in different pipelines.

**Artifacts**

When an artifact version is registered, related activities like commits, tests, and code scans are tracked so that regardless of when the artifact version is deployed, those details can be retrieved. It can be in the current pipeline execution, a later execution of the same pipeline, a pipeline that is triggered by the current one, or a separate pipeline that is triggered independently.

When you associate commits with an artifact version \(CI pipeline\), and define an artifact package \(CD pipeline\), all artifact versions generated since the last time the app was deployed to production are included in the list of commits for the change. Consolidation of these items is helpful, especially when there are multiple CI builds before the deployment.

DevOps change request attributes:

-   **Category** DevOps or the **Categorize DevOps change requests on "DevOps Change" field** check box is selected in DevOps properties. For more information, see [DevOps change request without mandating category as DevOps](../task/create-devops-change-any-category.md).
-   Commits and Work Items related lists

**Packages**

A package tracks when one or more artifact versions are being used in a deployment pipeline. This provides two important benefits:

1.  Retrieval of activities for all artifact versions declared in the package. For example, for use in an automated change approval policy.
2.  Recording when a specified artifact version was successfully released, ensuring that information tied to them is no longer considered. For example, for later change requests.

## Artifact setup

1.  [Create an artifact tool record in DevOps](integrating-devops-change-with-third-party-tools.md).

    **Note:** An artifact tool isn’t necessary unless a webhook or user-created integration subflow configuration is required to look up artifact versions.

2.  Register artifacts in the CI pipeline.
3.  Create a package in the CD pipeline.

    **Note:** The package creation step must be before the Prod Deploy step.


## Artifact registration

Configure artifact registration in a scripted pipeline or freestyle job using the [DevOps API](https://www.servicenow.com/docs/access?context=devops-api&version=australia&pubname=australia-api-reference&ft:locale=en-US) `/artifact/registration` endpoint. Multiple artifact versions are supported.

For Jenkins pipeline:

-   Scripted and declarative pipeline \(`snDevOpsArtifact` Jenkinsfile command\)

    For example:

    ```
    snDevOpsArtifact(artifactsPayload: """{"artifacts": [{"name": "sa-web.jar", "version": "1.9","semanticVersion": "1.9.0","repositoryName": "services-1031"}], "branchName": "master"}""")
    ```

-   Freestyle job \(**Register Artifact** build step\)

    For example:

    ```
    {"artifacts":[{"name":"sentiment-analysis-web2","version":"1.9","semanticVersion":"1.9.0","repositoryName":"maven-releases"}]}
    ```


## Artifact package creation

**Important:** You must add the package creation step before the change step in your pipeline, and package creation must be added in a stage which is previous to the change step, so that packages are linked to the pipeline execution for a change request.

Configure artifact package creation in a scripted pipeline or freestyle job using the [DevOps API](https://www.servicenow.com/docs/access?context=devops-api&version=australia&pubname=australia-api-reference&ft:locale=en-US) `/package/registration` endpoint.

**Note:** Package name must be specified.

For Jenkins pipeline:

-   Freestyle job \(**Create Package** build step\)

    For example:

    ```
    {"artifacts":[{"name":"sentiment-analysis-web2","version":"1.9","repositoryName":"maven-releases"}]}
    ```

-   Declarative and scripted pipeline \(`snDevOpsPackage` Jenkinsfile command\)

    Package with more than one artifact \(from different repos\) in the payload, for example:

    ```
    snDevOpsPackage(name: "sentimentpackage", artifactsPayload: """{"artifacts":[{"name": "sa-web.jar", "version": "1.9", "repositoryName": "services-1031"}, "{"name": "sa-db.jar", "version": "1.3.2", "repositoryName": "services-1032"}], "branchName": "master"}""")
    ```

    ![DevOps change acceleration for releases package](../image/dev-ops-change-releases.png)


**Note:** When an artifact version isn’t available during the build, build details \(pipelineName or projectName, taskExecutionNumber, stageName, branchName\) are used to look up the artifact version in the task execution.

Jenkins plugin step `includeBuildInfo` can be used to include build details in the API call.

## Artifact workflow and objects

The orchestration tool job publishes the new artifact \(consisting of versions\) to the artifact repository. Each artifact version is associated with a task execution \(consisting of the related code commits\). A package is created for the release \(consisting of specific artifact versions flagged for deployment\) and, after the deployment stage completes, the package is marked as deployed to production.

These objects are part of the artifact structure.

-   **Artifact tool**

    Used to support artifact repository managers such as JFrog Artifactory.

    **Note:** An artifact tool isn’t necessary unless a webhook or user-created integration subflow configuration is required to look up artifact versions.

-   **Artifact repository**

    Target for artifacts generated in a build, and also a source of artifacts required by a build. Can be created manually, or through the RegisterArtifact API as new artifacts are published under new repositories in a tool.

-   **Artifact**

    Artifact name for which different builds \(artifact versions\) are generated. Can be created manually, or through the RegisterArtifact API. Artifacts \(versions\) are associated with a task execution and published to an artifact repository.

-   **Artifact version**

    Specific version of the artifact. Deployable component of an application generated by a CI build. When provided, semantic version is used.

    Can be created through discovery, or through the RegisterArtifact API. Artifacts \(versions\) are associated with a task execution and published to a tracked artifact repository.

-   **Semantic version**

    Optional attribute of an artifact version that, when provided, is used to determine commits for a change. Semantic version format is \(MAJOR.MINOR.PATCH\).

-   **Package**

    Collection of artifact versions used as input to a CD pipeline, or for associating test results.

    Package creation is triggered by the CreatePackage API call from the orchestration tool and contains the name, version, and repository name of all the artifact versions included in the package. A check box indicates whether the package has been deployed to production.


DevOps change acceleration for releases:

![DevOps change request.](../image/dev-ops-category-change-request.png "DevOps change request – category DevOps")

![DevOps change request commits.](../image/dev-ops-change-request-artifacts.png "DevOps change request – commits and work items")

![DevOps artifact version list.](../image/dev-ops-artifact-version-list.png "DevOps artifact version list")

![DevOps artifact commits.](../image/dev-ops-artifact-commits.png "DevOps artifact version – commits")

![DevOps artifact packages.](../image/dev-ops-artifacts-packages.png "DevOps artifact version – packages")

![DevOps package.](../image/dev-ops-package.png "DevOps package")

You can also see all existing pipeline change requests directly from the **Changes** module in the application navigator.

You can see all existing change control and pipeline change requests directly using the **Changes** module in the application navigator.

Navigate to **DevOps Change Workspace** &gt; **Changes** &gt; **Pipeline change requests** &gt; **All** for all change-related information.

**Pipeline change requests**

![Pipeline change requests.](../image/dev-ops-pipeline-req.png "Changes module")

You can see all the existing artifacts and packages directly using the **List** module in the application navigator.

Navigate to **DevOps Change Workspace** &gt; **Lists** &gt; **Artifact** for all artifact-related information.

![List of artifacts and packages.](../image/dev-ops-artifacts-list.png "List module")

## Artifacts and packages monitoring

When artifacts and packages are registered from a source tool into ServiceNow, they are often staged in the **sn\_devops\_artifact\_staging** table, while the remaining necessary data for creation and linkage of these objects is either received from inbound events, or fetched by DevOps flows.

Most of the times, these staging records are processed within a few seconds. But there may be cases where the necessary data is never received, so these records may be left idle. The **Description** field on the table below contains a summary of the details missing in such cases to help in easier monitoring.

**Note:** It is recommended to have unique artifact names for release builds, that is, different artifact names for builds running on different branch builds.

<table id="table_gf4_kd4_d1c"><thead><tr><th>

Staging type

</th><th>

Staging code

</th><th>

When can this occur

</th><th>

Final state?

</th><th>

Description

</th></tr></thead><tbody><tr><td>

create\_package\_association

</td><td>

WAITING\_FOR\_OTHER\_STAGED\_REQUESTS

</td><td>

During a package registration call, when the task execution where the call originated from is found in the system and post processed, but not all artifact versions passed in the artifacts payload have been found in the system.

</td><td>

No

</td><td>

Your package registration request is pending for the following reason:

 Task execution found for association \(TE00012345\) and post processing flag is set to true, but not all artifact versions were found.

 Total artifact count: 2

</td></tr><tr><td>

create\_package\_association

</td><td>

TASK\_EXEC\_POST\_PROCESSING\_PENDING

</td><td>

During a package registration call, when the task execution where the call originated from is found in the system but hasn’t yet been post processed. That is, the Completed webhook event for this task execution hasn’t yet been processed.

</td><td>

No

</td><td>

Your package registration request is pending for the following reason:

 Task execution found for association \(TE00012345\), but post processing complete flag is not set to true.

 Total artifact count: 2

</td></tr><tr><td>

create\_package\_association

</td><td>

NO\_TASK\_EXECUTION\_FOUND

</td><td>

During a package registration call, when the task execution where the call originated from isn’t yet found in the system.

</td><td>

No

</td><td>

Your package registration request is pending for the following reason:

 Task execution not found for association \(pipelineName=TestPipeline, stageName=Package, taskExecutionNumber=18\).

 Total artifact count: 2

</td></tr><tr><td>

create\_package

</td><td>

VERSION\_NOT\_FOUND

</td><td>

During a package registration call, when the artifact version passed in the artifacts payload hasn’t yet been found in the system.

</td><td>

No

</td><td>

Your package registration request is pending for the following reason:

 Artifact version not found \(name=TestArtifact, version=2.5, repositoryName=TestRepo, pipelineName=TestPipeline, stageName=Package, taskExecutionNumber=18\).

 Artifact count: 1 out of 2

</td></tr><tr><td>

create\_package

</td><td>

VERSION\_NOT\_FOUND

</td><td>

During a package registration call, when the artifact version isn’t passed in the artifacts payload, but it contains either a taskExecutionSysId or \(pipelineName, stageName, taskExecutionNumber\) that can be used to lookup the task execution record, which in this case is found and post processed, but doesn’t have any artifact version record associated.

</td><td>

No

</td><td>

Your package registration request is pending for the following reason:

 Artifact version not available in payload and not found using task execution details \(name=TestArtifact, version=2.5, repositoryName=TestRepo, pipelineName=TestPipeline, stageName=Package, taskExecutionNumber=18\) \(TE00012345\).

 Artifact count: 1 out of 2

</td></tr><tr><td>

create\_package

</td><td>

TASK\_EXEC\_POST\_PROCESSING\_PENDING

</td><td>

During a package registration call, when the artifact version isn’t passed in the artifacts payload, but it contains either a taskExecutionSysId or \(pipelineName, stageName, taskExecutionNumber\) that can be used to lookup the task execution record, which in this case is found but not yet post processed.

</td><td>

No

</td><td>

Your package registration request is pending for the following reason:

 Artifact version not available in payload, and task execution found for association but post processing complete flag is not set to true \(name=TestArtifact, version=2.5, repositoryName=TestRepo, pipelineName=TestPipeline, stageName=Package, taskExecutionNumber=18\) \(TE00012345\).

 Artifact count: 1 out of 2

</td></tr><tr><td>

create\_package

</td><td>

NO\_TASK\_EXECUTION\_FOUND

</td><td>

During a package registration call, when the artifact version isn’t passed in the artifacts payload, but it contains either a taskExecutionSysId or \(pipelineName, stageName, taskExecutionNumber\) that can be used to lookup the task execution record, which in this case isn’t found.

</td><td>

No

</td><td>

Your package registration request is pending for the following reason:

 Artifact version not available in payload, and task execution also not found for association \(name=TestArtifact, version=2.5, repositoryName=TestRepo, pipelineName=TestPipeline, stageName=Package, taskExecutionNumber=18\).

 Artifact count: 1 out of 2

</td></tr><tr><td>

create\_package

</td><td>

WAITING\_FOR\_OTHER\_STAGED\_REQUESTS

</td><td>

During a package registration call, when the artifact version passed in the artifacts payload has been found in the system, but must wait for the other related staging records to be processed \(including both create\_package or create\_package\_association records\).

</td><td>

No

</td><td>

Your package registration request is pending for the following reason:

 Artifact version found, but need to wait for the remaining package registration staging records.

 Artifact count: 1 out of 2

</td></tr><tr><td>

register\_artifact

</td><td>

TASK\_EXEC\_POST\_PROCESSING\_PENDING

</td><td>

During an artifact registration call, when the task execution where the call originated from is found in the system but hasn’t been post processed yet. That is the 'Completed' webhook event for this task execution hasn’t yet been processed.

</td><td>

No

</td><td>

Your artifact registration request is pending for the following reason:

 Artifact version created and task execution found for association for association \(TE00012345\), but post processing complete flag is not set to true.

</td></tr><tr><td>

register\_artifact

</td><td>

NO\_TASK\_EXECUTION\_FOUND

</td><td>

During an artifact registration call, when the task execution where the call originated from isn’t yet found in the system.

</td><td>

No

</td><td>

Your artifact registration request is pending for the following reason:

 Artifact version created, but task execution not found for association \(pipelineName=TestPipeline, stageName=Package, taskExecutionNumber=18\).

</td></tr><tr><td>

register\_artifact

</td><td>

VERSION\_ALREADY\_REGISTERED

</td><td>

During an artifact registration call, when the artifact version provided in the artifacts payload for a given artifact and repository, already exists in the system.

</td><td>

Yes \(Ignored\)

</td><td>

Your artifact registration request was ignored for the following reason:

 Artifact version has already been registered.

</td></tr><tr><td>

register\_artifact

</td><td>

NO\_SUBFLOW\_CONFIGURED

</td><td>

During an artifact registration call, when the artifact version isn’t provided in the artifacts payload, and both webhook and look-up subflow aren't to find the artifact version record.

</td><td>

Yes \(Ignored\)

</td><td>

Your artifact registration request was ignored for the following reason:

 Artifact version not available in payload. Webhook and look-up subflow are not available.

</td></tr><tr><td>

register\_artifact

</td><td>

NO\_TASK\_EXECUTION\_FOUND

</td><td>

During an artifact registration call, when the artifact version isn’t provided in the artifacts payload, but webhook is supported and the artifact version record can be found, but the task execution where the call originated from isn’t yet found in the system.

</td><td>

No

</td><td>

Your artifact registration request is pending for the following reason:

 Artifact version found via webhook, but task execution not found for association \(pipelineName=TestPipeline, stageName=Package, taskExecutionNumber=18\).

</td></tr><tr><td>

register\_artifact

</td><td>

TASK\_EXEC\_POST\_PROCESSING\_PENDING

</td><td>

During an artifact registration call, when the artifact version isn’t provided in the artifacts payload, but webhook is supported and the artifact version record can be found, and the task execution where the call originated from is found in the system but hasn’t been post processed yet. That is, the Completed webhook event for this task execution hasn’t yet been processed.

</td><td>

No

</td><td>

Your artifact registration request is pending for the following reason:

 Artifact version found via webhook and task execution found for association \(TE00012345\), but post processing complete flag is not set to true.

</td></tr><tr><td>

register\_artifact

</td><td>

NO\_TASK\_EXECUTION\_FOUND

</td><td>

During an artifact registration call, when the artifact version isn’t provided in the artifacts payload, but look-up subflow is supported and the artifact version record can be found, but the task execution where the call originated from isn’t yet found in the system.

</td><td>

No

</td><td>

Your artifact registration request is pending for the following reason:

 Artifact version found via lookup, but task execution not found for association \(pipelineName=TestPipeline, stageName=Package, taskExecutionNumber=18\).

</td></tr><tr><td>

register\_artifact

</td><td>

TASK\_EXEC\_POST\_PROCESSING\_PENDING

</td><td>

During an artifact registration call, when the artifact version isn’t provided in the artifacts payload, but look-up subflow is supported and the artifact version record can be found, and the task execution where the call originated from is found in the system but hasn’t been post processed yet. That is, the Completed webhook event for this task execution hasn’t yet been processed.

</td><td>

No

</td><td>

Your artifact registration request is pending for the following reason:

 Artifact version found via lookup and task execution found for association \(TE00012345\), but post processing complete flag is not set to true.

</td></tr><tr><td>

register\_artifact

</td><td>

ERROR\_CALLING\_SUBFLOW

</td><td>

During an artifact registration call, when the artifact version isn’t provided in the artifacts payload, and look-up subflow is supported but the artifact version couldn't be found.

</td><td>

Yes \(Ignored\)

</td><td>

Your artifact registration request was ignored for the following reason:

 Artifact version not found by the look-up subflow.

</td></tr><tr><td>

register\_artifact

</td><td>

ERROR\_CALLING\_SUBFLOW

</td><td>

During an artifact registration call, when the artifact version isn’t provided in the artifacts payload, and look-up subflow is supported but could not find the artifact version due to an error in the subflow.

</td><td>

Yes \(Ignored\)

</td><td>

Your artifact registration request was ignored for the following reason:

 Artifact version not found by the look-up subflow due to an error \(refer to DevOps logs for additional details\).

</td></tr><tr><td>

register\_artifact

</td><td>

ERROR\_CALLING\_SUBFLOW

</td><td>

During an artifact registration call, when the artifact version isn’t provided in the artifacts payload, and look-up subflow is supported but wasn’t executed because the parent artifact record could not be found in the system.

</td><td>

Yes \(Ignored\)

</td><td>

Your artifact registration request was ignored for the following reason:

 Artifact not found.

</td></tr></tbody>
</table>-   **[Commits included in DevOps change request](dev-ops-commits-release.md)**  
The DevOps artifact package and its associated artifact versions are used to determine which commits are included in a DevOps change.

**Parent Topic:**[Accelerating your DevOps change process](dev-ops-change-acceleration.md)

