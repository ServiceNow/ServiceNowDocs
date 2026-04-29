---
title: Managing Azure DevOps artifacts
description: DevOps Change Velocity makes it easy to manage artifacts published through Azure DevOps build pipelines. You can import and track these artifacts and manage the packages in DevOps Change Velocity.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Managing Azure DevOps artifacts

DevOps Change Velocity makes it easy to manage artifacts published through Azure DevOps build pipelines. You can import and track these artifacts and manage the packages in DevOps Change Velocity.

Types of artifact sources supported by DevOps Change Velocity:

-   Build
-   Azure Artifacts

## Build Artifacts

Build and pipeline artifacts published using the Publish Build Artifacts \(PublishBuildArtifacts\) and Publish Pipeline Artifacts \(PublishPipelineArtifacts\) tasks respectively on the Azure DevOps are automatically created in your DevOps Change Velocity instance. You can also import historical data for build artifacts.

Build artifacts created using the Publish Build Artifacts task will be part of the artifact repository whose name will be defaulted to the build pipeline name.

**Note:** If two artifacts with the same name, belonging to the same repository, and having different versions are used as release triggers for a release pipeline, then the related lists \(like work items, commits, test summaries, and so on\) will include DevOps data related to both the artifact versions when a change exists in the release pipeline. For example, if artifact-1.0 and artifact-2.0 are release triggers to manage rollback scenarios in deployment, then change \(if part of the release pipeline\) will include related lists data for both the versions.

You can also continue to leverage the existing Extension-based artifact registration and import. For more information, see [Use the ServiceNow DevOps extension for Azure DevOps and Azure DevOps custom actions](../task/config-dev-ops-extensions-azure.md#) and [Artifacts and packages](using-dev-ops-release-change.md).

**Important:** Using Extension-based artifact registration isn’t required if the PublishBuildArtifacts and PublishPipelineArtifacts tasks mentioned above are used.

## Azure Artifacts

You can import and track the artifacts to your DevOps Change Velocity instance. You can import Azure DevOps artifacts that are published to the Azure Artifacts using the Universal Package task only.

**Note:** Only **Universal** packages are currently supported for importing and tracking.

\(DevOps 1.35 and later versions\) The **Feed connection alias** field is available on the Azure DevOps Tools form. This field is auto-populated with an alias for the feed connection. For more information about connecting a DevOps tool, see [Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md).

After upgrade, to select and add the artifact repositories using App Onboarding, you must select **Discover** to discover existing artifact repositories. The records are added to the Artifact Repositories related list. For more information about the adding artifact repositories, see [Associate tool objects to applications - Workspace](../task/apps-associate-objects-wkspc.md).

For tracking the artifact repositories, change the value of the **Track** column to True \(default value, False\).![Screen shot for the Tools page showing Feed connection alias field and Artifact Repositories related list.](../image/dev-ops-ado-artifact-connection-alias.png)

When an Azure Artifact is published via the Universal Package Task, the artifact information is associated with a build pipeline within 24 hours using the **ADO Artifacts Daily** scheduled job.

**Note:**

-   As Azure DevOps Artifact creation is not dependent on Build Pipeline completion. If Azure DevOps Artifact is used as Trigger for a Release Pipeline, it would be triggered even if Build pipeline is pending completion due to a change request.
-   The scheduled job is executed every 24 hours by default and can also be executed on-demand. However, as the scheduled job is performance intensive, it shouldn’t be executed frequently.

The following points must be considered while importing Azure DevOps artifacts:

1.  Artifacts can’t be published from the Release Pipelines due to Azure DevOps limitations.
2.  Artifact Repositories are tracked as follows:
    -   Historical Import of Azure DevOps artifacts is accomplished using the App Onboarding. For more information, see [Associate tool objects to applications - Workspace](../task/apps-associate-objects-wkspc.md).
    -   For real-time tracking of the artifacts, the value for the **Track** column must be changed to True \(default value, False\). Otherwise, the Feed or Artifact Repository won’t be tracked.
3.  The application supports the project-specific feeds but not the Organization specific feeds. Azure DevOps artifacts when published through Azure DevOps pipeline are only supported.
4.  Azure DevOps artifacts not linked to any build or release pipeline \(orphan artifacts\) aren’t supported.
5.  Azure DevOps Artifacts are stored in the following format:
    -   Azure DevOps artifact linked to only Build Pipeline \(or\) Build and Release Pipeline:

        *&lt;artifact-name&gt;-&lt;1.build-number.0&gt; \(Build Number of Build Pipeline\)*

    -   Azure DevOps artifact linked only to Release Pipeline:

        *&lt;artifact-name&gt;-&lt;1.build-number.0&gt; \(Build Number of Release Pipeline\)*


## Azure DevOps Artifact mapping with DevOps Change Velocity

The following table explains the mapping of Azure DevOps artifacts with ServiceNow DevOps fields:

|Azure DevOps Artifact|DevOps Change Velocity|
|---------------------|----------------------|
|Feeds|Artifact Repositories|
|Packages|Artifacts|
|Provenance/build number|Versions|

## Limitations

-   Azure DevOps Artifact Project with 4000 Feeds \(or less\) is supported.
-   Azure DevOps artifact Feed with 800 packages or artifacts \(or less\) is supported.
-   Azure DevOps pipeline with 200 packages or artifacts \(or less\) publishing is supported.

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](azure-devops-integration-dev-ops.md)

